---
description: text=レンダラーは、テキストを事前にサイズが設定されたレイヤーに適用した場合（size=が指定されている場合も含む）、textPs=レンダラーとは根本的に異なる位置に配置します。
seo-description: text=レンダラーは、テキストを事前にサイズが設定されたレイヤーに適用した場合（size=が指定されている場合も含む）、textPs=レンダラーとは根本的に異なる位置に配置します。
seo-title: テキストの配置
solution: Experience Manager
title: テキストの配置
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# テキストの位置{#text-positioning}

text=レンダラーは、テキストを事前にサイズが設定されたレイヤーに適用した場合（size=が指定されている場合も含む）、textPs=レンダラーとは根本的に異なる位置に配置します。

自己サイズ調整`text=`レイヤーと`textPs=`レイヤーは、外観と位置が似ています。

`textPs=` レンダリングされたテキストグリフの一部がテキストボックスの境界の外側に部分的に広がる場合でも、文字セルの上端をテキストボックスの上端に揃えます(この場合 `\vertalt`)。特定のフォントのレンダリングされたグリフが、テキストボックスの左端と右端から少しはみ出す場合もあります。 すべてのレンダリングされたテキストをレイヤーの長方形内に含める必要があるアプリケーションでは、RTF `\marg*`コマンドまたは`textFlowPath=`を使用してテキストのレンダリング領域を調整できます。

これに対し、`text=`は、必要に応じてレンダリングされたテキストをシフトし、レンダリングされたすべてのグリフが指定したテキストボックス内に完全に収まるようにします。

`text=`は、単純なアプリケーションでは少し使いやすくなりますが、`textPs=`オファーは、フォントの面やテキストの効果に関係なく、正確な位置を指定します。

## 例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

次に、事前にサイズが設定されたテキストの例を示します。 テキストのサイズ自動調整の動作が異なります。

** `Text=`常に上部に狭い余白を表示：**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=`は、テキストボックスの上端に沿ってテキストをレンダリングします。Arialなどの一般的なフォントでも、若干切り抜かれる場合があります。**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=`は、レンダリングされたテキストを自動的に下に移動し、クリッピングを回避します。**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=`は、隆起した部分を含むテキストを移動しません。テキストがレイヤー0上にある場合は、大幅に切り抜かれます。**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**上部の10 pt(200 twip)のマージンは、このテキストを切り抜かずにレンダリングします。**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定のスクリプトフォントのレンダリングされたグリフがテキストボックスの外側に大幅に広がる場合があります。**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
