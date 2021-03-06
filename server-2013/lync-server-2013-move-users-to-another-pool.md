﻿---
title: 別のプールへのユーザーの移動
TOCTitle: 別のプールへのユーザーの移動
ms:assetid: e7b4968c-0e9d-4d56-b5f1-9edf0f7206f8
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg182600(v=OCS.15)
ms:contentKeyID: 48274011
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 別のプールへのユーザーの移動

 

_**トピックの最終更新日:** 2013-03-11_

Lync Server コントロール パネルを使用して、ユーザーを特定のサーバーまたはプールに割り当てることができます。


> [!TIP]
> Microsoft Office Communications Server 2007 R2 またはそれ以前のバージョンを実行しているソース プールから、複合 Active Directory 環境の Lync Server 2013 のターゲット プールにすべての既存ユーザーを移動すると、Active Directory のレプリケーション速度が遅くなることがあります。この状態を回避するため、検索フィルターを使用して、Microsoft Office Communications Server 2007 R2 またはそれ以前のバージョンを実行しているプールからユーザーを別々に移動するか、Lync Server 管理シェルを使用して、コマンドレットによってユーザーを移動できます。また、フィルター機能は Lync Server 2013 ユーザーにも使用できます。



## 選択したユーザーを別のサーバーまたはプールに移動するには

1.  CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザー ウィンドウを開いて管理 URL を入力し、Lync Server コントロール パネルを開きます。Lync Server コントロール パネルを開くために使用できる他の方法の詳細については、「[Lync Server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」を参照してください。

3.  左側のナビゲーション バーで \[**ユーザー**\] をクリックします。

4.  \[**ユーザーの検索**\] ボックスに、検索するユーザー アカウントの表示名、名、姓、セキュリティ アカウント マネージャー (SAM) のアカウント名、SIP アドレス、または回線 URI (Uniform Resource Identifier) の全部または最初の一部を入力して、\[**検索**\] をクリックします。

5.  表の一覧で、特定のユーザーまたは複数のユーザーを選択します。

6.  \[**アクション**\] メニューの \[**選択したユーザーをプールに移動する**\] をクリックします。

7.  \[**ユーザーの移動**\] の \[**移動先レジストラ プール**\] で、ユーザーの移動先のプールを選択します。

8.  (オプション) 移動先のサーバーまたはプールを使用できない場合は、\[**強制移動**\] チェック ボックスをオンにします。
    

    > [!WARNING]
    > [<STRONG>強制</STRONG>] を選択すると、ユーザー アカウントは移動しますが、関連付けられているユーザー データ (ユーザーが予約した会議など) がすべて削除されます。選択しない場合は、アカウントも関連付けられているデータも移動します。



## サーバー間またはプール間ですべてのユーザーを移動するには

1.  CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザー ウィンドウを開いて管理 URL を入力し、Lync Server コントロール パネルを開きます。Lync Server コントロール パネルを開くために使用できる他の方法の詳細については、「[Lync Server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」を参照してください。

3.  左側のナビゲーション バーで \[**ユーザー**\] をクリックします。

4.  \[**アクション**\] メニューの \[**すべてのユーザーをプールに移動する**\] をクリックします。

5.  \[**ユーザーの移動**\] の \[**移動元レジストラ プール**\] で、移動するユーザー アカウントが入っているプールを選択します。

6.  \[**移動先レジストラ プール**\] で、ユーザーの移動先のプールを選択します。

7.  (オプション) 移動先のサーバーまたはプールを使用できない場合は、\[**強制移動**\] チェック ボックスをオンにします。
    

    > [!WARNING]
    > [<STRONG>強制</STRONG>] を選択すると、ユーザー アカウントは移動しますが、関連付けられているユーザー データ (ユーザーが予約した会議など) がすべて削除されます。選択しない場合は、アカウントも関連付けられているデータも移動します。



## フィルターを使用してユーザーをプール間で移動するには

1.  CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  ブラウザー ウィンドウを開いて管理 URL を入力し、Lync Server コントロール パネルを開きます。Lync Server コントロール パネルを開くために使用できる他の方法の詳細については、「[Lync Server 2013 管理ツールを開く](lync-server-2013-open-lync-server-administrative-tools.md)」を参照してください。

3.  左側のナビゲーション バーで \[**ユーザー**\] をクリックします。

4.  \[**ユーザー検索**\] で、\[**検索**\] をクリックし、\[**フィルターの追加**\] をクリックします。

5.  検索条件で \[**レジストラー プール**\] を選択し、\[**が次の値に等しい**\] を選択して、\[**現在のプールの FQDN**\] を選択し、\[**検索**\] をクリックします。

6.  \[**アクション**\] メニューの \[**すべてのユーザーをプールに移動**\] をクリックします。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>既存のユーザー セットに対してフィルターを適用すると、オプション [<strong>すべてのユーザーをプールに移動</strong>] は、可能性のあるユーザーすべてではなく、フィルターされたユーザーのサブセットのコンテキストとなります 。</td>
    </tr>
    </tbody>
    </table>


7.  \[**ユーザーの移動**\] の \[**移動元レジストラー プール**\] で、移動するユーザー アカウントが入っているプールを選択します。

8.  \[**移動先レジストラー プール**\] で、ユーザーの移動先のプールを選択します。

9.  (オプション) 移動先のサーバーまたはプールを使用できない場合は、\[**強制**\] チェック ボックスをオンにします。
    

    > [!WARNING]
    > [<STRONG>強制</STRONG>] を選択すると、ユーザー アカウントは移動しますが、関連付けられているユーザー データ (ユーザーが予約した会議、連絡先など) がすべて削除されます。選択しない場合は、アカウントも関連付けられているデータも移動します。



## Lync 管理シェルを使用してユーザーをプール間で移動するには

1.  Windows PowerShell コマンドの実行方法 (ローカルまたはリモートのどちらで実行するか) に応じて、正しい Lync Server 2013 管理者ロールのメンバーとして次のようにログオンする必要があります。
    
    1.  コマンドをローカル コンピューターで実行する場合 (たとえば、フロント エンド サーバーに直接ログオンする場合): Lync Server 管理シェルがインストールされているコンピューターに、RTCUniversalServerAdmins グループのメンバーとして、または「[Lync Server 2013 でのセットアップのアクセス許可の委任](lync-server-2013-delegate-setup-permissions.md)」に説明されている必要なユーザー権限を使用してログオンします。
    
    2.  コマンドを別のコンピューターでリモートで実行する場合 (たとえば、自分のコンピューターにログオンし、コマンドを Standard Edition のフロント エンド サーバーでリモートで実行する場合): CsUserAdministrator または CsAdministrator の役割に割り当てられているユーザー アカウントから、内部展開の任意のコンピューターにログオンします。

2.  Lync Server 管理シェルを以下の手順で起動します。\[**スタート**\]、\[**すべてのプログラム**\]、\[**Microsoft Lync Server 2013**\]、\[**Lync Server 管理シェル**\] の順にクリックします。

3.  単一のユーザーを移動するには、Move-CsUser コマンドレットを次のように使用します。
    
        Move-CsUser -Identity "Pilar Ackerman" -Target "pool01.contoso.net"
    
    この場合、移動するユーザーは Pilar Ackerman で、現在割り当てられているホーム プールから、プール pool01.contoso.net に移動します。

4.  大量のユーザーを移動するには、フィルターと **Get-CsUser** コマンドレットを使用し、ユーザーの結果セットを **Move-CsUser** に渡します。
    
        Get-CsUser -Filter {RegistrarPool -eq "CurrentPoolFqdn"} | Move-CsUser -Target "TargetPoolFQDN"
    
    **Get-CsUser** と **Move-CsUser** を組み合わせたコマンドを実行すると、たとえば、次のような結果が得られます。
    
        Get-CsUser -Filter {RegistrarPool -eq "pool02.contoso.net"} | Move-CsUser -Target "pool01.contoso.net"

## 関連項目

#### その他のリソース

[ユーザー アカウント プロパティの変更](lync-server-2013-modifying-user-account-properties.md)

