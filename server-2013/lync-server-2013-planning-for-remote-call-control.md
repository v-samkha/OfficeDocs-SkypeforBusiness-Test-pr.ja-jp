﻿---
title: 'Lync Server 2013: リモート通話コントロールの計画'
TOCTitle: リモート通話コントロールの計画
ms:assetid: 688a0328-1aa7-449f-b5f7-98c876112ed2
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg558658(v=OCS.15)
ms:contentKeyID: 48272377
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 リモート通話コントロールの計画

 

_**トピックの最終更新日:** 2012-09-05_

Lync Server 2013 では、リモート通話コントロールに対するサポートにより、構内交換機 (PBX) 電話をデスクトップ コンピューターの Lync 2013 を使用して制御できます。このセクションでは、リモート通話コントロール機能およびリモート通話コントロールを展開するための要件について説明します。

PBX および Lync Server 2013 間の統合により、リモート通話コントロールに対して有効化されているユーザーは、Lync 2013 ユーザー インターフェイス (UI) を使用して、次のような方法で PBX 電話の通話を制御できます。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>最終的には、ユーザーの PBX 電話をホストする PBX の機能が、そのユーザーが利用することができるリモート通話コントロールの機能を決定します。</td>
</tr>
</tbody>
</table>


  - 通話を発信する

  - 着信通話に応答する

  - インスタント メッセージで着信した通話に応答する
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>つまり、発信者の電話番号が、組織内のグローバル アドレス一覧 (GAL) の、呼び出し先の Lync 連絡先リストの、またはフェデレーション パートナー組織の、インスタント メッセージ アドレスに関連付けられる場合です。</td>
    </tr>
    </tbody>
    </table>


  - 通話の転送

  - 着信の転送

  - 通話の保留

  - 複数の同時通話間の切り替え

  - 既に通話中である時に 2 番目の通話に応答する (つまり、通話中の着信)

  - デュアルトーン多重周波数 (DTMF) 電話番号をダイヤルする

  - \[会話\] ウィンドウで、Microsoft Office OneNote メモ プログラムにメモを入力する

さらに、ユーザーがリモート通話コントロールに対して有効化されている場合、Lync 2013 は次の通話情報をユーザーに提供します。

  - 発信者の電話番号が、リモート通話コントロールが有効になっているユーザーの Microsoft Office Outlook メッセージおよびグループ作業クライアントの連絡先リスト、Lync の連絡先リスト、または組織の GAL に存在する場合は、名前による発信者の ID。

  - Outlook の \[会話履歴\] フォルダーに保存されている、過去の着信および発信通話。

  - ユーザーの Outlook 受信トレイ フォルダーに送信される不在着信通知 (ただし、通話の受信時に Lync が実行されている場合のみ生成されます)。

## リモート通話コントロールとエンタープライズ VoIP

リモート通話コントロール機能は エンタープライズ VoIP 機能から分離しており、ユーザーを両方に対して有効化することはできませんが、エンタープライズ VoIP は、リモート通話コントロールに対して有効化されているユーザーも利用可能な機能のサブセットを提供します。エンタープライズ VoIP が展開されると、リモート通話コントロールに対して有効化されているユーザーは、Lync を使用して次の エンタープライズ VoIP 機能にアクセスできます。

  - 別の Lync クライアントに対する通話の発信および受信

  - エンタープライズ VoIP に対して有効化されているユーザーによって作成された会議の音声部分への参加

## このセクション中

  - [Lync Server 2013 のリモート通話コントロールの展開タスク](lync-server-2013-deployment-tasks-for-remote-call-control.md)
