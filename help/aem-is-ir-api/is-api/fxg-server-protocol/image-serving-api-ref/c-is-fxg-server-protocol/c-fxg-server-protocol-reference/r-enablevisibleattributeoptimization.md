---
description: FXGの最適化を有効にします。
seo-description: FXGの最適化を有効にします。
seo-title: enableVisibleAttributeOptimization
solution: Experience Manager
title: enableVisibleAttributeOptimization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXGの最適化を有効にします。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;E)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

FXGで表示がfalseに設定されている要素を削除し、このFXGを渡すと、FXGの処理時間が短くなります。 FXG内の他の要素に影響を与えない可視性がfalseの要素のみが削除されます。 例えば、テキストが存在し、の表示がfalseに設定さ `Path``Path` れている場合、この修飾子が有効になっていても、FXGからは削除されません。これは、このパスにテキストを描画する必要があるためです。

初期設定は 1 です
