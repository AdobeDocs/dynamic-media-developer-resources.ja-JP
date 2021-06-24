---
description: 「紙人形」レイヤーアプリを作成します。
solution: Experience Manager
title: 例C
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# 例C{#example-c}

「紙人形」レイヤーアプリを作成します。

背景画像には、モデルまたはマネキンの写真が含まれます。 画像カタログ内の追加レコードには、様々なアパレルやアクセサリーアイテムが含まれ、形状やサイズのマネキンと一致するように撮影されます。

各アパレル/アクセサリー写真は、画像サイズを最小限に抑えるために、マスクし、マスクのバウンディングボックスに切り抜きます。 画像アンカーと解像度は慎重に制御し、レイヤーと背景画像の位置揃えを維持し、すべての画像を画像カタログに追加し、適切な値を`catalog::Resolution`と`catalog::Anchor`に格納します。

レイヤリングに加えて、選択した項目の色も変更します。 これらの項目のレコードは、元の色を削除し、色付けコマンドに適した方法で明るさとコントラストを調整するために前処理されます。 この前処理は、Photoshopなどの画像編集ツールを使用してオフラインで実行するか、簡単な場合は`op_brightness=`と`op_contrast=`を`catalog::Modifier`フィールドに追加して3回だけ実行できます。

すべてのオブジェクトは既にイメージアンカー(`catalog::Anchor`)とスケール(`catalog::Resolution`)によって適切に配置されているので、このアプリケーションでは個別のテンプレートを使用できません。 適切なレイヤー順序を確保するために、クライアントに任せます。

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

高さを指定します。 これにより、背景色で塗りつぶされるマージンを得ることなく、返される画像の幅をマネキン画像の縦横比に応じて変化させることができます。

すべてが同じである限り、各レイヤーに指定する解像度は関係ありません。 このバージョンでは、合成画像より大きいビューを使用できない場合があります。 解像度の値を大きく指定すると、この制限に関連する問題を回避できます。 すべての処理と合成は、最高のパフォーマンスと出力品質を実現するために、要求された画像サイズに最適な解像度で行われます。

すべてのソース画像がフルスケールで同じ解像度を持つ場合は、 `res=`コマンドを省略できます（このタイプのアプリケーションでは、このような場合が考えられます）。

`rootId`は、URLパスで指定された`rootId`と同じであっても、すべての`src=`コマンドに対して指定する必要があります。

画像カタログを使用しない場合は、解像度ベースの拡大縮小アプローチは使用できません。 この場合、各レイヤーの`catalog::Resolution`値と背景レイヤーの`catalog::Resolution`値の比率に基づいて、各レイヤー項目に対して明示的なスケール係数を計算する必要があります。 合成リクエスト（レイヤ数が少ない場合）は、次のようになります。

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
