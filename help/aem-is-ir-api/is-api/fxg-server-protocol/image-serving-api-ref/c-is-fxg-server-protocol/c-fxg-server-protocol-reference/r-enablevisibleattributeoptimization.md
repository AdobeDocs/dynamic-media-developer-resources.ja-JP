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
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---


# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXGの最適化を有効にします。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> enableVisibleAttributeOptimization(&amp;enableVisibleAttributeOptimization)</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

FXGで表示がfalseに設定されている要素を削除し、このFXGを渡すとFXGの処理時間が短くなります。 表示がfalseの要素のみが削除されますが、FXGの他の要素には影響しません。 例えば、`Path`にテキストがあり、`Path`の表示/非表示がfalseに設定されている場合、この修飾子が有効になっていても、FXGからは削除されません。これは、このパスにテキストを描画する必要があるためです。

初期設定は 1 です
