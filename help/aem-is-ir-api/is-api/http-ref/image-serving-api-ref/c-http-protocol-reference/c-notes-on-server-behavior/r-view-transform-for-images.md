---
description: 画像の変換を表示
solution: Experience Manager
title: 画像の変換を表示
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 画像の変換を表示{#view-transform-for-images}

イメージが `req=img` リクエストは、次の値を考慮して、合成イメージから派生します。 `wid=`, `hei=`, `fit=`, `scl=`, `rgn=`, `attribute::DefaultPix`, `attribute::MaxPix`、および合成画像のサイズ。

次の場合 `wid=` および `hei=` が指定され、 `scl=` ではなく、合成画像は、 `wid=` および `hei=`. 表示方向の縦横比が合成画像の縦横比と異なる場合、拡大/縮小された合成画像は、 `align=` 値を指定する場合は、それ以外の場合は中央揃えにします。 画像データで覆われていないスペースは、 `bgc=` または、指定されていない場合は、 `attribute::BkgColor`.

次の場合 `scl=` を指定すると、合成イメージはその尺度係数で拡大・縮小されます。 次の場合 `wid=` および/または `hei=` を指定した場合、拡大/縮小された画像は次のように切り抜かれます。 `wid=` および/または `hei=` または必要に応じて余分なスペースを追加します。 `align=` は、画像を切り抜く場所または余分なスペースを追加する場所を指定し、余分なスペースは `bgc=` または `attribute::BkgColor`.

どちらでもない場合 `wid=`, `hei=` nor `scl=` を指定し、合成画像の幅または高さが次の値を超えた場合に、 `attribute::DefaultPix`を指定した場合、合成画像は拡大/縮小され、 `attribute::DefaultPix`. それ以外の場合は、合成画像は拡大・縮小せずに使用されます。

これ以上拡大・縮小せずにビュー画像が返されるようにするには、 `scl=1`.

次の場合 `rgn=` が指定された場合、返信画像は適切に切り抜かれ、最終的な返信画像のサイズに達します。 このサイズは、 `attribute::MaxPix` （定義されている場合）。返信画像のサイズがどちらのサイズよりも大きい場合は、エラーが生成されます。

次の場合 `fmt=` には、アルファを含まないデータを指定します。返信画像の透明な領域は、 `bgc=` または `attribute::BkgColor`.
