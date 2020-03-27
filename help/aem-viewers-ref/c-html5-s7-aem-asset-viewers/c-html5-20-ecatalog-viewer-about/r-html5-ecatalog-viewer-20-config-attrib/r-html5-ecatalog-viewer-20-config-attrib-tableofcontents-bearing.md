---
description: 'null'
seo-description: 'null'
seo-title: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic media
uuid: 791aaaa5-3777-4f68-a445-caa3d975d883
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> ドロップダウンパネルの外観の方向を制御します。 </p> <p>fit-verticalを設定すると <span class="codeph"></span>、コンポーネントはまずパネルの基本の位置をボタンの下部に移動し、基本の位置から右または左にパネルをロールアウトしようとします。 試行のたびに、外側のコンテナでパネルが切り取られているかどうかがチェックされます。 すべての試行が失敗した場合、パネルの基本の位置を上に移動し、右方向と左方向でロールアウト試行を繰り返します。 </p> <p>fit-lateralを設定すると <span class="codeph"></span>、コンポーネントは同じロジックを使用しますが、基本を最初に右に移動し、下方向および上方向のロールアウトを試します。 次に、ベースを左に移動し、下方向と上方向のロールアウトを試します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> ユーザーがアイドル状態のときにパネルを非表示にするドロップダウン自動非表示タイマーの遅延時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-55436ddd78b04f538dbb9a7a8463feae}

（オプション）

## 初期設定 {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## 例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
