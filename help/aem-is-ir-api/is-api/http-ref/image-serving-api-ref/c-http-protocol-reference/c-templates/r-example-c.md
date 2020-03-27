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

---


# 例C{#example-c}

「紙の人形」レイヤーアプリを作成します。

背景画像には、モデルやマネキンの写真が含まれます。 画像カタログ内の他のレコードには、さまざまなアパレルやアクセサリーアイテムが含まれており、形状やサイズのマネキンと一致するように撮影されています。

各アパレル/アクセサリーの写真は、画像サイズを最小限に抑えるために、マスクされ、マスクのバウンディングボックスにトリミングされます。 画像アンカーと解像度は、レイヤーと背景画像の間の配置を維持するように注意して制御し、すべての画像が画像カタログに追加され、に適切な値が保存さ `catalog::Resolution` れま `catalog::Anchor`す。

レイヤー化に加えて、選択した項目の色も変更します。 これらの項目のレコードは、色彩の統一コマンドに適した方法で、元の色を削除し、明るさとコントラストを調整するために、事前処理されます。 この前処理は、Photoshopなどの画像編集ツールを使用してオフラインで行うことも、単純な場合は、フィールドにとを追加して3回だけ行うこ `op_brightness=` と `op_contrast=` もでき `catalog::Modifier`ます。

このアプリケーションでは、すべてのオブジェクトが既に画像アンカー( `catalog::Anchor`)と拡大/縮小( `catalog::Resolution`)によって適切に整列されているので、別のテンプレートを使用する必要はありません。 適切なレイヤー順序を確実にするために、クライアントに任せます。

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

高さのみを指定します。 これにより、返される画像の幅をマネキン画像の縦横比に応じて変化させ、背景色で余白を埋める必要がなくなります。

すべてが同じである限り、各レイヤーの解像度を指定する必要はありません。 このバージョンでは、ビューのサイズを合成画像より大きくすることはできません。 大きな解像度の値を指定すると、この制限に関連する問題を回避できます。 すべての処理と合成は、要求された画像サイズに最適な解像度で行われ、最高のパフォーマンスと出力品質を実現します。

すべて `res=` のソース画像がフルスケールで同じ解像度を持つ場合（この種のアプリケーションでは、この場合）、コマンドを省略できます。

URLパ `rootId` スで指定されたのと同 `src=` じでも、すべてのコマンドに対してを指定 `rootId` する必要があります。

画像カタログを使用しない場合、解像度ベースの拡大・縮小方法は使用できません。 この場合、各レイヤーの値と背景レイヤーの値の比率に基づいて、各レイヤー項目の明示的なスケー `catalog::Resolution` ル係数を計算する `catalog::Resolution` 必要があります。 （少ないレイヤーで）合成要求は次のようになります。

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

