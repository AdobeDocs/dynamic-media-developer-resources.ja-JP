---
description: eCatalog検索ビューアでは、メイン表示の上にある画像マップアイコンのレンダリングがサポートされています。
seo-description: eCatalog検索ビューアでは、メイン表示の上にある画像マップアイコンのレンダリングがサポートされています。
seo-title: 画像マップのサポート
solution: Experience Manager
title: 画像マップのサポート
topic: Dynamic media
uuid: 22ba8168-b384-4eda-a147-ce8172cfed11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# 画像マップのサポート{#image-map-support}

eCatalog検索ビューアでは、メイン表示の上にある画像マップアイコンのレンダリングがサポートされています。

マップアイコンの外観は、[画像マップ効果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)で説明されているように、CSSを通じて制御されます。

画像マップは、次の3つの操作のいずれかを実行します。外部Webページ、情報パネルのポップアップアクティベーション、内部ハイパーリンクにリダイレクトします。

## 外部Webページにリダイレクト{#section-32ebe3c3a7f74892a428c5d48801de4d}

画像マップの`href`属性には、外部リソースへのURLが含まれます。このURLは、明示的に指定するか、サポートされているJavaScriptテンプレート関数の1つに含めます。`loadProduct()`、`loadProductCW()`、および`loadProductPW()`。

以下は、単純なURLリダイレクトの例です。

`href=http://www.adobe.com`

この例では、同じURLが`loadProduct()`関数で囲まれます。

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

画像マップの`HREF`属性にJavaScriptコードを追加すると、そのコードはクライアントのコンピューター上で実行されます。 したがって、JavaScriptコードが安全であることを確認してください。

## 情報パネルポップアップアクティベーション{#section-7aa036420af646d1ad8cdc388add0b57}

情報パネルを操作するために、画像マップには`ROLLOVER_KEY`属性が設定されています。 また、`href`属性を同時に設定します。そうしないと、外部URL処理が情報パネルポップアップアクティベーションに干渉します。

最後に、ビューア設定に`InfoPanelPopup.template`パラメーターと`InfoPanelPopup.infoServerUrl`パラメーターの適切な値が含まれていることを確認します。

>[!NOTE]
>
>情報パネルポップアップを設定する場合、情報パネルに渡されるHTMLコードとJavaScriptコードは、クライアントのコンピューター上で実行されます。 したがって、このようなHTMLコードとJavaScriptコードが安全であることを確認してください。

## 内部ハイパーリンク{#section-6afa4fb2fe564c429e0201f019a95849}

画像マップをクリックすると、ビューア内で内部ページの入れ替えが実行されます。 この機能を使用するために、画像マップの`href`属性は次の特殊な形式を持ちます。

` href=target: *`idx`*`

` *`idx`*`は、カタログ見開きの0を基準とするインデックスです。

eCatalog内の3D見開きを指す画像マップの`href`属性の例を次に示します。

`href=target:2`
