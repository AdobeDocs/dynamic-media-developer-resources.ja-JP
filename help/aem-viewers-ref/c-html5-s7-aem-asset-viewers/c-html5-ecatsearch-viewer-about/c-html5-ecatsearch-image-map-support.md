---
description: eCatalog検索ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされています。
seo-description: eCatalog検索ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされています。
seo-title: 画像マップのサポート
solution: Experience Manager
title: 画像マップのサポート
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像マップのサポート{#image-map-support}

eCatalog検索ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされています。

マップアイコンの外観は、画像マップエフェクトの説明に従ってCSS [で制御します](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)。

画像マップは、次の3つの操作のいずれかを実行します。外部Webページ、情報パネルのポップアップのアクティブ化、内部ハイパーリンクにリダイレクトします。

## 外部Webページにリダイレクトする {#section-32ebe3c3a7f74892a428c5d48801de4d}

画像マ `href` ップの属性に、外部リソースへのURLが含まれています。このURLは、明示的に指定されるか、サポートされているJavaScriptテンプレート関数の1つに含まれます。 `loadProduct()`、、 `loadProductCW()`および `loadProductPW()`。

次に、単純なURLリダイレクトの例を示します。

`href=http://www.adobe.com`

この例では、同じURLが関数で囲まれてい `loadProduct()` ます。

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

Be aware that when you add the JavaScript code into the `HREF` attribute of your image map, the code is run on the client’s computer. したがって、JavaScriptコードが安全であることを確認してください。

## 情報パネルポップアップの有効化 {#section-7aa036420af646d1ad8cdc388add0b57}

情報パネルを操作するために、画像マップに属性が設定さ `ROLLOVER_KEY` れています。 また、属性を同時に設 `href` 定します。設定しないと、外部URLの処理が情報パネルのポップアップのアクティブ化に干渉します。

最後に、ビューアの設定に、およびオプションでパラメータに適した値が含ま `InfoPanelPopup.template` れていることを確認し `InfoPanelPopup.infoServerUrl` ます。

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTMLコードとJavaScriptコードがクライアントのコンピューター上で実行されることに注意してください。 したがって、このようなHTMLコードとJavaScriptコードが安全であることを確認してください。

## 内部ハイパーリンク {#section-6afa4fb2fe564c429e0201f019a95849}

画像マップをクリックすると、ビューア内で内部ページの入れ替えが実行されます。 この機能を使用するために、画像マ `href` ップの属性は次の特殊な形式を持ちます。

` href=target: *`idx`*`

idxは ` *``*` 、カタログ見開きの0を基準とするインデックスです。

eCatalog内の3D見開きを指 `href` す画像マップの属性の例を次に示します。

`href=target:2`
