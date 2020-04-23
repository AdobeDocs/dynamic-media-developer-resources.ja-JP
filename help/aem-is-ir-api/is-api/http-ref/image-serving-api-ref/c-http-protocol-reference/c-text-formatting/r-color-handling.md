---
description: RTF仕様では、\colortblで指定したRGBカラー値が許可されています。 各コンポーネントには、\red、\green、\blueの各コマンドが別々に用意されています。
seo-description: RTF仕様では、\colortblで指定したRGBカラー値が許可されています。 各コンポーネントには、\red、\green、\blueの各コマンドが別々に用意されています。
seo-title: カラー処理
solution: Experience Manager
title: カラー処理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 341693d69fc414dacf984d66e2eaeba2418e663b

---


# カラー処理{#color-handling}

RTF仕様では、で指定したRGBカラー値が許可されま `\colortbl`す。 各コンポーネントには、、、およびの各コ `\red`マンド `\green`が別々に用意さ `\blue` れています。

独自のRTF拡張コマンドを使用す `\cmykcolortbl` ると、CMYKカラーを指定できます。各カラーコンポーネントには、、、、およびの各コ `\cyan`マンド `\magenta`が付 `\yellow`属して `\black` います。

の色成分の値 `\colortbl` は、0 ～ 255の範囲です。 のコンポーネン `\cmykcolortbl` ト値は0 ～ 100の範囲です。

でサポートされて `\*\iscolortbl`いるRTF拡張 `textPs=`コマンドを使用すると、標準の画像サービングカラー値を持つカラーテーブルを、フルRGB、グレー、CMYK、アルファをサポートして指定できます。 次の構文を使用します。

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 1つ以上のISカラー値、「;」で区切る

同じ文字列またはRTF文字列で複数のタイプのカラーテーブルを指 `text=` 定で `textPs=` きます。 各カラーテーブルのエントリ数は異なる場合があります。 画像サービングは、次の順序で色を検索します。の前( `\iscolortbl` テキストレイヤーのピクセルタイプがCMYKの場合のみ) `\cmykcolortbl``\colortbl`。 必要 `textPs=` に応じて、色はCMYKとRGBの間で正確に変換されます（RGB色が指定されているがCMYK出力が必要な場合など）。 特定のインデックス値の色が見つからない場合は、デフォルトの色（黒）が使用されます。

ISカラー値 [の構文](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) については、colorを参照してください。

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` はサポートされませ `\*\iscolortbl`ん。 `textPs=` はサポートされませ `\cmykcolortbl`ん。

Photofontsのレンダリング時に、色の選択は無視されます。

## 例 {#section-0f166bb72bd44479be01131077851142}

RTF文字列を標準のRTFテキストエディターで開いたときに、色のデフォルト値を表示したまま、3つのテキスト色を変数で制御できます。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
