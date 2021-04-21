---
description: プリロード画像は静的なアセットプレビュー画像で、init()メソッドを呼び出した直後に読み込まれ、ビューアSDKライブラリ、アセットおよびプリセット情報のダウンロード中に表示されます。 プリロード画像の目的は、ビューアの読み込み時間を視覚的に改善し、コンテンツをユーザに迅速に提示することです。
solution: Experience Manager
title: 画像のプリロード
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 画像をプリロード{#preload-image}

プリロード画像は静的なアセットプレビュー画像で、init()メソッドを呼び出した直後に読み込まれ、ビューアSDKライブラリ、アセットおよびプリセット情報のダウンロード中に表示されます。 プリロード画像の目的は、ビューアの読み込み時間を視覚的に改善し、コンテンツをユーザに迅速に提示することです。

プリロード画像は、最も一般的なビューア埋め込み方法（高さ無制限のレスポンシブ埋め込み）で適切に機能します。 見出し[高さ無制限のレスポンシブデザイン埋め込み](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)を参照してください。

ただし、他の埋め込みメソッドや特定の設定オプションを使用する場合、この機能には特定の制限があります。 プリロードイメージは、次の場合は正しくレンダリングされない場合があります。

* ビューアのサイズが固定されていて、サイズがビューアプリセットレコード内の`stagesize`設定属性を使用して定義されている場合、または最上位レベルのビューアコンテナ要素の外部ビューアCSSファイルで定義されている場合。
* 幅と高さが定義されたビューア埋め込みのフレキシブルサイズ埋め込みを使用する場合。 [幅と高さが定義されたフレキシブルサイズ埋め込み](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)を参照してください。

上記の操作モードの1つでビューアを使用する場合は、`preloadImage`設定属性を使用して画像のプリロード機能を無効にする必要があります。

また、設定で有効になっている場合でも、事前読み込み画像は使用されません。ビューアが`display:none` CSS設定を使用して非表示になるか、DOMツリーから切り離される場合は、DOM要素に埋め込みます。
