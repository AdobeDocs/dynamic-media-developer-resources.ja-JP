---
description: 例Aと同様ですが、背景色はべた塗りで、縦横比の異なる画像に合わせてコンポジットの高さを変えることができます。
solution: Experience Manager
title: 例B
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# 例B{#example-b}

例Aと同様ですが、背景色はべた塗りで、縦横比の異なる画像に合わせてコンポジットの高さを変えることができます。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

画像はレイヤー0に配置され、`size=`の高さの値は0に設定されます。これにより、800ピクセルの幅に拡大縮小した後、実際の高さは画像の高さによって決まります。

`extend=` は、上下に100ピクセル、右に200ピクセルを追加します。

レイヤ0とレイヤ1の両方の接触チャネルは、合成領域の中央右に配置され、希望のテキスト位置になります。

次の図に、画像の縦横比とテキスト文字列の組み合わせ結果を示します。

![](assets/exampleb.png)

