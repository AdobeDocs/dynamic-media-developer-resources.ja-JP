---
description: 例Aと同様の要件ですが、単色の背景を使用し、縦横比が異なる画像に対応するために、コンポジットの高さを変更できます。
solution: Experience Manager
title: 例B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
TQID: 'https://experienceleague.adobe.com/nwRD9lmoHIjjFR32pdr0g6jRpsIIZicZXmVBXC74ot4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# 例B{#example-b}

例Aと同様の要件ですが、単色の背景を使用し、縦横比が異なる画像に対応するために、コンポジットの高さを変更できます。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> カタログ：:Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> カタログ：：修飾子</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

画像はレイヤー0に配置され、高さの値`size=`は0に設定されます。 この設定により、画像を幅800 ピクセルに拡大/縮小した後、実際の高さが画像の高さによって決まります。

変数`extend=`は、上下に100 ピクセル、右に200 ピクセルを追加します。

レイヤー0とレイヤー1の両方の原点は、合成領域の右中央に配置され、目的のテキスト位置になります。

次の画像は、画像の縦横比が異なり、テキスト文字列が異なる場合の合成結果を示しています。

![B画像の例](assets/exampleb.png)
