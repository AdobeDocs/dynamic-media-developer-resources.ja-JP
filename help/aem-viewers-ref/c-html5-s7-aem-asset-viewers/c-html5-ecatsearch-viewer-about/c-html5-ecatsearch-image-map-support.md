---
description: eCatalog 検索ビューアは、メインビューの上にある画像マップアイコンのレンダリングをサポートしています。
solution: Experience Manager
title: 画像マップのサポート
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 画像マップのサポート{#image-map-support}

eCatalog 検索ビューアは、メインビューの上にある画像マップアイコンのレンダリングをサポートしています。

マップアイコンの外観は、[&#x200B; 画像マップエフェクト &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289) で説明されているように、CSS で制御されます。

画像マップは、外部 Web ページへのリダイレクト、情報パネルのポップアップのアクティブ化、内部ハイパーリンクの 3 つのアクションのいずれかを実行します。

## 外部 Web ページにリダイレクト {#section-32ebe3c3a7f74892a428c5d48801de4d}

画像マップの `href` 属性には、外部リソースへの URL が、明示的に指定されたか、サポートされているJavaScript テンプレート関数（`loadProduct()`、`loadProductCW()`、`loadProductPW()`）のいずれかにラップされています。

以下はシンプルな URL リダイレクトの例です。

`href=http://www.adobe.com`

この例では、同じ URL が `loadProduct()` 関数でラップされています。

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

JavaScript コードを画像マップの `HREF` 属性に追加すると、そのコードはクライアントのコンピューター上で実行されることに注意してください。 そのため、JavaScript コードが安全であることを確認してください。

## 情報パネルポップアップの有効化 {#section-7aa036420af646d1ad8cdc388add0b57}

情報パネルを操作するために、画像マップには `ROLLOVER_KEY` 属性が設定されています。 また、`href` 属性を同時に設定します。そうしないと、外部 URL 処理が情報パネルのポップアップアクティベーションに干渉します。

最後に、ビューア設定に、`InfoPanelPopup.template` パラメーターとオプションで `InfoPanelPopup.infoServerUrl` パラメーターの適切な値が含まれていることを確認してください。

>[!NOTE]
>
>情報パネルポップアップを設定する場合、情報パネルに渡されたHTML コードとJavaScript コードはクライアントのコンピューター上で実行されます。 そのため、このようなHTML コードとJavaScript コードが安全であることを確認してください。

## 内部ハイパーリンク {#section-6afa4fb2fe564c429e0201f019a95849}

画像マップをクリックすると、ビューア内で内部ページ入れ替えが実行されます。 この機能を使用するために、画像マップの `href` 属性には次のような特殊な形式があります。

` href=target: *`idx`*`

ここで、`*`idx`*` はカタログスプレッドのゼロベースのインデックスです。

次に、eCatalog 内の 3D スプレッドを指すイメージ マップの `href` 属性の例を示します。

`href=target:2`
