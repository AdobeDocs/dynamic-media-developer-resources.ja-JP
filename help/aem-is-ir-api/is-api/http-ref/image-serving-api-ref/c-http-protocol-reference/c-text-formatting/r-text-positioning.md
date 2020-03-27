---
description: text=レンダラーは、事前にサイズのレイヤーに適用される場合（例えばsize=が指定される場合）、textPs=レンダラーとは基本的に異なるテキストの位置を配置します。
seo-description: text=レンダラーは、事前にサイズのレイヤーに適用される場合（例えばsize=が指定される場合）、textPs=レンダラーとは基本的に異なるテキストの位置を配置します。
seo-title: テキストの位置
solution: Experience Manager
title: テキストの位置
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# テキストの位置{#text-positioning}

text=レンダラーは、事前にサイズのレイヤーに適用される場合（例えばsize=が指定される場合）、textPs=レンダラーとは基本的に異なるテキストの位置を配置します。

自動サイズ調整とレ `text=`イヤー `textPs=` の外観と位置は同じです。

`textPs=` レンダリングされたテキストグリフの一部がテキストボックスの境界の一部外に広がる場合でも、文字セルの上端をテキストボックスの上端に揃えます(この場合は `\vertalt`)。 また、特定のフォントのレンダリングされたグリフが、テキストボックスの左端と右端の少し外側に突出する場合があります。 すべてのレンダリングされたテキストをレイヤーの長方形内に含める必要があるアプリケーションの場合は、RTFコ `\marg*` マンドを使用す `textFlowPath=` るか、テキストのレンダリング領域を調整するために使用できます。

これに対し、では、必要に `text=` 応じてレンダリングされたテキストが移動し、レンダリングされたすべてのグリフが指定したテキストボックス内に完全に収まるようにします。

簡単なア `text=` プリケーションでは使いやすくなりますが、では、フォント `textPs=` やテキスト効果とは無関係に正確な位置を指定できます。

## 例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

次の例は、事前にサイズが設定されたテキストです。 テキストの自動サイズ調整の動作が異なります。

**常 `Text=` に上部に狭いマージンを表示：**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

**テキス `textPs=` トボックスの上端に沿ってテキストをレンダリングします。Arial:**などの一般的なフォントの場合でも、テキストがわずかに切り取られる場合があります。

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

**クリッピ `text=` ングを避けるため、レンダリングされたテキストは自動的に下に移動します**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

**テキ `textPs=` ストがレイヤー0:**上にある場合は、隆起した部分を含むテキストは移動されず、大幅にクリッピングされます。

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**上部の10 pt (200 twip)のマージンは、このテキストを切り抜かずにレンダリングします。**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定のスクリプトフォントのレンダリングされたグリフがテキストボックスの外側に大幅に拡張される場合があります。**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
