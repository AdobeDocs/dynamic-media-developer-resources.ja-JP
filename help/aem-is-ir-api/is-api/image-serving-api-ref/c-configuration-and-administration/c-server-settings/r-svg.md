---
description: この節の設定は、SVGのレンダリングが必要な場合にのみ考慮する必要があります。
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# SVG{#svg}

この節の設定は、SVGのレンダリングが必要な場合にのみ考慮する必要があります。

## SV::SvgHeapSize -SVGのヒープサイズ {#section-59ab17681daa4be8b5d794713e1a504e}

SVGレンダラーの Java ヒープサイズ。 デフォルトは「200m」（200M バイト）です。

## PS::svgProvider.rootPaths -SVGデータのルートフォルダ {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVGソースデータファイルの場所。 ファイルの絶対パスまたはファイルの相対パスを指定できます。 *[!DNL install_folder]*&#x200B;セミコロンで区切られます。 通常、次と同じ値に設定： `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit — 最大SVGファイルサイズ {#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG・ソース・ファイル・サイズ (kBytes)。 この制限を超えるSVGファイルのレンダリングを試みると、サーバーはエラーを返します。 デフォルトは 1024 KB です。

## IS::SvgMAxRenderRgnPixels -SVG出力画像サイズの制限 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRender で生成できる画像のサイズを制限します。 0 より大きい整数値（100 万ピクセル単位） レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 初期設定は 4。

## PS::svgProvider.port - [!DNL Platform Server] リスニングポート {#section-f7e42a96c2dd4523b46f0557c239e659}

SvgRender が画像を取得するために [!DNL Platform Server] 埋め込まれるSVG。

重要 SVGRender コンポーネントを正しく機能させるには、この設定オプションを `TC::PsPort`.

## PS::svgProvider.fontRoot -SVGフォントファイルフォルダ {#section-a8d45b0d68504945b8780f5eac351b0d}

SvgRender がSVG・テキストのレンダリングに必要なフォント・ファイルを検索する場所を指定します。通常、 `IS::RootPaths`. デフォルトは [!DNL  *[!DNL install_folder]*/images] と入力します。

## SVG::SVGRender.port, IS::SVGTcpPort -SVG通信ポート {#section-608687123aa644b7b58fe42385d71b79}

Image Server と SVGRender コンポーネントが通信するポートを設定します。

>[!NOTE]
>
>SVGRender コンポーネントを正しく機能させるには、同じポート番号を `SVG::SVGRender.port` および `IS::SVGTcpPort`.
