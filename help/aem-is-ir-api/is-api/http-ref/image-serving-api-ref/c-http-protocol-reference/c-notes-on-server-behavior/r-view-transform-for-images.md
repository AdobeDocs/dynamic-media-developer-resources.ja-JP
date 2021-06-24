---
description: 画像の変換の表示
solution: Experience Manager
title: 画像の変換の表示
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: fc20cbc2-9d66-4c52-80c2-9ba7c3b54744
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 画像の変換の表示{#view-transform-for-images}

`req=img`リクエストに応じてクライアントに返されるイメージは、次の値を考慮して、複合イメージから派生します。`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`および合成画像のサイズ。

`wid=`と`hei=`を指定し、`scl=`が指定されていない場合、合成画像は、`wid=`と`hei=`で定義された表示範囲内に収まるように拡大/縮小されます。 ビューレクトの縦横比がコンポジット画像の縦横比と異なる場合、拡大/縮小されたコンポジット画像は、`align=`値を使用してビューレクト内に揃えられます（指定した場合、中央揃えになります）。 画像データで覆われていないスペースは`bgc=`で埋められます。指定しない場合は`attribute::BkgColor`で埋められます。

`scl=`を指定した場合、合成画像はその倍率で拡大/縮小されます。 `wid=`や`hei=`も指定した場合は、拡大/縮小された画像は`wid=`や`hei=`に切り抜かれ、必要に応じて空白が追加されます。 `align=` は、画像を切り抜く場所または余分なスペースを追加する場所を指定し、余分なスペースはまたはで埋め `bgc=` ま `attribute::BkgColor`す。

`wid=`、`hei=`、`scl=`のいずれも指定されておらず、合成画像の幅または高さが`attribute::DefaultPix`を超える場合、合成画像は`attribute::DefaultPix`を超えないように拡大/縮小されます。 それ以外の場合は、合成画像は拡大・縮小せずに使用されます。

ビュー画像がそれ以上拡大・縮小されずに返されるようにするには、`scl=1`を指定します。

`rgn=`を指定した場合、返信画像は切り抜かれ、最終的な返信画像のサイズに達します。 このサイズは`attribute::MaxPix`（定義されている場合）と比較され、返信画像のサイズがどちらのサイズよりも大きい場合はエラーが生成されます。

`fmt=`でアルファなしのデータを指定した場合、返信画像内の透明な領域はすべて`bgc=`または`attribute::BkgColor`で塗りつぶされます。
