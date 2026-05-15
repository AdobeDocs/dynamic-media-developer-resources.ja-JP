---
title: カラー処理
description: RTF仕様では、&bsol;colortblで指定されたRGB カラー値を使用できます。 各コンポーネントは、&bsol;red、&bsol;green、および&bsol;blue コマンドで個別に提供されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
TQID: 'https://experienceleague.adobe.com/w5IfFwmdMegueJbDMjwvb5XCPuemRcJ1XTqcJFgdEMQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# カラー処理{#color-handling}

RTF仕様では、`\colortbl`で指定されたRGB カラー値を使用できます。 各コンポーネントには、`\red`、`\green`、`\blue`の各コマンドが個別に用意されています。

独自のRTF拡張コマンド `\cmykcolortbl`を使用すると、CMYK カラーを指定できます。各カラーコンポーネントには`\cyan`、`\magenta`、`\yellow`、および`\black` コマンドが用意されています。

`\colortbl`のカラーコンポーネント値は0 ～ 255の範囲です。 `\cmykcolortbl`のコンポーネント値は0 ～ 100の範囲です。

`textPs=`がサポートするRTF拡張コマンド `\*\iscolortbl`は、標準の画像サービングカラー値を持つカラーテーブルを指定する手段を提供します。完全なRGB、グレー、CMYK、およびアルファがサポートされます。 構文は次のとおりです。

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 1つ以上のIS カラー値が、&#39;;&#39;で区切られています

同じ`text=`または`textPs=`のRTF文字列で、複数のタイプのカラーテーブルを指定できます。 各カラーテーブルには、異なる数のエントリを含めることができます。 画像サービングは、次の順序でカラーを検索しようとします：`\iscolortbl` before `\cmykcolortbl` （テキストレイヤーのピクセルタイプがCMYKの場合のみ） before `\colortbl`. `textPs=`の場合のみ、必要に応じて、CMYKとRGBの間でカラーが正確に変換されます（例えば、RGBのカラーが指定されていてもCMYK出力が必要な場合）。 特定のインデックス値の色が見つからない場合は、デフォルトの色（黒）が使用されます。

IS カラー値の構文については、[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)を参照してください。

## 制限 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修飾子`text=`は`\*\iscolortbl`をサポートしていません。 修飾子`textPs=`は`\cmykcolortbl`をサポートしていません。

Photofontsをレンダリングする際に、カラー選択は無視されます。

## 例 {#section-0f166bb72bd44479be01131077851142}

標準のRTF テキストエディターでRTF文字列を開いたときに色のデフォルト値を表示しながら、3つのテキストカラーを変数で制御できるようにします。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
