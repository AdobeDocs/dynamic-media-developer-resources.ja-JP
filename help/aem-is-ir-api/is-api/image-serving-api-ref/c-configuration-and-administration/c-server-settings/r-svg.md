---
description: この節の設定は、SVGレンダリングが必要な場合にのみ考慮する必要があります。
seo-description: この節の設定は、SVGレンダリングが必要な場合にのみ考慮する必要があります。
seo-title: SVG
solution: Experience Manager
title: SVG
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e69b150-46ac-480f-96db-afadccc40fe4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SVG{#svg}

この節の設定は、SVGレンダリングが必要な場合にのみ考慮する必要があります。

## SV::SvgHeapSize - SVGヒープサイズ {#section-59ab17681daa4be8b5d794713e1a504e}

SVGレンダラーのJavaヒープサイズ。 デフォルトは「200m」（200Mバイト）です。

## PS::svgProvider.rootPaths - SVGデータのルートフォルダー {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVGソースデータファイルの場所。 絶対ファイルパスまたはセミコロンで区切った相対パスを1つ *[!DNL install_folder]*&#x200B;以上指定できます。 通常はと同じ値に設定します `IS::RootPath`。

## PS::svgProvider.SVGFileSizeLimit - SVGファイルの最大サイズ {#section-b9c81e3e104642ebbdd9f000843d3256}

SVGソースファイルの最大サイズ(KB)。 この制限を超えるSVGファイルのレンダリングを試みると、サーバーはエラーを返します。 デフォルトは1024 KBです。

## IS::SvgMAxRenderRgnPixels - SVG出力画像サイズの制限 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRenderで生成できる画像のサイズを制限します。 0より大きい整数値（百万ピクセル単位）。 レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 初期設定は 4。

## PS::svgProvider.port — プラットフォームサーバーのリスニングポート {#section-f7e42a96c2dd4523b46f0557c239e659}

SVGレンダリングに埋め込むPlatform Serverから画像を取得するためにSvgRenderで使用されるポートです。

重要SVGRenderコンポーネントを正しく機能させるには、この設定オプションをと同じ値に設定する必要がありま `TC::PsPort`す。

## PS::svgProvider.fontRoot - SVGフォントファイルフォルダー {#section-a8d45b0d68504945b8780f5eac351b0d}

SVGテキストのレンダリングに必要なフォントファイルをSvgRenderが見つける場所を指定します。通常、で指定したパスの1つで `IS::RootPaths`す。 初期設定は[!DNL *[!DNL install_folder]*/images]です。

## SVG::SVGRender.port、IS::SVGTcpPort - SVG通信ポート {#section-608687123aa644b7b58fe42385d71b79}

Image ServerとSVGRenderコンポーネントが通信するポートを設定します。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>SVGRenderコンポーネントを正しく機能させるには、とに同じポート番号を指定する必要があ `SVG::SVGRender.port` りま `IS::SVGTcpPort`す。

