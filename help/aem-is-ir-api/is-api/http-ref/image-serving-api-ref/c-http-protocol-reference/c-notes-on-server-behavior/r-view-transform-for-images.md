---
description: 画像の表示変換
solution: Experience Manager
title: 画像の表示変換
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# 画像の表示変換{#view-transform-for-images}

`req=img`要求に応じてクライアントに返される画像は、次の値を考慮して、複合画像から得られます。`wid=`、`hei=`、`fit=`、`scl=`、`rgn=`、`attribute::DefaultPix`、`attribute::MaxPix`、合成画像のサイズ。

`wid=`と`hei=`を指定し、`scl=`を指定しない場合、`wid=`と`hei=`で定義される表示レクト内に収まるように、合成画像は拡大縮小されます。 表示rectの縦横比が合成画像の縦横比と異なる場合は、`align=`値を使用して、拡大/縮小された合成画像を表示rect内で揃えます（指定した場合）。それ以外の場合は中央揃えにします。 画像データで覆われていないスペースは、`bgc=`または`attribute::BkgColor`で埋められます。

`scl=`を指定した場合、合成画像はその倍率で拡大・縮小されます。 `wid=`や`hei=`も指定した場合は、必要に応じて、拡大・縮小された画像が`wid=`や`hei=`に切り抜かれるか、または空白が追加されます。 `align=` は、画像を切り抜く場所または余分なスペースを追加する場所を指定し、余分なスペースは `bgc=` またはで埋めま `attribute::BkgColor`す。

`wid=`、`hei=`、`scl=`のいずれも指定されていない場合で、合成画像の幅または高さが`attribute::DefaultPix`を超える場合は、合成画像は`attribute::DefaultPix`を超えないように拡大縮小されます。 それ以外の場合は、合成画像は拡大・縮小せずに使用されます。

表示画像をそれ以上拡大・縮小せずに返すには、`scl=1`を指定します。

`rgn=`を指定した場合、返信画像はそれに応じて切り抜かれ、最終的な返信画像のサイズに到達します。 このサイズは`attribute::MaxPix`と比較され（定義されている場合）、返信画像のサイズがどちらのサイズよりも大きい場合はエラーが生成されます。

`fmt=`でアルファなしのデータを指定した場合、返信画像の透明部分はすべて`bgc=`または`attribute::BkgColor`で塗りつぶされます。
