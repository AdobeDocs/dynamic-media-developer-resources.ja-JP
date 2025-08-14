---
title: SVG
description: この節の設定は、SVGのレンダリングが必要な場合にのみ考慮する必要があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 2%

---

# SVG{#svg}

この節の設定は、SVGのレンダリングが必要な場合にのみ考慮する必要があります。

## SV::SvgHeapSize - SVGのヒープサイズ {#section-59ab17681daa4be8b5d794713e1a504e}

SVG レンダラーの Java ヒープサイズ。 デフォルトは「200m」（200 MB）です。

## PS::svgProvider.rootPaths - SVG データルートフォルダー {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG ソースデータファイルの場所。 1 つ以上の絶対ファイルパスまたは *[!DNL install_folder]* に対する相対パスをセミコロンで区切って指定できます。 通常は、`IS::RootPath` と同じ値に設定します。

## PS::svgProvider.SVGFileSizeLimit - SVGの最大ファイルサイズ {#section-b9c81e3e104642ebbdd9f000843d3256}

SVG ソースファイルの最大サイズ（kBytes）。 この制限を超えるSVG ファイルをレンダリングしようとすると、サーバーがエラーを返します。 デフォルトは 1024 K バイトです。

## IS::SvgMAxRenderRgnPixels - SVG出力画像のサイズ制限 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRender で生成できる画像のサイズを制限します。 0 より大きい整数値（100 万ピクセル）。 レンダリング操作がサイズ制限を超える場合、エラーが返されます。 初期設定値は 4 です。

## PS::svgProvider.port - [!DNL Platform Server] リスニングポート {#section-f7e42a96c2dd4523b46f0557c239e659}

SVG レンダリングに埋め込む [!DNL Platform Server] から画像を取得するために SvgRender に使用されるポート。

重要 SVGRender コンポーネントを正しく機能させるには、この構成オプションを `TC::PsPort` と同じ値に設定する必要があります。

## PS::svgProvider.fontRoot - SVG Font Files フォルダー {#section-a8d45b0d68504945b8780f5eac351b0d}

SvgRender がSVG テキストのレンダリングに必要なフォントファイルを見つける場所を指定します。通常、`IS::RootPaths` で指定されたパスの 1 つです。 デフォルトは [!DNL *[!DNL install_folder]*/images] です。

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Image Server と SVGRender コンポーネントが通信するポートを設定します。

>[!NOTE]
>
>SVGRender コンポーネントを正しく機能させるには、`SVG::SVGRender.port` と `IS::SVGTcpPort` に同じポート番号を指定する必要があります。
