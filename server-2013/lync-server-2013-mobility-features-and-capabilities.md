﻿---
title: 'Lync Server 2013: モビリティの機能'
TOCTitle: モビリティの機能
ms:assetid: 12517a88-2531-44a5-bea5-d8884aff53eb
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Hh689983(v=OCS.15)
ms:contentKeyID: 48271318
ms.date: 12/10/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 のモビリティの機能

 

_**トピックの最終更新日:** 2016-12-08_

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

Lync Server 2013 の累積した更新プログラム: 2013 年 2 月で導入されたモビリティ機能では、Lync 2010 Mobile および Lync 2013 Mobile のクライアント機能がサポートされます。Lync Server 2013 Mobility Service を展開すると、ユーザーは、サポートされる Apple iOS、Android、および Windows Phone、または Nokia Symbian の各モバイル デバイスを使用して、インスタント メッセージの送受信、連絡先の表示、プレゼンスの表示など、各種作業を実行できます。また、クリックして会議に参加、勤務先から通話、同一番号接続、ボイス メール、不在着信など、モバイル デバイスでいくつかのエンタープライズ VoIP 機能がサポートされます。Lync Server 2013 の累積した更新プログラム: 2013 年 2 月で導入された新しい機能には、会議出席者のためのボイス オーバー IP (VoIP) 機能とビデオ (H.264) が含まれます。

Lync Server 2013 の累積した更新プログラム: 2013 年 2 月で導入されたモビリティ機能では、Lync 2013 Mobile のクライアント機能がサポートされます。Lync Server 2013 の累積した更新プログラム: 2013 年 2 月では統合コミュニケーション Web API (UCWA) がインストールされます。UCWA は、Lync 2013 Mobile のクライアントで使用されるコンポーネントです。Lync Server 2013 では、Lync 2010 Mobile クライアント用に Mcx が使用されます。Lync Server 2013 の累積した更新プログラム: 2013 年 2 月では、モビリティ サービスの新しいエントリ ポイントとして UCWA が導入されます。Lync Server 2013 は、Lync Server 2010 の累積した更新プログラム: 2011 年 11 月で導入された Mobility Service (Mcx) を同時に実装し、Lync 2010 Mobile をサポートします。Lync Server 2013 の累積した更新プログラム: 2013 年 2 月を展開すると、ユーザーはサポートされる Apple iOS、Android、および Windows Phone の各モバイル デバイスを使用して以下の作業を実行できます。


> [!IMPORTANT]
> Lync Server 2010 の累積した更新プログラム: 2011 年 11 月の Mobility Service でサポートされる機能には (Mcx) の印が付けられています。示されているすべての機能は、Lync Server 2013 の累積した更新プログラム: 2013 年 2 月で導入された UCWA でサポートされます。



  - インスタント メッセージの送受信 (Mcx)

  - プレゼンスの表示 (Mcx)

  - 連絡先の表示 (Mcx)

  - クリックして会議に参加 (Mcx)

  - 勤務先から通話 (Mcx)

  - 同一番号接続 (Mcx)

  - ボイス メール (Mcx)

  - 不在着信通知 (Mcx)

  - ボイス オーバー IP (VoIP)

  - 出席者のビデオ (H.264)

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lync 2010 Mobile では Nokia Symbian デバイス用のクライアントが提供されました。Lync 2013 Mobile に Nokia Symbian ベースのデバイス用のクライアントはありません。</td>
</tr>
</tbody>
</table>


Apple iPad ユーザーは強化機能を利用できるようになります。iPad ユーザーは、音声コールバックを使用して会議に参加した後、アップロードされた Microsoft PowerPoint プレゼンテーションを会議内で表示したり、アプリケーションとデスクトップを共有したり、会議の参加者リストを表示したり、会議内で共有するその他のコンテンツ タイプの通知を受け取ったりできます。


> [!TIP]
> "同一番号接続" では、ユーザーは勤務先電話番号にダイヤルされた通話を携帯電話で受信します。"勤務先から通話" では、ユーザーは、携帯電話番号の代わりに勤務先電話番号を使用して、Lync Mobile クライアントから通話を発信します。"ダイヤルアウト" では、クライアントは、(Lync Mobile バージョンに基づいて) Mcx または UCWA に要求を送信して通話を発信します。サーバーは通話を開始した後、ユーザーの携帯電話にコールバックします。ユーザーが応答すると、サーバーはもう一方の参加者にダイヤルすることで通話を完了します。"勤務先から電話" を使用すると、ユーザーは通話中に勤務先 ID を維持できます。つまり、発信者の携帯番号が呼び出し先に表示されません。また、発信者に発信通話料金がかかりません。



<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>すべてのモバイル デバイスですべての機能がまったく同じように動作するとは限りません。モバイル デバイスでサポートされる機能の詳細については、「モバイル クライアントの比較表」(<a href="http://go.microsoft.com/fwlink/?linkid=234777" class="uri">http://go.microsoft.com/fwlink/?linkid=234777</a>) を参照してください。サポートされるデバイスとオペレーティング システムの詳細については、「<a href="lync-server-2013-planning-for-mobile-clients.md">Lync Server 2013 でのモバイル クライアントの計画</a>」で、要件に関するトピックを参照してください。</td>
</tr>
</tbody>
</table>


Lync Server 2013 の自動検出機能を使用すると、ユーザーが URL をデバイスの設定に手動で入力しなくても、モバイル アプリケーションで Lync Server 2013 Web サービスを自動的に検索できます。URL をモバイル デバイスの設定に手動で入力することも、主にトラブルシューティングの目的でサポートされます。


> [!IMPORTANT]
> Mcx と UCWA は無料のサービスであり、Lync 2010 Mobile と Lync 2013 Mobile のクライアントをサポートするにはこの 2 つを展開します。Lync 2013 Mobile は Lync Server 2010 展開にサインインできません。Lync 2010 Mobile と Lync 2013 Mobile は、Lync Server 2013 の累積した更新プログラム: 2013 年 2 月が適用された Lync Server 2013 展開を使用できます。



モビリティ機能では、バックグラウンドで実行されるアプリケーションをサポートしないモバイル デバイス用に*プッシュ通知*もサポートされます。プッシュ通知とは、モバイル アプリケーションが活動していない間に発生したイベントに関して、モバイル デバイスに送信される通知です。たとえば、不在着信したインスタント メッセージング (IM) への招待によってプッシュ通知を発生できます。

Mcx、UCWA、自動検出サービス、およびプッシュ通知のサポートは、Lync Server 2013 で提供されます。更新されたクライアント機能、およびモビリティのエントリ ポイントとしての UCWA の使用は、Lync Server 2013 の累積した更新プログラム: 2013 年 2 月で導入されます。
