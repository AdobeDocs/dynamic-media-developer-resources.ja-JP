---
description: 例Aと同様の要件ですが、背景にべた塗りを使用し、コンポジットの高さを変えて、縦横比の異なる画像に対応できます。
solution: Experience Manager
title: 例B
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# 例B{#example-b}

例Aと同様の要件ですが、背景にべた塗りを使用し、コンポジットの高さを変えて、縦横比の異なる画像に対応できます。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,5,50&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

画像がレイヤー0に配置され、`size=`の高さの値が0に設定されている場合、幅800ピクセルに拡大縮小した後、画像の高さによって実際の高さが決まります。

`extend=` 上下100ピクセル、右下200ピクセルを追加します。

レイヤ0とレイヤ1の原点は、合成領域の中央右に配置され、希望のテキスト位置になります。

次の図は、画像の縦横比が異なり、テキスト文字列が異なる複合結果を示しています。

![](assets/exampleb.png)
