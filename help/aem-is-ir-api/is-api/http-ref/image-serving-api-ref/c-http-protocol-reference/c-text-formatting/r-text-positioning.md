---
title: テキストの配置
description: text= レンダラーは、事前サイズのレイヤーに適用する場合（つまり、size=が指定されている場合）は、textPs= レンダラーとは根本的に異なるテキストを配置します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
TQID: 'https://experienceleague.adobe.com/7I2AvTFME7oJArnXGqgFmm1pqEDGq5syGguLHlkdvfg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 312
ht-degree: 0%

---

# テキストの配置{#text-positioning}

`text=` レンダラーは、事前サイズのレイヤーに適用する場合（つまり、size=も指定する場合）は、textPs= レンダラーとは根本的に異なるテキストを配置します。

セルフサイズ設定の`text=`および`textPs=`のレイヤーの外観と位置が似ています。

`textPs=`は、レンダリングされたテキスト字形の一部がテキストボックスの境界の一部を超えて伸びている場合でも、文字セルの上部とテキストボックスの上部を整列させます（`\vertalt`と仮定）。 また、特定のフォントのレンダリングされた字形が、テキストボックスの左端と右端からわずかに突出する場合もあります。 レンダリングされたすべてのテキストをレイヤーの長方形に含める必要があるアプリケーションでは、RTF `\marg*` コマンドまたは`textFlowPath=`を使用してテキストのレンダリング領域を調整できます。

対照的に、`text=`はレンダリングされたテキストを必要に応じてシフトし、レンダリングされたすべてのグリフが指定されたテキストボックス内に完全に収まることを保証します。

`text=`は、単純なアプリケーションでは少し使いやすいかもしれませんが、`textPs=`は、フォントの顔やテキスト効果に依存しない正確な配置を提供します。

## 例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

次の例は、事前サイズのテキスト用です。 セルフサイズのテキストの動作が異なります。

**&#x200B; `Text=`は常に上に狭い余白を提供します：**

![&#x200B; テキストの配置の例1つの画像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

**&#x200B; `textPs=`は、テキストボックスの上部にテキストを密接に整列させてレンダリングします。これにより、Arial®:**&#x200B;などの一般的なフォントでも、一部がクリッピングされます

![&#x200B; テキストの配置の例2つの画像](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

**&#x200B; `text=`は、クリッピングを避けるために、レンダリングされたテキストを自動的に下に移動します：**

![&#x200B; テキスト配置の例3つの画像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

**&#x200B; `textPs=`は、隆起した部分を含むテキストを移動しないため、テキストがレイヤー0:**&#x200B;にある場合、大幅にクリッピングされます

![&#x200B; テキスト配置の例4つの画像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**上部の10 pt （200 twips）の余白は、このテキストをクリッピングせずにレンダリングします：**

![&#x200B; テキスト配置の例5つの画像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定のスクリプトフォントのレンダリングされた字形が、テキストボックスの外側に大きく広がる場合があります：**

![&#x200B; テキストの配置の例6つの画像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
