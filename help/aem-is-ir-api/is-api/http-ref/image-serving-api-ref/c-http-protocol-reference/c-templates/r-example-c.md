---
title: 例 C
description: 「紙人形」レイヤーアプリを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# 例 C{#example-c}

「紙人形」レイヤーアプリを作成します。

背景画像には、モデルまたはマネキンの写真が含まれます。 画像カタログの追加レコードには、様々なアパレルやアクセサリーアイテムが含まれ、形状やサイズのマネキンに合わせて撮影されます。

各アパレル/アクセサリー写真は、画像サイズを最小限に抑えるために、マスクのバウンディングボックスにマスクおよび切り抜かれます。 画像アンカーと解像度は慎重に制御して、レイヤーと背景画像の位置合わせを維持し、すべての画像を画像カタログに追加し、適切な値を `catalog::Resolution` と `catalog::Anchor` に保存します。

レイヤリングに加えて、選択した項目の色も変更する必要があります。 これらの項目のレコードは、元の色を削除し、色付けコマンドに適した方法で明るさとコントラストを調整するために前処理されます。 この前処理は、Adobe Photoshopなどの画像編集ツールを使用してオフラインでおこなうことも、簡単な場合は `op_brightness=` と `op_contrast=` を `catalog::Modifier` フィールドに追加して 3 回だけおこなうこともできます。

すべてのオブジェクトは既にイメージアンカー ( `catalog::Anchor` ) とスケール ( `catalog::Resolution` ) によって適切に位置揃えされているので、このアプリケーションでは個別のテンプレートを使用できません。 適切な画層順序を確保するため、クライアントに任せます。

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

高さのみを指定します。 これにより、返される画像の幅が、背景色で塗りつぶされるマージンを取得せずに、マネキン画像の縦横比に応じて変化します。

すべてが同じである限り、各レイヤーの解像度を指定する必要はありません。 このバージョンでは、複合画像よりも大きいビューを使用できない場合があります。 解像度の値を大きく指定すると、この制限に関連する問題を回避できます。 すべての処理と合成は、最高のパフォーマンスと出力品質を実現するために、要求されたイメージサイズに最適な解像度で行われます。

すべてのソース画像のフルスケールの解像度が同じ場合（このタイプのアプリケーションの場合は、このような場合）は、 `res=` コマンドを省略できます。

`rootId` は、URL パスで指定された `rootId` と同じであっても、すべての `src=` コマンドに対して指定する必要があります。

画像カタログを使用しない場合は、解像度ベースの拡大/縮小アプローチはできません。 この場合、各レイヤーの `catalog::Resolution` 値と背景レイヤーの `catalog::Resolution` 値の比率に基づいて、各レイヤー項目に対して明示的な尺度係数を計算する必要があります。 合成リクエスト（レイヤ数が少ない）は次のようになります。

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
