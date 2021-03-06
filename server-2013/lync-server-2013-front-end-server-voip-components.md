﻿---
title: 'Lync Server 2013: フロント エンド サーバーの VoIP コンポーネント'
TOCTitle: フロント エンド サーバーの VoIP コンポーネント
ms:assetid: 310e81a7-da45-47d4-95d0-92837e386502
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg425812(v=OCS.15)
ms:contentKeyID: 48271676
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 のフロント エンド サーバーの VoIP コンポーネント

 

_**トピックの最終更新日:** 2012-10-01_

フロント エンド サーバーの VoIP コンポーネントは次のとおりです。

  - 変換サービス

  - 着信ルーティング コンポーネント

  - 発信ルーティング コンポーネント

  - Exchange UM ルーティング コンポーネント

  - 内部クラスター ルーティング コンポーネント

  - [Lync Server 2013 の仲介サーバー コンポーネント](lync-server-2013-mediation-server-component.md)

## 変換サービス

変換サービスは、ダイヤルされた電話番号を、管理者が定義した正規化ルールに基づいて E.164 形式またはその他の形式に変換するサーバー コンポーネントです。変換サービスでは、独自の番号付けシステムを使用する組織や E.164 をサポートしていないゲートウェイまたは PBX を使用する組織の場合は、E.164 以外の形式に変換できます。

## 着信ルーティング コンポーネント

着信ルーティング コンポーネントは、主に エンタープライズ VoIP クライアントのユーザーが指定した任意の設定に従って、着信通話を処理します。着信ルーティング コンポーネントはまた、ユーザーが設定した場合に、代理人着信および同時着信を行います。たとえば、ユーザーは、不在時の着信を転送するか、それとも単に通知に記録するかを指定します。着信の転送を有効にした場合は、不在時の着信を、別の電話番号または着信応答が構成されている Exchange UM サーバーに転送するように指定できます。着信ルーティング コンポーネントは、すべての Standard Edition サーバーおよび フロント エンド サーバーに既定でインストールされます。

## 発信ルーティング コンポーネント

発信ルーティング コンポーネントは、発信通話を通話先の PBX または PSTN にルーティングします。発信者に、ユーザーの音声ポリシーに定義された通話の承認ルールが適用され、それぞれの発信のルーティングに対して最適な PSTN ゲートウェイが決定されます。発信ルーティング コンポーネントは、すべての Standard Edition サーバーおよび フロント エンド サーバーに既定でインストールされます。

発信ルーティング コンポーネントで使用されるルーティング ロジックは、主にネットワーク管理者またはテレフォニー管理者が組織の要件に従って構成します。

## Exchange UM ルーティング コンポーネント

Exchange UM ルーティング コンポーネントは、Lync Server と Exchange ユニファイド メッセージング (UM) を実行しているサーバーとの間のルーティングを処理します。これにより、Lync Server とユニファイド メッセージングの機能が統合されます。

Exchange UM ルーティング コンポーネントはまた、Exchange UM サーバーが利用できない時の PSTN を介したボイス メールの再ルーティングも処理します。エンタープライズ VoIP ユーザーが、セントラル サイトにつながる回復力のある WAN リンクを持たないブランチ サイトにいる場合、ブランチ サイトで展開する 存続可能ブランチ アプライアンスが、WAN が停止している間ブランチ サイトのユーザーにボイス メールのサバイバビリティ機能を提供します。WAN リンクが利用できない場合、存続可能ブランチ アプライアンスは次の作業を行います。

  - セントラル サイトの Exchange ユニファイド メッセージング サーバーに、PSTN を介して不在時の着信を再ルーティングします。

  - ユーザーが PSTN を介してボイス メール メッセージを取得できるようにします。

  - 不在着信通知をキューに入れ、WAN リンクが回復した時に Exchange UM サーバーへそれらをアップロードします。

ボイス メールの再ルーティングを有効にするには、Exchange 管理者は Exchange UM 自動応答 (AA) がメッセージのみを受け入れるよう構成することを推奨します。

これらの機能の詳細については、「[Lync Server 2013 での Exchange ユニファイド メッセージング統合の計画](lync-server-2013-planning-for-exchange-unified-messaging-integration.md)」および「[Lync Server 2013 でのエンタープライズ VoIP の復旧の計画](lync-server-2013-planning-for-enterprise-voice-resiliency.md)」を参照してください。

## 内部クラスター ルーティング コンポーネント

内部クラスター ルーティング コンポーネントは、通話を呼び出し先のプライマリ レジストラー プールにルーティングします。 それが不可能な場合、コンポーネントは、通話を呼び出し先のバックアップ レジストラー プールにルーティングします。 呼び出し先のプライマリ レジストラー プールおよびバックアップ レジストラー プールが IP ネットワークを介して到達不能の場合、内部クラスター ルーティング コンポーネントは PSTN を介して通話をユーザーの電話番号へ再ルーティングします。

## VoIP に必要なその他のフロントエンド サーバー コンポーネント

フロント エンド サーバーまたは ディレクターに存在するその他のコンポーネントは次のとおりです。これらは、VoIP コンポーネントそのものではありませんが、VoIP に不可欠なサポートを提供します。

  - **ユーザー サービス。**各着信通話の通話先電話番号に対して逆引き番号検索を実行し、その電話番号を通話先ユーザーの SIP URI と照合します。この情報を使用して、着信ルーティング コンポーネントはユーザーの登録 SIP エンドポイントに通話を分散します。ユーザー サービスは、すべての フロント エンド サーバーおよび ディレクターの主要なコンポーネントです。

  - **ユーザー レプリケーター。**Active Directory ドメイン サービス からユーザーの電話番号を抽出し、ユーザー サービスおよびアドレス帳サーバーから利用できる、RTC データベースのテーブルにその番号を書き込みます。ユーザー レプリケーターは、すべてのフロント エンド サーバーの主要なコンポーネントです。

  - **アドレス帳サーバー。**Active Directory ドメイン サービス のグローバル アドレス一覧情報を Lync Server クライアントに提供します。また、RTC データベースからユーザーおよび連絡先の情報を取得してアドレス帳ファイルに書き込み、Lync クライアントによってダウンロードされたそのファイルを共有フォルダーに格納します。アドレス帳サーバーでは情報を RTCAb データベースに書き込みます。このデータベースは、Microsoft Lync 2010 Mobile からのユーザーの検索クエリに応答するためにアドレス帳 Web クエリ サービスで使用されます。RTC データベースに書き込まれたエンタープライズ ユーザーの電話番号は、Lync にユーザーの連絡先をプロビジョニングするために、必要に応じて正規化されます。アドレス帳サービスは、すべてのフロント エンド サーバーに既定でインストールされます。アドレス帳 Web クエリ サービスは、各フロント エンド サーバーで Web サービスと共に既定でインストールされます。

