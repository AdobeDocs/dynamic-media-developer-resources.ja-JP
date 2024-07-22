---
description: プラス記号の付いたオーバーセットテキストフレームを表示します。 テキストオーバーフローインジケーターは、テキストフレーム（連結テキストの場合は最後のテキストフレーム）でテキストが割り当てられたスペースを超えた場合に表示します。 インジケーターは、プラス記号が付いた赤いボックスです。
solution: Experience Manager
title: markOverflowingTextFrames
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1e2a3d4-ef1f-4d5e-be9c-eeec36f46603
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---

# markOverflowingTextFrames{#markoverflowingtextframes}

プラス記号の付いたオーバーセットテキストフレームを表示します。 テキストオーバーフローインジケーターは、テキストフレーム（連結テキストの場合は最後のテキストフレーム）でテキストが割り当てられたスペースを超えた場合に表示します。 インジケーターは、プラス記号が付いた赤いボックスです。

<table id="simpletable_F17FD29EB52043BF9000923ED5195A26"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">&amp;markOverflowingTextFrames</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

修飾子 `markOverflowingTextFrames=1` を URL 呼び出しで設定すると、テキストが上書きされるすべてのテキストフレームにプラス記号が付きます。 また、Dynamic Media Classic プレビューアでは、テキストオーバーセットインジケーターはデフォルトで「`TRUE`」に設定されています。

初期設定は 0。
