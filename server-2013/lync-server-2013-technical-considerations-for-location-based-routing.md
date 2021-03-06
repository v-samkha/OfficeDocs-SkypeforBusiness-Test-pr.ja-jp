﻿---
title: 'Lync Server 2013: 場所に基づくルーティングに関する技術的考慮事項'
TOCTitle: 場所に基づくルーティングに関する技術的考慮事項
ms:assetid: 2e2a9199-7c6f-48d3-9adb-3873fc4f8c4e
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ994027(v=OCS.15)
ms:contentKeyID: 52056566
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 場所に基づくルーティングに関する Lync Server 2013 の技術的考慮事項

 

_**トピックの最終更新日:** 2013-03-09_

場所に基づくルーティングを計画する場合、次のシナリオに対する影響を考慮する必要があります。

## 障害復旧

プライマリ プールからバックアップ プールへのフェールオーバー時およびプライマリ プールに対する通常の動作の回復時、障害と復旧の手続き中は常に、場所に基づくルーティングが適用されます。

## 存続可能ブランチ アプライアンス

場所に基づくルーティングを構成すると、存続可能ブランチ アプライアンスに関連したゲートウェイをどこに展開するかの計画に影響します。SBA に関連したゲートウェイは、存続可能ブランチ アプライアンスと同じネットワーク サイト内に配置されている必要があります。そうしないと、場所に基づくルーティングが構成されている場合、存続可能ブランチ アプライアンスに属しているユーザーは発信通話ができません。 存続可能ブランチ アプライアンスと特定のサイト間の WAN 接続がダウンした場合、場所に基づくルーティングの制約は引き続き適用されます。

## 関連項目

#### その他のリソース

[Lync Server 2013 での場所に基づくルーティングの計画](lync-server-2013-planning-for-location-based-routing.md)

