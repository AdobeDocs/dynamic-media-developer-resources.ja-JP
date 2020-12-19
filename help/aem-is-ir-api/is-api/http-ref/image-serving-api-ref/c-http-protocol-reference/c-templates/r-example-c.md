---
description: 「紙の人形」レイヤーアプリを作成します。
seo-description: 「紙の人形」レイヤーアプリを作成します。
seo-title: 例C
solution: Experience Manager
title: 例C
topic: Scene7 Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# 例C{#example-c}

「紙の人形」レイヤーアプリを作成します。

背景画像には、モデルやマネキンの写真が含まれます。 画像カタログ内の追加記録には、様々な衣料やアクセサリーアイテムが含まれており、マネキンの形状やサイズに合わせて撮影されます。

各アパレル/アクセサリー写真はマスクされ、マスクのバウンディングボックスにトリミングされて、画像サイズを最小限に抑えられます。 画像アンカーと解像度は、レイヤーと背景画像の間の位置揃えを維持するように注意して制御され、すべての画像が画像カタログに追加され、適切な値が`catalog::Resolution`と`catalog::Anchor`に保存されます。

レイヤー化に加えて、選択した項目の色も変更します。 これらの項目のレコードは、前処理されて元の色が削除され、色彩の統一コマンドに適した方法で明るさとコントラストが調整されます。 この前処理は、Photoshopなどの画像編集ツールを使用してオフラインで行うか、単純な場合は`op_brightness=`と`op_contrast=`を`catalog::Modifier`フィールドに追加して、3つに1回行うことができます。

すべてのオブジェクトが既に画像アンカー(`catalog::Anchor`)と拡大/縮小(`catalog::Resolution`)によって適切に整列されているので、このアプリケーションでは個別のテンプレートを使用できません。 レイヤーの順序を適切に決めるために、クライアントに任せます。

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

高さのみを指定します。 これにより、余白を背景色で塗りつぶすことなく、返される画像の幅をマネキン画像の縦横比に応じて変化させることができます。

すべてが同じである限り、各レイヤーの解像度を指定する必要はありません。 このバージョンでは、表示のサイズを合成画像より大きくできない場合があります。 解像度の値を大きく指定すると、この制限に関連する問題を回避できます。 すべての処理と合成は、要求された画像サイズに対して最適な解像度で行われ、最高のパフォーマンスと出力品質を実現します。

すべてのソース画像がフルスケールで同じ解像度を持つ場合は、`res=`コマンドを省略できます（この種のアプリケーションでは省略される可能性があります）。

`rootId`は、URLパスで指定された`rootId`と同じである場合でも、すべての`src=`コマンドに対して指定する必要があります。

画像カタログを使用しない場合、解像度ベースの拡大・縮小方法は使用できません。 この場合、各レイヤーの`catalog::Resolution`値と背景レイヤーの`catalog::Resolution`値の比率に基づいて、各レイヤー項目の明示的なスケール係数を計算する必要があります。 合成要求（レイヤ数が少ない）は次のようになります。

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

