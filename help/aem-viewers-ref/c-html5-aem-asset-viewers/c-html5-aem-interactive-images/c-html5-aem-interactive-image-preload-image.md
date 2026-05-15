---
title: プリロード画像
description: Preload imageは、init （） メソッドを呼び出した直後に読み込まれる静的なアセットプレビューイメージです。Viewer SDK ライブラリ、アセット、プリセット情報がダウンロードされている間に表示されます。 プリロード画像の目的は、ビューアの読み込み時間を視覚的に改善し、コンテンツをユーザに迅速に提示することである。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
TQID: 'https://experienceleague.adobe.com/GlTbkyDeUNGf4gjmEEGbh1NaQ-nOgPZLtrz9kH4eK7o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 0%

---

# プリロード画像{#preload-image}

Preload imageは、init （） メソッドを呼び出した直後に読み込まれる静的なアセットプレビューイメージです。Viewer SDK ライブラリ、アセット、プリセット情報がダウンロードされている間に表示されます。 プリロード画像の目的は、ビューアの読み込み時間を視覚的に改善し、コンテンツをユーザに迅速に提示することである。

プリロード画像は、最も一般的なビューアの埋め込み方法（高さ制限のないレスポンシブ埋め込み）に適しています。 見出し[無制限の高さを持つレスポンシブデザイン埋め込み](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)を参照してください。

ただし、他の埋め込み方法や特定の設定オプションを使用する場合、この機能には一定の制限があります。 次の場合、プリロード画像が適切にレンダリングされないことがあります。

* ビューアがサイズで固定され、サイズがビューアプリセットレコード内の`stagesize`設定属性を使用して定義されている場合。 または、最上位のビューアコンテナ要素に外部ビューア CSS ファイルを使用します。
* 幅と高さが定義されたビューア埋め込み方法でフレキシブルサイズ埋め込みを使用する場合。 見出し[幅と高さが定義された柔軟なサイズ埋め込みを参照してください](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435)。

上記のいずれかの操作モードでビューアを使用している場合は、`preloadImage`構成属性を使用して画像のプリロード機能を無効にします。

また、プリロード画像は、設定で有効になっている場合でも使用されません。ビューアがDOM要素に埋め込まれている場合は、`display:none` CSS設定を使用して非表示にするか、DOM ツリーから切り離します。
