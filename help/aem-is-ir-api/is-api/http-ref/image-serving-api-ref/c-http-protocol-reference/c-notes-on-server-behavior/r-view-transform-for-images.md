---
description: 画像のビュー変換
solution: Experience Manager
title: 画像のビュー変換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 画像のビュー変換{#view-transform-for-images}

`req=img` 要求に応答してクライアントに返される画像は、`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix` の値および合成画像のサイズを考慮することによって、合成画像から派生されます。

`wid=` と `hei=` が指定され、`scl=` が指定されていない場合、合成イメージは、`wid=` と `hei=` で定義されるビューの rect 内に完全に収まるように尺度が調整されます。 ビュー rect のアスペクト比が合成画像のアスペクト比と異なる場合、スケールされた合成画像は、`align=` の値を使用してビュー rect 内で位置揃えされます（指定した場合）。それ以外の場合は中央揃えされます。 画像データでカバーされないスペースは、`bgc=` で埋められます。指定しない場合は `attribute::BkgColor` で埋められます。

`scl=` を指定した場合、合成画像はそのスケール係数によってスケールされます。 `wid=` や `hei=` も指定されている場合は、必要に応じて、拡大縮小された画像が `wid=` や `hei=` に切り抜かれるか、余分なスペースが追加されます。 `align=` は、画像を切り抜く場所や余分なスペースを追加する場所を指定し、余分なスペースは `bgc=` または `attribute::BkgColor` で埋めます。

`wid=`、`hei=`、`scl=` のいずれも指定されておらず、合成画像の幅または高さが `attribute::DefaultPix` を超える場合、合成画像は `attribute::DefaultPix` を超えないように拡大縮小されます。 それ以外の場合は、拡大縮小せずに合成画像を使用します。

これ以上の拡大縮小を行わずにビューイメージが返されるようにするには、`scl=1` を指定します。

`rgn=` を指定すると、返信画像はそれに応じて切り抜かれ、最終的な返信画像サイズに到達します。 このサイズは `attribute::MaxPix` （定義されている場合）と比較され、返信画像がいずれかのディメンションでより大きい場合、エラーが生成されます。

アルファを使用せずにデータを指定した `fmt=` 合、返信画像内の透明領域は `bgc=` または `attribute::BkgColor` で塗りつぶされます。
