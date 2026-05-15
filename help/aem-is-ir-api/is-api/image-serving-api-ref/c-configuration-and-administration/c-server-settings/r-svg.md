---
title: SVG
description: このセクションの設定は、SVG レンダリングが必要な場合にのみ考慮する必要があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
TQID: 'https://experienceleague.adobe.com/B9kyf-cEvz6A-IPoeY6jLzP4mUnGoG2ZjxAGKexdDpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# SVG{#svg}

このセクションの設定は、SVG レンダリングが必要な場合にのみ考慮する必要があります。

## SV::SvgHeapSize - SVG ヒープサイズ {#section-59ab17681daa4be8b5d794713e1a504e}

SVG レンダラーのJava ヒープサイズ。 デフォルトは「200 m」（200 MB）です。

## PS::svgProvider.rootPaths - SVG Data Root Folders {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG ソースデータファイルの場所。 1つ以上の絶対ファイルパスまたは&#x200B;*[!DNL install_folder]*&#x200B;に対する相対パスを、セミコロンで区切って指定できます。 通常は`IS::RootPath`と同じ値に設定されます。

## PS::svgProvider.SVGFileSizeLimit - SVG ファイルの最大サイズ {#section-b9c81e3e104642ebbdd9f000843d3256}

SVG ソースファイルの最大サイズ （k バイト単位）。 この制限を超えるSVG ファイルをレンダリングしようとすると、サーバーはエラーを返します。 デフォルトは1024 KBです。

## IS::SvgMAxRenderRgnPixels - SVG出力イメージ サイズの制限 {#section-5be1fd9639424d878a5ffd11736d3920}

SVGRenderが生成できる画像のサイズを制限します。 0を超える整数値（単位は百万ピクセル）。 レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 デフォルトは4です。

## PS::svgProvider.port - [!DNL Platform Server] リスニング ポート {#section-f7e42a96c2dd4523b46f0557c239e659}

SvgRenderで使用されるポートは、SVG レンダリングに埋め込むために[!DNL Platform Server]から画像を取得します。

重要SVGRender コンポーネントを正しく機能させるには、この設定オプションを`TC::PsPort`と同じ値に設定する必要があります。

## PS::svgProvider.fontRoot - SVG フォントファイルフォルダー {#section-a8d45b0d68504945b8780f5eac351b0d}

SvgRenderがSVG テキストのレンダリングに必要なフォントファイルを検索する場所を指定します。通常、`IS::RootPaths`で指定されたパスの1つです。 デフォルトは[!DNL *[!DNL install_folder]*/images]です。

## SVG::SVGRender.port, IS::SVGTcpPort - SVG Communications Port {#section-608687123aa644b7b58fe42385d71b79}

Image ServerとSVGRender コンポーネントが通信するポートを設定します。

>[!NOTE]
>
>SVGRender コンポーネントを正しく機能させるには、`SVG::SVGRender.port`と`IS::SVGTcpPort`に同じポート番号を指定する必要があります。
