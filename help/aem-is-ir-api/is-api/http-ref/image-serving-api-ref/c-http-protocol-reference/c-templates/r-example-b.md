---
description: 例Aと同様の要件ですが、背景色をべた塗りにし、コンポジットの高さを変えて、縦横比の異なる画像に合わせることができます。
seo-description: 例Aと同様の要件ですが、背景色をべた塗りにし、コンポジットの高さを変えて、縦横比の異なる画像に合わせることができます。
seo-title: 例B
solution: Experience Manager
title: 例B
topic: Scene7 Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 例B{#example-b}

例Aと同様の要件ですが、背景色をべた塗りにし、コンポジットの高さを変えて、縦横比の異なる画像に合わせることができます。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.50&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

画像がレイヤー0に配置され、の高さの値が0に設定されると、 `size=` 800ピクセル幅に拡大した後の実際の高さが画像の高さによって決まります。

`extend=` は、上下に100ピクセル、右に200ピクセルを追加します。

レイヤ0とレイヤ1の両方の原点は、合成領域の中央右に配置され、希望のテキスト位置になります。

次の図に、画像の縦横比とテキスト文字列の組み合わせを示します。

![](assets/exampleb.png)

