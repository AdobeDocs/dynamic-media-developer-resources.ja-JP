---
description: 'null'
seo-description: 'null'
seo-title: 画像の変換の表示
solution: Experience Manager
title: 画像の変換の表示
topic: Scene7 Image Serving - Image Rendering API
uuid: 8594f746-0e58-4a59-933c-a44dc0b06c25
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像の変換の表示{#view-transform-for-images}

要求に応じてクライアントに返される画像は、 `req=img` 次の値を考慮して合成画像から得られます。 `wid=`、、、 `hei=`、、 `fit=`、 `scl=`、、 `rgn=`および合 `attribute::DefaultPix``attribute::MaxPix`成画像のサイズ。

とが指 `wid=` 定さ `hei=` れ、が指定されていな `scl=` い場合、およびで定義されたビューレクト内に収まるように合成画像が拡大/縮小さ `wid=` れま `hei=`す。 ビューレクトの縦横比が合成画像の縦横比と異なる場合は、値を使用して拡大/縮小された合成画像がビューレクト内で揃えられます（指定した場合）。それ以外の場合は、 `align=` 中央揃えになります。 画像データで覆われていないスペースは、または(指定され `bgc=` ていない場合は)で埋められます `attribute::BkgColor`。

を指定 `scl=` した場合、合成画像はその倍率で拡大・縮小されます。 または/ `wid=` また `hei=` は両方を指定した場合は、必要に応じて、拡大/縮小された画像が切り抜かれ、また `wid=` は余分なスペ `hei=` ースが追加されます。 `align=` は、画像が切り抜かれる場所または余分なスペースが追加される場所を指定し、余分なスペースはまたで埋めら `bgc=` れま `attribute::BkgColor`す。

どちらも指 `wid=`定さ `hei=` れていな `scl=` い場合、もしくはが指定されていない場合、また、合成画像の幅または高さが超過した場合、 `attribute::DefaultPix`合成画像は超えないように拡大縮小されま `attribute::DefaultPix`す。 選択しない場合、合成画像は拡大・縮小せずに使用されます。

これ以上拡大・縮小を行わずにビュー画像が返されるようにするには、を指定しま `scl=1`す。

を指定 `rgn=` すると、返信画像が切り抜かれ、最終的な返信画像のサイズになります。 このサイズは(定義されて `attribute::MaxPix` いる場合)と比較され、どちらのサイズでも返信画像が大きい場合はエラーが生成されます。

アルファ `fmt=` なしでデータを指定した場合、返信画像の透明な領域はすべてまたはで塗りつぶ `bgc=` されま `attribute::BkgColor`す。
