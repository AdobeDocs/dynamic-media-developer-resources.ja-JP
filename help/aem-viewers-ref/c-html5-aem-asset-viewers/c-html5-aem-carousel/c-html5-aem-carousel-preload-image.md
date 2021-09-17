---
title: 画像のプリロード
description: プリロード画像は、 init()メソッドを呼び出した直後に読み込まれ、ビューアSDKライブラリ、アセットおよびプリセット情報のダウンロード中に表示される静的なアセットプレビュー画像です。 プリロード画像の目的は、視覚的にビューアの読み込み時間を改善し、ユーザに対して迅速にコンテンツを提示することです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 画像のプリロード{#preload-image}

プリロード画像は、 init()メソッドを呼び出した直後に読み込まれ、ビューアSDKライブラリ、アセットおよびプリセット情報のダウンロード中に表示される静的なアセットプレビュー画像です。 プリロード画像の目的は、視覚的にビューアの読み込み時間を改善し、ユーザに対して迅速にコンテンツを提示することです。

プリロード画像は、最も一般的なビューア埋め込み方法（高さ無制限のレスポンシブ埋め込み）に適しています。 見出し[高さ無制限のレスポンシブデザイン埋め込み](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e)を参照してください。

ただし、この機能には、他の埋め込み方法や特定の設定オプションを使用する場合に一定の制限があります。 次の場合に、イメージのプリロードが正しくレンダリングされない可能性があります。

* ビューアのサイズを固定し、サイズを定義する場合は、ビューアプリセットレコード内の`stagesize`設定属性を使用するか、最上位ビューアのコンテナ要素用の外部ビューアのCSSファイルを使用します。
* ビューア埋め込みの幅と高さが定義された方法でフレキシブルサイズ埋め込みを使用する場合。 [幅と高さを定義したフレキシブルサイズ埋め込み](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)を参照してください。

上記の操作モードのいずれかでビューアを使用する場合は、 `preloadImage`設定属性を使用して、プリロード画像機能を無効にします。

また、設定でビューアがDOM要素に埋め込まれている場合、CSS設定を使用して非表示になっているか、DOMツリーから切り離されている場合でも、プリロード画像は使用されません。`display:none`
