---
description: 例 A と同様の要件ですが、単色の背景を使用し、合成の高さを変化させて、縦横比の異なる画像に対応できます。
solution: Experience Manager
title: 例 B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# 例 B{#example-b}

例 A と同様の要件ですが、単色の背景を使用し、合成の高さを変化させて、縦横比の異なる画像に対応できます。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

イメージがレイヤ 0 に配置され、高さの値 `size=` が 0 に設定されます。 この設定では、画像の幅を 800 ピクセルに拡大/縮小した後、実際の高さが画像の高さによって決定されます。

変数 `extend=` は、上下に 100 ピクセル、右側に 200 ピクセルを追加します。

レイヤー 0 とレイヤー 1 の両方の原点が合成領域の右中央に配置され、目的のテキスト位置が得られます。

次の画像は、画像の異なる縦横比と異なるテキスト文字列の合成結果を示しています。

![&#x200B; 例 B 画像 &#x200B;](assets/exampleb.png)
