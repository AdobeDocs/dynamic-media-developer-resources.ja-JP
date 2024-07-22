---
description: FXG の最適化を有効にします。
solution: Experience Manager
title: enableVisibleAttributeOptimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# enableVisibleAttributeOptimization{#enablevisibleattributeoptimization}

FXG の最適化を有効にします。

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">&amp;enableVisibleAttributeOptimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

FXG で可視性が false に設定されている要素を削除し、この FXG を渡します。これにより、FXG の処理時間が短縮されます。 ただし、FXG 内の他の要素には影響を与えない、可視性が false の要素のみを削除します。 たとえば、`Path` に文字があり、`Path` の表示が false に設定されている場合、このモディファイヤを有効にしても FXG から削除されません。これは、文字をこのパスに描画する必要があるためです。

初期設定は 1。
