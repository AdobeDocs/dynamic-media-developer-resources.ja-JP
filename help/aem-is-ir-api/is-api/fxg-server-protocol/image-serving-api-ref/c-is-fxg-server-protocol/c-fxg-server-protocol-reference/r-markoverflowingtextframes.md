---
description: オーバーセットテキストフレームをプラス記号で表示します。 テキストオーバーフローインジケータは、テキストフレーム（スレッドテキストの場合は最後のテキストフレーム）で割り当てられているスペースをテキストが超過した場合に表示されます。インジケータはプラス記号が入った赤いボックスとして表示されます。
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 60%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

オーバーセットテキストフレームをプラス記号で表示します。 テキストオーバーフローインジケータは、テキストフレーム（スレッドテキストの場合は最後のテキストフレーム）で割り当てられているスペースをテキストが超過した場合に表示されます。インジケータはプラス記号が入った赤いボックスとして表示されます。

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

URL呼び出しを通じて修飾子`markOverflowingTextFrames=1`を設定すると、テキストがオーバーセットされるすべてのテキストフレームがプラス記号でマークされます。 また、Dynamic Media Classicのプリビューアでは、テキストのオーバーセットインジケーターはデフォルトで「`TRUE`」に設定されています。

初期設定は 0 です
