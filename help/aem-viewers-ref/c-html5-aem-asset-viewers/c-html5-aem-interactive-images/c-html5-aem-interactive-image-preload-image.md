---
title: イメージのプリロード
description: プリロード画像は、init() メソッドを呼び出した直後に読み込まれ、ビューア SDK ライブラリ、アセット、プリセット情報のダウンロード中に表示される静的なアセットプレビュー画像です。 プリロード画像の目的は、視覚的にビューアの読み込み時間を改善し、ユーザに対して迅速にコンテンツを提示することです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 54bea5fc-916c-4a58-bc06-b726884d488a
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# イメージのプリロード{#preload-image}

プリロード画像は、init() メソッドを呼び出した直後に読み込まれ、ビューア SDK ライブラリ、アセット、プリセット情報のダウンロード中に表示される静的なアセットプレビュー画像です。 プリロード画像の目的は、視覚的にビューアの読み込み時間を改善し、ユーザに対して迅速にコンテンツを提示することです。

画像のプリロードは、最も一般的なビューア埋め込み方法（高さ無制限のレスポンシブ埋め込み）に適しています。 見出し [ 高さ無制限のレスポンシブデザイン埋め込み ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435) を参照してください。

ただし、この機能には、他の埋め込み方法や特定の設定オプションを使用する場合に一定の制限があります。 次の場合、イメージのプリロードが正しくレンダリングされないことがあります。

* ビューアのサイズを固定し、サイズをビューアプリセットレコード内の `stagesize` 設定属性を使用して定義する場合。 または、最上位のビューアのコンテナ要素に外部ビューアの CSS ファイルを使用します。
* ビューア埋め込みの幅と高さを定義した方法でフレキシブルサイズ埋め込みを使用する場合。 [ 幅と高さが定義されたフレキシブルサイズ埋め込み ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-images.md#section-6bb5d3c502544ad18a58eafe12a13435) を参照してください。

上記のいずれかの操作モードでビューアを使用している場合は、 `preloadImage` 設定属性を使用して画像機能のプリロードを無効にします。

また、設定で有効にしている場合でも、CSS 設定 `display:none` を使用してビューアを DOM 要素に埋め込んだり、DOM ツリーから切り離したりして非表示になっている場合は、プリロード画像は使用されません。
