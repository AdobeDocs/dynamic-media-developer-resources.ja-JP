---
title: SVG
description: このセクションの設定は、SVGレンダリングが必要な場合にのみ考慮する必要があります。
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

このセクションの設定は、SVGレンダリングが必要な場合にのみ考慮する必要があります。

## SV::SvgHeapSize - SVGのヒープサイズ {#section-59ab17681daa4be8b5d794713e1a504e}

SVGレンダラーの Java ヒープサイズ。 デフォルトは「200m」（200 MB）です。

## PS::svgProvider.rootPaths -SVGデータのルートフォルダー {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVGのソースデータファイルの場所。 1 つ以上の絶対ファイルパスまたは *[!DNL install_folder]* に対する相対パスをセミコロンで区切って指定できます。 通常は、`IS::RootPath` と同じ値に設定します。

## PS::svgProvider.SVGFileSizeLimit – 最大SVGファイルサイズ {#section-b9c81e3e104642ebbdd9f000843d3256}

SVGソースファイルの最大サイズ（k バイト単位）。 この制限を超えるSVGファイルをレンダリングしようとすると、サーバーがエラーを返します。 デフォルトは 1024 K バイトです。

## IS::SvgMAxRenderRgnPixels -SVG出力画像のサイズ制限 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRender で生成できる画像のサイズを制限します。 0 より大きい整数値（100 万ピクセル）。 レンダリング操作がサイズ制限を超える場合、エラーが返されます。 初期設定値は 4 です。

## PS::svgProvider.port - [!DNL Platform Server] リスニングポート {#section-f7e42a96c2dd4523b46f0557c239e659}

SVGレンダリングに埋め込む [!DNL Platform Server] から画像を取得するために SvgRender に使用されるポート。

重要 SVGRender コンポーネントを正しく機能させるには、この構成オプションを `TC::PsPort` と同じ値に設定する必要があります。

## PS::svgProvider.fontRoot -SVGフォントファイルフォルダー {#section-a8d45b0d68504945b8780f5eac351b0d}

SvgRender がフォントテキストのレンダリングに必要なSVGファイルを見つける場所を指定します。通常、`IS::RootPaths` で指定されたパスの 1 つです。 デフォルトは [!DNL *[!DNL install_folder]*/images] です。

## SVG::SVGRender.port, IS::SVGTcpPort - SVG通信ポート {#section-608687123aa644b7b58fe42385d71b79}

Image Server と SVGRender コンポーネントが通信するポートを設定します。

>[!NOTE]
>
>SVGRender コンポーネントを正しく機能させるには、`SVG::SVGRender.port` と `IS::SVGTcpPort` に同じポート番号を指定する必要があります。
