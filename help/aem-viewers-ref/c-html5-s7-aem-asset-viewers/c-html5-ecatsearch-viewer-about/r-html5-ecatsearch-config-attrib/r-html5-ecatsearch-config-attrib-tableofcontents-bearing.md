---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# TableOfContents.bearing{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> ドロップダウンパネルの外観の方向を制御します。 </p> <p><span class="codeph"> fit-vertical</span> に設定すると、コンポーネントは最初に基本パネルの位置をボタンの下部に移動し、基本パネルの位置から右または左にパネルをロールアウトしようとします。 試行のたびに、コンポーネントはパネルが外部コンテナによってクリップされているかどうかを確認します。 すべての試行が失敗した場合、コンポーネントはベースパネルの位置を上に移動しようと試み、ロールアウトの試行を右方向と左方向に繰り返します。 </p> <p>「フィット – ラテラル </span>」 <span class="codeph"> 設定した場合、コンポーネントは同様のロジックを使用しますが、最初にベースを右に移動し、ロールアウト方向を下に向けたり上に向けたりします。 次に、ベースを左に移動し、ロール アウト方向を上下に試します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> ユーザーがアイドル状態のときにパネルを非表示にするドロップダウン自動非表示タイマーの遅延を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-55436ddd78b04f538dbb9a7a8463feae}

オプション。

## 初期設定 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
