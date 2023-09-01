---
title: カラー処理
description: RTF 仕様は、&bsol;colortbl で指定されたRGBの色の値を許可します。 各コンポーネントは、&bsol;red, &bsol;green, &bsol;blue コマンドと共に個別に提供されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# カラー処理{#color-handling}

RTF 仕様は、で指定されたRGBの色の値を許可します。 `\colortbl`. 各コンポーネントは、 `\red`, `\green`、および `\blue` コマンド。

独自の RTF 拡張コマンド `\cmykcolortbl` では、CMYK カラーを指定できます。各カラーコンポーネントは、 `\cyan`, `\magenta`, `\yellow`、および `\black` コマンド。

次のカラーコンポーネント値： `\colortbl` は 0 ～ 255 の範囲です。 次のコンポーネント値： `\cmykcolortbl` は 0 ～ 100 の範囲です。

RTF 拡張コマンド `\*\iscolortbl`，サポート元 `textPs=`を使用すると、標準の画像サービングカラー値と、フルRGB、グレー、CMYK およびアルファをサポートするカラーテーブルを指定できます。 構文は次のとおりです。

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 1 つ以上の IS カラー値（「;」で区切る）

同じに複数の種類のカラーテーブルを指定できます `text=` または `textPs=` RTF 文字列。 各カラーテーブルには、異なる数のエントリを含めることができます。 画像サービングは、次の順序で色を検索します。 `\iscolortbl` 前 `\cmykcolortbl` （テキストレイヤーのピクセルタイプが CMYK の場合のみ） `\colortbl`. の場合 `textPs=` 必要に応じて、色は CMYK とRGBの間で正確に変換されます ( 例えば、RGBの色が指定されていて CMYK 出力が必要な場合など )。 特定のインデックス値の色が見つからない場合は、デフォルトの色（黒）が使用されます。

参照： [カラー](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) を参照してください。

## 制限事項 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修飾子 `text=` はをサポートしていません。 `\*\iscolortbl`. 修飾子 `textPs=` はをサポートしていません。 `\cmykcolortbl`.

Photofonts のレンダリング時には、色の選択は無視されます。

## 例 {#section-0f166bb72bd44479be01131077851142}

RTF 文字列を標準の RTF テキストエディタで開いたときに、色のデフォルト値を表示しながら、3 つのテキスト色を変数で制御できます。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
