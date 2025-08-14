---
title: 例 C
description: 「紙の人形」レイヤリングアプリケーションを作成します。
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

「紙の人形」レイヤリングアプリケーションを作成します。

背景画像には、モデルまたはマネキンの写真が含まれます。 画像カタログの追加レコードには、形状やサイズのマネキンに合わせて撮影されたさまざまなアパレルやアクセサリーが含まれています。

各アパレル/アクセサリーの写真は、マスクされ、マスクのバウンディングボックスに切り抜かれて画像サイズが最小限に抑えられます。 画像アンカーと解像度は、レイヤーと背景画像の間の整列を維持するために慎重に制御され、すべての画像は、画像カタログに追加され、適切な値が `catalog::Resolution` および `catalog::Anchor` に格納されます。

レイヤー化に加えて、選択した項目の色も変更する必要があります。 これらの項目のレコードは、元の色を削除し、色付けコマンドに適した方法で明るさとコントラストを調整するために前処理されます。 この前処理は、Adobe Photoshopなどの画像編集ツールを使用して、オフラインで実行することも、簡単なケースでは、`op_brightness=` フィールドに `op_contrast=` と `catalog::Modifier` を追加することで簡単に実行することもできます。

このアプリケーションでは、すべてのオブジェクトが既にイメージ アンカーによって適切に位置合わせされており（`catalog::Anchor`）、尺度が設定されているため（`catalog::Resolution`）、別のテンプレートは必要ありません。 適切なレイヤー順序を確保するかどうかは、クライアントが決定します。

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

高さのみが指定されます。 これにより、返される画像の幅をマネキン画像の縦横比に応じて変化させることができ、背景色で余白を埋めることはありません。

すべてのレイヤーが同じである限り、各レイヤーに対して指定する解像度は関係ありません。 このバージョンでは、ビューを合成画像より大きくできない場合があります。 解像度の値を大きくすると、この制限に関連する問題を回避できます。 すべての処理および合成は、最高のパフォーマンスと出力品質を達成するために、リクエストされた画像サイズに最適な解像度で行われます。

すべてのソース画像の解像度がフルスケールで同じ場合（このタイプのアプリケーションの場合によくある）、`res=` のコマンドを省略できます。

URL パスで指定した `rootId` と同じであっても、すべての `src=` コマンドに対して `rootId` を指定する必要があります。

画像カタログを使用しない場合、解像度ベースの拡大縮小アプローチは使用できません。 この場合には、各画層の `catalog::Resolution` 値と背景の画層の `catalog::Resolution` 値との比率に基づいて、各画層項目ごとに明確な尺度係数を計算する必要があります。 合成リクエスト（レイヤ数が少ない）は次のようになります。

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
