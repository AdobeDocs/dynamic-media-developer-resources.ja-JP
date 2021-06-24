---
description: FXGの最適化を有効にします。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXGの最適化を有効にします。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

このFXGを渡す際に、FXGで表示がfalseに設定されている要素を削除し、FXGの処理時間を短縮します。 ただし、FXGの他の要素に影響を与えない、可視性がfalseの要素のみを削除します。 例えば、`Path`にテキストが存在し、`Path`の表示がfalseに設定されている場合、このパスにテキストを描画する必要があるので、この修飾子を有効にしてもFXGからは削除されません。

初期設定は 1 です
