﻿---
title: 'Lync Server 2013: バックエンド サーバーの高可用性'
TOCTitle: バックエンド サーバーの高可用性
ms:assetid: c559aacb-4e1d-4e78-9582-41f966ad418d
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ205248(v=OCS.15)
ms:contentKeyID: 48273536
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 のバックエンド サーバーの高可用性

 

_**トピックの最終更新日:** 2013-08-12_

バックエンド サーバーの高可用性を確保するには、同期 SQL ミラーリングと SQL クラスタリングのいずれかを使用します。これらのいずれかのソリューションの使用はオプションですが、組織のビジネス継続性を維持するには推奨されます。非同期 SQL ミラーリングは、Lync Server 2013 でのバックエンド サーバーの高可用性用にはサポートされていません。これ以降、特に指定がない限り、SQL ミラーリングは同期 SQL ミラーリングを意味するものとします。

トポロジ ビルダーを使用すると、SQL ミラーリングを簡単に設定できます。SQL フェールオーバー クラスタリングの場合、設定に SQL Server を使用する必要があります。

障害復旧用の別のフロントエンド プールとペアになっているプールで SQL ミラーリングと SQL クラスタリングのいずれかを使用する場合、両方のプールで同じバックエンド高可用性ソリューションを使用する必要があります。SQL ミラーリングを使用しているプールと、SQL クラスタリングを使用しているプールをペアにすることできません。

SQL ミラーリングを展開すると、プール内のすべての Lync Server データベースがミラー化されます。これには、中央管理ストア (そのプールに存在する場合) および応答グループ アプリケーション データベースとコール パーク アプリケーション データベース (これらのアプリケーションがプール内で実行している場合) も含まれます。

SQL ミラーリングでは、サーバーに対して共有ストレージを使用する必要はありません。各サーバーは、データベースのコピーをローカル ストレージに保持します。

SQL ミラーリングの展開では、監視を使用することも使用しないこともできます。バックエンド サーバーのフェールオーバーが自動的になるので、監視を使用することをお勧めします。使用しない場合は、管理者が手動でフェールオーバーを実行する必要があります。監視を展開した場合でも、管理者は必要に応じてバックエンド サーバーのフェールオーバーを手動で開始できます。

監視を使用する場合は、バックエンド サーバーの複数のペアに対して 1 つの監視を使用できます。監視とバックエンド サーバーのペアを 1 対 1 で対応させる必要はありません。ただし、バックエンド サーバーの複数のペアに対して 1 つの監視を使用する展開は、ペアごとに異なる監視を使用するトポロジほど復元性が高くありません。

SQL クラスタリングのサポートの詳細については、「[Lync Server 2013 でのデータベース ソフトウェアのサポート](lync-server-2013-database-software-support.md)」を参照してください。SQL クラスタリングの展開の詳細については、「[Lync Server 2013 での SQL Server クラスタリングの構成](lync-server-2013-configure-sql-server-clustering.md)」を参照してください。

## SQL ミラーリングを使用したバックエンド サーバーの自動フェールオーバーの復旧時間

SQL ミラーリングを使用した自動バックエンド フェールオーバーの場合、目標復旧時間 (RTO) のエンジニアリング目標は 5 分です。同期 SQL ミラーリングなので、バックエンド サーバー障害の間にデータ損失が発生する可能性は、サーバー間のデータ移動中にフロントエンド サーバーとバックエンド サーバーの両方が同時にダウンするという希な状況を除き、ありません。目標復旧ポイント (RPO) のエンジニアリング目標は 5 分です。

## SQL ミラーリングを使用したバックエンド サーバー障害の間のユーザー エクスペリエンス

障害の間のユーザー エクスペリエンスは、障害の特徴とトポロジによって異なります。

監視を構成してあり、プリンシパルで障害が発生した場合は、SQL ミラーリングを使用したバックエンド サーバーのフェールオーバーは自動的かつ迅速に行われます。使用中のユーザーがセッションで大きな中断を感じることはありません。

監視を構成してない場合は、管理者がフェールオーバーを手動で実行するまでにしばらく時間がかかります。その間、使用中のユーザーが影響を受ける可能性があります。ユーザーは約 30 分、通常どおりにセッションを続行します。プライマリがまだ復元されない場合、または管理者がバックアップにフェールオーバーしなかった場合は、ユーザーは復元モードに切り替えられます。つまり、 Lync Server での永続的な変更が必要なタスク (連絡先の追加など) を実行することはできません。

プリンシパルとミラーの両方のバックエンド サーバーで障害が発生した場合、またはどちらかのサーバーと監視で障害が発生した場合は、バックエンド サーバーは使用できなくなります (プリンシパルがまだ動作していたとしても)。この場合、使用中のユーザーはしばらくしてから復元モードに切り替えられます。

