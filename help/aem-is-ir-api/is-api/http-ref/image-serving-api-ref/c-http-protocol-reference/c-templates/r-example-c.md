---
title: 例C
description: 「紙の人形」レイヤリングアプリケーションを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
TQID: 'https://experienceleague.adobe.com/PRayyg-oBmqHohNjYBa4bgtxdK9tdb6qd6vaLkGJZEg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# 例C{#example-c}

「紙の人形」レイヤリングアプリケーションを作成します。

背景画像には、モデルまたはマネキンの写真が含まれます。 画像カタログの追加のレコードには、さまざまなアパレルやアクセサリーのアイテムが含まれており、マネキンの形やサイズに合わせて撮影されています。

各アパレル/アクセサリー写真はマスクされ、画像サイズを最小限に抑えるためにマスクのバウンディングボックスに切り抜かれます。 画像のアンカーと解像度は、レイヤーと背景画像との整合性を維持するために慎重に制御され、すべての画像が画像カタログに追加され、適切な値が`catalog::Resolution`と`catalog::Anchor`に保存されます。

レイヤーに加えて、選択した項目のカラーも変更します。 これらのアイテムのレコードは、元のカラーを削除し、色付けコマンドに適した方法で明るさとコントラストを調整するために前処理されます。 この前処理は、Adobe Photoshopなどの画像編集ツールを使用してオフラインで実行することも、簡単なケースでは、`op_brightness=`と`op_contrast=`を`catalog::Modifier` フィールドに追加することで簡単に実行することもできます。

このアプリケーションでは、すべてのオブジェクトが既に画像アンカー（`catalog::Anchor`）および拡大・縮小（`catalog::Resolution`）によって適切に配置されているため、別のテンプレートは必要ありません。 適切なレイヤー順序を確保するのは、クライアントに任せます。

一般的なリクエストは次のようになります。

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

高さのみが指定されます。 これにより、返される画像の幅は、マネキン画像の縦横比に応じて異なり、余白が背景色で塗りつぶされることはありません。

すべてのレイヤーが同じである限り、各レイヤーに対してどのような解像度が指定されているかは関係ありません。 このバージョンでは、ビューを合成画像よりも大きくすることはできません。 大きな解像度の値を指定すると、この制限に関連する問題を回避できます。 あらゆる処理と合成は、要求された画像サイズに対して最適な解像度で行われ、最高のパフォーマンスと出力品質を実現するのに役立ちます。

すべてのソース画像がフルスケールで同じ解像度を持つ場合、`res=` コマンドは省略できます（このタイプのアプリケーションの場合はおそらく省略されます）。

`rootId`は、URL パスで指定された`rootId`と同じであっても、すべての`src=` コマンドに対して指定する必要があります。

画像カタログを使用しない場合、解像度ベースの拡大・縮小は不可能です。 この場合、各レイヤーの`catalog::Resolution`値と背景レイヤーの`catalog::Resolution`値の比率に基づいて、各レイヤー項目について明示的なスケール係数を計算する必要があります。 合成リクエスト（レイヤー数が少ない）は次のようになります。

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
