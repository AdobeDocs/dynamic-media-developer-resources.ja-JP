---
title: テキストの配置
description: text=レンダラーは、事前サイズのレイヤーに適用する場合（size=が指定されている場合も同様）、textPs=レンダラーとは基本的に異なるテキストを配置します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# テキストの配置{#text-positioning}

`text=` レンダラーは、事前サイズのレイヤーに適用する場合（size=が指定されている場合など）、textPs=レンダラーとは根本的に異なるテキストを配置します。

セルフサイズ `text=` と `textPs=` レイヤーの外観と位置は同じです。

`textPs=` は、レンダリングされたテキストグリフの一部がテキストボックス境界の外側に広がる場合でも、文字セルの上部をテキストボックスの上部に揃えます（`\vertalt` と仮定）。 特定のフォントのレンダリングされたグリフが、テキストボックスの左右の端を少し越えて突出する場合もあります。 レイヤーの長方形内にすべてのレンダリングテキストを含める必要があるアプリケーションの場合は、RTF `\marg*` コマンドまたは `textFlowPath=` を使用して、テキストのレンダリング領域を調整できます。

これに対して、`text=` は、必要に応じてレンダリングされたテキストを移動し、レンダリングされたすべてのグリフが指定したテキストボックス内に完全に収まることを保証します。

`text=` は、単純なアプリケーションで使いやすい場合がありますが、`textPs=` は、フォント面やテキスト効果に関係なく、正確な位置を指定できます。

## 例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

次に、事前サイズのテキストの例を示します。 テキストのサイズ変更の動作が異なります。

** `Text=` 常に上部に狭い余白を提供します：**

![テキストの配置の例 1 つの画像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` は、テキストをテキストボックスの上端に合わせて厳密に配置してレンダリングします。Arial®:**などの一般的なフォントでも、少しクリップが発生します。

![テキストの配置例 2 つの画像](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` レンダリングされたテキストを自動的に下に移動して、クリッピングを避けます。**

![テキストの配置の例 3 つの画像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` では、隆起した部分を含むテキストは移動されず、テキストがレイヤー 0 上にある場合は大幅なクリッピングが発生します。**

![テキストの配置の例 4 つの画像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**上部の余白が 10 pt (200 twip) の場合、このテキストはクリッピングなしでレンダリングされます。**

![テキストの配置の例 5 つの画像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定のスクリプトフォントのレンダリングされたグリフが、テキストボックスの外側に大きく広がる場合があります。**

![テキストの配置の例 6 つの画像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
