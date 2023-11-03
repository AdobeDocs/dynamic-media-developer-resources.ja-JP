---
title: テキストの配置
description: text=レンダラーは、事前サイズのレイヤーに適用する場合（size=が指定されている場合）、textPs=レンダラーとは根本的に異なるテキストを配置します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# テキストの配置{#text-positioning}

The `text=` レンダラーは、事前サイズのレイヤーに適用した場合（size=を指定した場合）、textPs=レンダラーとは根本的に異なるテキストを配置します。

自己サイズ設定 `text=`および `textPs=` 画層の外観と位置は同じです。

The `textPs=` 文字セルの上部をテキストボックスの上部に揃えます ( `\vertalt`) を含め、レンダリングされたテキストグリフの一部がテキストボックスの境界の外側に部分的に広がる場合でも同様です。 特定のフォントのレンダリングされたグリフが、テキストボックスの左右端を少し越えて突出する場合もあります。 レイヤーの長方形内にすべてのレンダリングテキストを含める必要があるアプリケーションの場合、RTF `\marg*` コマンドまたは `textFlowPath=` を使用して、テキストのレンダリング領域を調整できます。

これに対して、 `text=` 必要に応じて、レンダリングされたテキストを移動し、指定したテキストボックス内にレンダリングされたすべてのグリフが完全に収まるようにします。

While `text=` は、単純なアプリケーションで使用する方が若干簡単な場合があります。 `textPs=` では、フォント面やテキスト効果に関係なく、正確な位置を指定できます。

## 例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

次に、事前サイズのテキストの例を示します。 テキストのサイズ変更の動作が異なります。

** `Text=` 常に上部に狭い余白を提供します：**

![テキストの配置の例 1 つの画像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` テキストをテキストボックスの上端に合わせてレンダリングします。その結果、Arial®:**などの一般的なフォントでも、少しクリップが発生します。

![テキストの配置の例 2 つの画像](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` レンダリングされたテキストを自動的に下にシフトし、クリッピングを避けます。**

![テキストの配置の例：3 つの画像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` 浮き出し部分を含むテキストを移動しないので、テキストがレイヤー 0:**上にある場合は大幅なクリッピングが発生します。

![テキストの配置の例 4 つの画像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**上部の 10 pt(200 twips) の余白は、このテキストをクリッピングなしでレンダリングします。**

![テキストの配置の例 5 つの画像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定のスクリプトフォントのレンダリングされたグリフが、テキストボックスの外側に大幅に拡張する場合があります。**

![テキストの配置の例 6 つの画像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
