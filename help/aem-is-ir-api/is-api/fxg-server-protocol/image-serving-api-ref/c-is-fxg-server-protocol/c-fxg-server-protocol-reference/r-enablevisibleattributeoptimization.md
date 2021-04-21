---
description: FXGの最適化を有効にします。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

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
