---
description: 例 A と同様の要件ですが、背景にべた塗りを使用し、縦横比の異なる画像に対応するために合成の高さを変えることができます。
solution: Experience Manager
title: 例 B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# 例 B{#example-b}

例 A と同様の要件ですが、背景にべた塗りを使用し、縦横比の異なる画像に対応するために合成の高さを変えることができます。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,50&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

画像はレイヤ 0 に配置され、`size=` の高さの値は 0 に設定されます。 この設定により、幅 800 ピクセルに拡大縮小した後、画像の高さによって実際の高さが決まります。

変数 `extend=` は、上下に 100 ピクセル、右に 200 ピクセルを追加します。

レイヤ 0 とレイヤ 1 の原点は、合成領域の中央右に配置され、希望のテキスト位置になります。

次の図は、画像の縦横比が異なり、テキスト文字列が異なる複合結果を示しています。

![B 画像の例](assets/exampleb.png)
