---
description: RTF仕様では、&bsol;colortblで指定されたRGBカラー値を許可します。 各コンポーネントは、 &bsol;red, &bsol;green, &bsol;blueの各コマンドで個別に提供されます。
solution: Experience Manager
title: カラー処理
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# カラー処理{#color-handling}

RTF仕様は、`\colortbl`で指定されたRGBカラー値を許可します。 各コンポーネントには、`\red`、`\green`、`\blue`の各コマンドが別々に用意されています。

独自のRTF拡張コマンド`\cmykcolortbl`を使用すると、CMYKカラーを指定できます。各カラーコンポーネントには、`\cyan`、`\magenta`、`\yellow`、`\black`の各コマンドが用意されています。

`\colortbl`の色成分の値は0～255の範囲です。 `\cmykcolortbl`のコンポーネント値は0～100の範囲です。

`textPs=`でサポートされるRTF拡張コマンド`\*\iscolortbl`を使用すると、標準の画像サービングカラー値を持つカラーテーブルを、完全なRGB、グレー、CMYK、アルファをサポートするように指定できます。 構文は次のとおりです。

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 1つ以上のISカラー値（「;」で区切る）

同じ`text=`または`textPs=` RTF文字列に複数の種類のカラーテーブルを指定できます。 各カラーテーブルには、異なる数のエントリを含めることができます。 画像サービングは、次の順序で色を検索します。`\iscolortbl`の`\cmykcolortbl`の前（テキストレイヤーのピクセルタイプがCMYKの場合のみ）を`\colortbl`の前に置きます。 `textPs=`の場合のみ、必要に応じて、色はCMYKとRGBの間で正確に変換されます（RGB色は指定されているがCMYK出力は必要な場合など）。 特定のインデックス値の色が見つからない場合は、デフォルトの色（黒）が使用されます。

ISカラー値の構文については、[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)を参照してください。

## 制限事項 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` はをサポートしていま `\*\iscolortbl`せん。`textPs=` はをサポートしていま `\cmykcolortbl`せん。

Photofontsのレンダリング時に、カラー選択は無視されます。

## 例 {#section-0f166bb72bd44479be01131077851142}

RTF文字列を標準のRTFテキストエディタで開いたときに、色のデフォルト値を表示しながら、3つのテキスト色を変数で制御できます。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
