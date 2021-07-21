---
description: この節の設定は、SVGのレンダリングが必要な場合にのみ考慮する必要があります。
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# SVG{#svg}

この節の設定は、SVGのレンダリングが必要な場合にのみ考慮する必要があります。

## SV::SvgHeapSize - SVGヒープサイズ {#section-59ab17681daa4be8b5d794713e1a504e}

SVGレンダラーのJavaヒープサイズです。 デフォルトは「200m」（200Mバイト）です。

## PS::svgProvider.rootPaths - SVGデータルートフォルダー {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVGソースデータファイルの場所。 絶対ファイルパスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスを、セミコロンで区切って指定できます。 通常は`IS::RootPath`と同じ値に設定します。

## PS::svgProvider.SVGFileSizeLimit - SVGファイルの最大サイズ {#section-b9c81e3e104642ebbdd9f000843d3256}

SVGソースファイルの最大サイズ(kBytes)。 この制限を超えるSVGファイルのレンダリングを試みると、サーバーはエラーを返します。 デフォルトは1024 KBです。

## IS::SvgMAxRenderRgnPixels - SVG出力画像サイズの制限 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRenderで生成できる画像のサイズを制限します。 0より大きい整数値（百万ピクセル単位）。 レンダリング操作がサイズ制限を超える場合、エラーが返されます。 初期設定は 4。

## PS::svgProvider.port — プラットフォームサーバーのリスニングポート {#section-f7e42a96c2dd4523b46f0557c239e659}

SVGレンダリングに埋め込む画像をPlatform Serverから取得するためにSvgRenderで使用されるポート。

重要SVGRenderコンポーネントを正しく機能させるには、この設定オプションを`TC::PsPort`と同じ値に設定する必要があります。

## PS::svgProvider.fontRoot - SVGフォントファイルフォルダ {#section-a8d45b0d68504945b8780f5eac351b0d}

SVGテキストのレンダリングに必要なフォントファイルをSvgRenderが検索する場所を指定します。通常、`IS::RootPaths`で指定されたパスの1つ。 初期設定は[!DNL *[!DNL install_folder]*/images]です。

## SVG::SVGRender.port, IS::SVGTcpPort - SVG通信ポート {#section-608687123aa644b7b58fe42385d71b79}

Image ServerとSVGRenderコンポーネントが通信するポートを設定します。

>[!NOTE]
>
>SVGRenderコンポーネントを正しく機能させるには、`SVG::SVGRender.port`と`IS::SVGTcpPort`に同じポート番号を指定する必要があります。
