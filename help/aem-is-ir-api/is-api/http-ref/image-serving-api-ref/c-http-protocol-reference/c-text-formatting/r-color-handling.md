---
title: カラー処理
description: RTF 仕様では、&bsol;colortbl で指定されたRGB カラー値が許可されています。 各コンポーネントは、&bsol;red、&bsol;green および&bsol;blue コマンドと共に個別に提供されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# カラー処理{#color-handling}

RTF 仕様では、`\colortbl` で指定されたRGB カラー値が許可されています。 各コンポーネントは、`\red`、`\green`、`\blue` の各コマンドと個別に提供されます。

独自の RTF 拡張コマンド `\cmykcolortbl` を使用すると、`\cyan`、`\magenta`、`\yellow` および `\black` コマンドで提供される各カラーコンポーネントで CMYK 色を指定できます。

`\colortbl` の色成分の値は、0 ～ 255 の範囲です。 `\cmykcolortbl` のコンポーネント値は 0 ～ 100 の範囲です。

`\*\iscolortbl` がサポートする RTF 拡張コマンド `textPs=` では、RGB、グレー、CMYK、アルファを完全にサポートする標準の画像サービングカラー値を使用して、カラーテーブルを指定できます。 次の構文で表されます。

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

1 つ以上の IS カラー値を *[!DNL colors]* し、「;」で区切ります。

同じ `text=` または RTF 文字列で複数の種類のカラーテーブル `textPs=` 指定できます。 各カラーテーブルには、異なる数のエントリを含めることができます。 画像サービングでは、カラーを次の順序で検索しようとします。`\iscolortbl` より前の `\cmykcolortbl` （テキストレイヤーのピクセルタイプが CMYK の場合のみ） `\colortbl`。 た `textPs=` えば、必要に応じて、CMYK とRGBの間でカラーが正確に変換されます（例えば、RGB カラーが指定されていても、CMYK 出力が必要な場合など）。 特定のインデックス値の色が見つからない場合は、デフォルトの色（黒）が使用されます。

IS カラー値の構文の説明については、[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) を参照してください。

## 制限 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修飾子 `text=` は `\*\iscolortbl` をサポートしていません。 修飾子 `textPs=` は `\cmykcolortbl` をサポートしていません。

フォトフォントをレンダリングする際、カラーの選択は無視されます。

## 例 {#section-0f166bb72bd44479be01131077851142}

3 つのテキストカラーを変数で制御しながら、標準の RTF テキストエディターで RTF 文字列を開いたときに、カラーのデフォルト値を表示できます。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
