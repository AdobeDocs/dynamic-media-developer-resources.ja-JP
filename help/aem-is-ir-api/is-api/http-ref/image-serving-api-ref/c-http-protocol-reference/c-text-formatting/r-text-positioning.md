---
description: text=レンダラーは、事前サイズのレイヤーに適用する場合（size=が指定されている場合も同様）、textPs=レンダラーとは根本的に異なるテキストを配置します。
solution: Experience Manager
title: テキストの配置
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# テキストの配置{#text-positioning}

text=レンダラーは、事前サイズのレイヤーに適用する場合（size=が指定されている場合も同様）、textPs=レンダラーとは根本的に異なるテキストを配置します。

セルフサイズの`text=`と`textPs=`のレイヤーの外観と位置は同じです。

`textPs=` 文字セルの上部をテキストボックスの上部に揃えます( `\vertalt`と仮定)。この結果、レンダリングされたテキストグリフの一部がテキストボックスの境界の一部外に広がる場合でも同様です。特定のフォントのレンダリングされたグリフが、テキストボックスの左右端を少し越えて突出する場合もあります。 レイヤーの長方形内にすべてのレンダリングテキストを含める必要があるアプリケーションの場合は、RTF `\marg*`コマンドまたは`textFlowPath=`を使用して、テキストレンダリング領域を調整できます。

これに対し、`text=`は、必要に応じてレンダリングされたテキストをシフトし、レンダリングされたすべてのグリフが指定のテキストボックス内に完全に収まるように保証します。

`text=`は、単純なアプリケーションでは少し使いやすい場合がありますが、`textPs=`は、フォント面やテキスト効果に関係なく、正確な位置を指定できます。

## 例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

次に、事前サイズのテキストの例を示します。 テキストのサイズ変更の動作が異なります。

** `Text=`は常に上部に狭い余白を提供します。**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=`は、テキストをテキストボックスの上部に合わせてきつく配置します。Arial:**などの一般的なフォントでも、テキストがわずかに切り詰められる場合があります。

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=`は、レンダリングされたテキストを自動的に下にシフトして、クリッピングを避けます。**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=`は、浮き出た部分を含むテキストを移動しないので、テキストがレイヤー0上にある場合は大幅に切り抜かれます**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**上部の10 pt(200 twip)の余白は、このテキストをクリッピングなしでレンダリングします。**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定のスクリプトフォントのレンダリングされたグリフが、テキストボックスの外側に大幅に拡張する場合があります。**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
