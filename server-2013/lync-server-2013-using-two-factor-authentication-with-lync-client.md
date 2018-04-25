﻿---
title: Lync クライアントでの 2 要素認証の使用
TOCTitle: Lync クライアントでの 2 要素認証の使用
ms:assetid: d4136e61-c3ab-4b26-85c8-c1b2c24f5ee3
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Dn338071(v=OCS.15)
ms:contentKeyID: 56270152
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync クライアントでの 2 要素認証の使用

 

_**トピックの最終更新日:** 2015-03-09_

このトピックでは、Lync 2013 クライアントで 2 要素認証を活用する方法について説明します。

## Lync 2013 に初めてサインインする

Lync 2013 をインストールすると、通常自動的に Lync のサインイン情報が構成されます。ただし、Lync を初めて使う場合は、手動でクライアントを起動する必要があります。

**Lync に初めてサインインするには、次の操作を行います。**

1.  組織のネットワークにログオンします。

2.  \[**スタート**\]、\[**すべてのプログラム**\]、\[**Microsoft Lync**\]、\[Lync 2013\] の順にクリックします。
    
    Lync のサインイン画面が表示されます。
    
      - \[サインイン アドレス\] ボックスが既に入力されている場合は、表示されているアドレスが正しいことを確認します。
    
      - 入力が正しくない、またはボックスが空の場合は、ユーザーの Lync のサインイン アドレスを入力します (通常はユーザーのメール アドレスです)。
    
      - パスワードを入力するボックスが空の場合は、パスワードを追加します。

3.  \[**サインイン**\] を選びます。

## Lync からサインアウトする

Lync を使い終わったら、表示を閉じるか、セッションからサインアウトするか、プログラムを終了することができます (すべて \[ファイル\] メニューから実行できます)。次の表で、オプションの違いについて説明します。


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>オプション</th>
<th>機能</th>
<th>実行する方法</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>閉じる</p></td>
<td><p>Lync の表示は閉じられますが、ユーザー ID で識別されている Lync セッションは引き続き実行されます。したがって、引き続き通知を受け取り、他のユーザーと対話できます。</p>
<p>タスク バーまたは画面の一番下にある通知領域の Lync アイコンをクリックすれば、いつでも表示を元に戻すことができます。</p></td>
<td><p>Lync のメイン画面で、次のいずれかの操作を行います。</p>
<ol>
<li><p>[<strong>オプション</strong>] をクリックし、[<strong>ファイル</strong>] &gt; [<strong>閉じる</strong>] の順に選びます。</p></li>
<li><p>ウィンドウの右上隅にある [<strong>閉じる</strong>] ボタン (X) をクリックします。</p></li>
</ol></td>
</tr>
<tr class="even">
<td><p>サインアウトする</p></td>
<td><p>ユーザー ID に関連付けられている Lync セッションが終了しますが、Lync はバックグラウンドで引き続き実行されます。サインアウトすると、サインイン ウィンドウが表示されます。</p>
<div class="alert">

> [!TIP]
> [<STRONG>サインイン情報を削除</STRONG>] を選ぶと、サインアウトするときにコンピューターからログオン ID とパスワードの記録を削除できます。このようにすると、サポート担当者が行うサインインの問題のトラブルシューティングが容易になることがあります。また、権限のないユーザーがあなたの資格情報でログインすることは難しくなるため、サインイン情報のセキュリティも確保できます。


</div></td>
<td><p>Lync メイン ウィンドウで、[<strong>オプション</strong>] をクリックし、[<strong>ファイル</strong>] &gt; [<strong>サインアウト</strong>] の順に選びます。</p></td>
</tr>
<tr class="odd">
<td><p>終了する</p></td>
<td><p>Lync セッションが終了し、コンピューター上の Lync がシャットダウンされます。終了後、Lync を再起動する場合は、[<strong>スタート</strong>] &gt; [<strong>すべてのプログラム</strong>] &gt; [<strong>Microsoft Lync</strong>] &gt; [<strong>Lync 2013</strong>] の順に選びます。</p></td>
<td><p>Lync メイン ウィンドウで、[<strong>オプション</strong>] をクリックし、[<strong>ファイル</strong>] &gt; [<strong>終了</strong>] の順に選びます。</p></td>
</tr>
</tbody>
</table>


## スマート カードで Lync にサインインする

一部の組織では、Lync 2013 ユーザーのセキュリティを強化するために、2 要素認証と呼ばれる複数の手順によるサインイン プロセスを使っています。このオプションを使うには、「スマート カード」で Lync にサインインする必要があります。スマート カードには、物理カードと仮想カードの 2 種類があります。

  - **物理カード**   クレジット カードと同じくらいのサイズです。ログインするときにスマート カード リーダーに挿入します。

  - **仮想カード**   実体のあるカードではなく、ユーザーのコンピューターの特別なチップに書き込まれた電子 ID で、コンピューター内にスマート カードが構築されます。TPM (トラステッド プラットフォーム モジュール) チップ搭載の Windows 8 コンピューターでのみ使うことができます。

## スマート カードを登録する

スマート カードでサインインする前に、カードを「登録」する必要があります。これは、ユーザーの資格情報をカードに紐付けることを指します。ここで、物理カードか仮想カードかによって手順が変わります。このプロセスは、既に Lync Server 管理者によって行われている可能性があります。不明な場合は、管理者に確認してください。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>仮想スマート カードは、それがインストールされているデバイスのみに関連付けられるため、ユーザーが使う Windows 8 コンピューターごとに異なるカードを登録する必要があります。</td>
</tr>
</tbody>
</table>


**スマート カードを手動で登録するには、次の操作を行います。**

1.  Lync を実行しているコンピューターにログオンします。

2.  Internet Explorer を使って、組織の証明機関 Web 登録ページに移動します。
    
    まだ持っていない場合は、Lync Server 管理者にこのリソースの Web アドレスを確認します。URL は、https://MyCA.\[ユーザーの会社名\].com/certsrv のようになります。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Internet Explorer 10 を使っている場合は、この Web サイトを互換モードで見る必要がある場合があります。</td>
    </tr>
    </tbody>
    </table>


3.  証明書のページにログオンするよう求められた場合は、ユーザーのドメイン アカウントを使ってログオンします (コンピューターの管理者としてはログオンしません)。

4.  Web サイトのようこそページで、\[**証明書の要求**\] を選びます。

5.  \[**証明書の要求の詳細設定**\] を選びます。

6.  \[**この CA への要求を作成し送信する。**\] を選んで、\[**次へ**\] をクリックします。

7.  「スマート カードの登録ステーション」というページが表示されます。要求を承認して ActiveX コントロールをインストールし、\[証明書の要求の詳細設定\] を次のように入力します。
    
    1.  \[**証明書のテンプレート**\] ドロップダウン リストから \[**スマート カード ユーザー**\] を選びます。
    
    2.  \[**新しいキー セットを作成する**\] を選びます。
    
    3.  スマート カードのラベルから製造元情報を確認し、\[**CSP**\] ドロップダウン リストから製造元を選びます。
    
    4.  まだ選んでいない場合は、要求の形式として \[**CSP**\] を選びます。
    
    5.  まだ選んでいない場合は、\[ハッシュ アルゴリズム\] ドロップダウン リストから \[**sha1**\] を選びます。
    
    6.  証明書に分かりやすい名前を付けて、\[**送信**\] をクリックします。

8.  登録ステーションに接続したカード リーダーに空のスマート カードを挿入し、\[**登録**\] をクリックします。

9.  要求メッセージが表示されたら、暗証番号 (PIN) を入力し、\[**OK**\] をクリックします。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>スマート カードを登録するために使う特別な PIN をテクニカル サポート担当者から受け取っていない場合は、既定のスマート カード PIN の値である 12345678 を使用します。</td>
    </tr>
    </tbody>
    </table>


10. スマート カードを最初に使うときに PIN の変更をユーザーに強制するオプションを選択します。

11. 登録ステーションに接続したカード リーダーに空のスマート カードを挿入し、\[**登録**\] をクリックします。

12. 要求メッセージが表示されたら、暗証番号 (PIN) を入力し、\[**OK**\] をクリックします。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>スマート カードを登録するために使う特別な PIN をテクニカル サポート担当者から受け取っていない場合は、既定のスマート カード PIN の値である 12345678 を使用します。</td>
    </tr>
    </tbody>
    </table>


13. スマート カードを最初に使うときに PIN の変更をユーザーに強制するオプションを選択します。

14. 表示された証明書に記載されたユーザーの情報を確認したら、\[**OK**\] をクリックします。

15. 証明書が発行されたことを知らせる通知を確認したら、\[**この証明書のインストール**\] をクリックして登録プロセスを完了します。

## 自分のスマート カードの資格情報で Lync にサインインする

初めてスマート カードを使う前に、Lync のサインイン ページで \[**サインイン情報を削除**\] をクリックすることをお勧めします。これにより、コンピューターに保存されているすべてのサインイン情報がクリアされ、エラーの原因を取り除くことができます。

**自分のスマート カードの資格情報で Lync にサインインするには、次の操作を行います。**

1.  Lync クライアントを起動します。

2.  サインイン画面で、ユーザーのアカウント名を \[**サインイン アドレス**\] ボックスに入力し、\[**サインイン**\] をクリックします。

3.  仮想スマート カードを使っている場合は、この手順は省略します。
    
    物理スマート カードを使っている場合は、メッセージが表示されたらスマート カードをスマート カード リーダーに挿入し、カードが認識されたら \[**OK**\] をクリックします。

4.  スマート カードの PIN 番号を入力し、\[**OK**\] をクリックします。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>サポート担当者からスマート カードの PIN 番号が割り当てられなかった場合は、既定の値 (12345678) を入力します。</td>
    </tr>
    </tbody>
    </table>
