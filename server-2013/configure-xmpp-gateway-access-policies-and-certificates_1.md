﻿---
title: XMPP ゲートウェイ アクセス ポリシーおよび証明書の構成
TOCTitle: XMPP ゲートウェイ アクセス ポリシーおよび証明書の構成
ms:assetid: cd91433e-6dfb-4553-8316-c1086b394221
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ721885(v=OCS.15)
ms:contentKeyID: 49887156
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# XMPP ゲートウェイ アクセス ポリシーおよび証明書の構成

 

_**トピックの最終更新日:** 2012-10-15_

XMPP フェデレーションは、XMPP (eXtensible Messaging and Presence Protocol) に基づく外部展開を定義します。XMPP を構成すると、Lync ユーザーは XMPP ドメイン ユーザーに次の方法でアクセスできます。

  - IM とプレゼンス - 1 対 1 のみ

  - XMPP フェデレーションからの連絡先を Lync クライアントに作成

XMPP (eXtensible Messaging and Presence Protocol) フェデレーション パートナーをサポートするためにポリシーを構成する場合、ポリシーは XMPP フェデレーション ドメインのユーザーには適用されますが、セッション開始プロトコル (SIP) インスタント メッセージング (IM) サービス プロバイダー (たとえば、Windows Live)、または SIP フェデレーション ドメインのユーザーには適用されません。XMPP フェデレーション パートナーは、ユーザーが連絡先を追加して通信することを許可する XMPP フェデレーション ドメインごとに構成します。ポリシーを設定した後、XMPP ゲートウェイ証明書を構成する必要があります。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>XMPP ゲートウェイの移行を開始するには、 Lync Server 2013 XMPP ゲートウェイを展開して、 Lync Server 2013 XMPP ゲートウェイでユーザーを有効にするためにアクセス ポリシーを構成する必要があります。これらの手順を行う前に、すべてのユーザーを Lync Server 2013 展開に移動する必要があります。詳細については、「 <a href="configure-xmpp-gateway-on-lync-server-2013_1.md">Lync Server 2013 での XMPP ゲートウェイの構成</a>」を参照してください。</td>
</tr>
</tbody>
</table>


## Lync Server 2013 XMPP ゲートウェイでユーザーを有効にするために外部アクセス ポリシーを構成する

1.  Lync Server コントロール パネルを開きます。

2.  左側のナビゲーション バーで \[ **フェデレーションおよび外部アクセス** \] をクリックし、\[ **外部アクセス ポリシー** \] をクリックします。

3.  \[ **新規** \] をクリックし、\[ **ユーザー ポリシー** \] をクリックします。

4.  外部アクセス ユーザー ポリシー用に名前を入力します。

5.  外部アクセス ユーザー ポリシー用に説明を提供します。

6.  \[ **フェデレーション ユーザーとの通信を有効にする** \] を選択します。

7.  \[ **XMPP フェデレーション ユーザーとの通信を有効にする** \] を選択します。

8.  \[ **確定** \] をクリックして、サイトまたはユーザー ポリシーへの変更を保存します。
