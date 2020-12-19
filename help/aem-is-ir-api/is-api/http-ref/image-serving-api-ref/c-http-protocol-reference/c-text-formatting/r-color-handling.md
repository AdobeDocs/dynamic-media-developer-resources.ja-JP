---
description: RTF仕様では、&bsol;colortblで指定されたRGBカラー値が許可されています。 各コンポーネントには、&bsol;red、&bsol;green、&bsol;blueの各コマンドが別々に用意されています。
solution: Experience Manager
title: カラー処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 925fb4b0a9018d711ea9a1db248dc2ddc803c9fb
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# 色処理{#color-handling}

RTF仕様では、`\colortbl`で指定されたRGBカラー値が許可されています。 各コンポーネントには、`\red`、`\green`、`\blue`の各コマンドが別々に用意されています。

独自のRTF拡張子コマンド`\cmykcolortbl`を使用すると、CMYK色を指定できます。各カラーコンポーネントには、`\cyan`、`\magenta`、`\yellow`、`\black`の各コマンドが付属します。

`\colortbl`の色成分値は0 ～ 255の範囲です。 `\cmykcolortbl`のコンポーネント値は0 ～ 100の範囲です。

`textPs=`でサポートされるRTF拡張子コマンド`\*\iscolortbl`を使用すると、標準の画像サービングカラー値を持つカラーテーブルを、フルRGB、グレー、CMYK、アルファをサポートする形式で指定できます。 次の構文を使用します。

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 1つ以上のISカラー値、「;」で区切る

同じ`text=`または`textPs=` RTF文字列内に、複数の種類のカラーテーブルを指定できます。 各カラーテーブルのエントリ数は異なる場合があります。 画像サービングでは、次の順序で色を検索します。`\iscolortbl`を`\cmykcolortbl`の前（テキストレイヤーのピクセルタイプがCMYKの場合のみ）に置き、`\colortbl`の前に置きます。 `textPs=`のみ、必要に応じて色はCMYKとRGBの間で正確に変換されます（RGB色が指定されているがCMYK出力が必要な場合など）。 特定のインデックス値の色が見つからない場合は、初期設定の色（黒）が使用されます。

ISカラー値の構文については、[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)を参照してください。

## 制限{#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` はをサポートしません `\*\iscolortbl`。`textPs=` はをサポートしません `\cmykcolortbl`。

Photofontsのレンダリング時、カラーの選択は無視されます。

## 例 {#section-0f166bb72bd44479be01131077851142}

変数を使用して3つのテキストカラーを制御でき、標準のRTFテキストエディタでRTF文字列を開いた場合でも、カラーのデフォルト値が表示されます。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
