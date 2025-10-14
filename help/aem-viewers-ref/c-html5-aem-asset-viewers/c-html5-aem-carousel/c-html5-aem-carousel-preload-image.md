---
title: 画像をプリロード
description: プリロード画像は、init （） メソッドを呼び出した直後に読み込まれ、ビューアのSDK ライブラリ、アセット、プリセット情報のダウンロード中に表示される静的アセットプレビュー画像です。 プリロード画像の目的は、視聴者のロード時間を視覚的に改善し、コンテンツを迅速にユーザーに提示することです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8caf156f-d641-44e9-94f9-5ba3245061a3
source-git-commit: 4aaa77b1fb58b30b02ee15f6080169fa354d5907
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 画像をプリロード{#preload-image}

プリロード画像は、init （） メソッドを呼び出した直後に読み込まれ、ビューアのSDK ライブラリ、アセット、プリセット情報のダウンロード中に表示される静的アセットプレビュー画像です。 プリロード画像の目的は、視聴者のロード時間を視覚的に改善し、コンテンツを迅速にユーザーに提示することです。

プリロード画像は、最も一般的なビューアの埋め込み方法に適しています。これは、高さが制限されないレスポンシブ埋め込みです。 見出し [&#x200B; 無制限の高さを使用したレスポンシブデザインの埋め込み &#x200B;](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel.md#concept-b44f1df3c1c64d4e8b5565e7736bf95e) を参照してください。

ただし、他の埋め込み方法や特定の設定オプションを使用する場合、この機能には特定の制限があります。 次の場合、プリロード画像が正しくレンダリングされない可能性があります。

* ビューアのサイズが固定され、サイズがビューアプリセットレコード内の設定属性 `stagesize` 使用して、または最上位のビューアコンテナ要素の外部ビューア CSS ファイルで定義されている場合。
* ビューアの埋め込みの幅と高さを定義したメソッドでフレキシブルサイズの埋め込みを使用する場合。 見出し [&#x200B; 幅と高さを定義した柔軟なサイズの埋め込み &#x200B;](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435) を参照してください。

上記のいずれかの操作モードでビューアを使用する場合は、`preloadImage` の設定属性を使用して、画像のプリロード機能を無効にします。

また、ビューアが DOM 要素に埋め込まれている場合、ビューアが CSS 設定を使用して非表示になるか、DOM ツリーから切り離され `display:none` 場合、プリロード画像は設定で有効になっていても使用されません。
