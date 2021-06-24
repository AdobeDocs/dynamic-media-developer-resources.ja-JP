---
description: eCatalog検索ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされます。
solution: Experience Manager
title: 画像マップのサポート
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,Business Practitioner
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 画像マップのサポート{#image-map-support}

eCatalog検索ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされます。

マップアイコンの外観は、[画像マップ効果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)で説明されているように、CSSを通じて制御します。

画像マップは、次の3つのアクションのいずれかを実行します。外部Webページ、情報パネルのポップアップのアクティブ化、内部ハイパーリンクにリダイレクトします。

## 外部Webページにリダイレクト {#section-32ebe3c3a7f74892a428c5d48801de4d}

画像マップの`href`属性には、外部リソースへのURLが含まれ、明示的に指定されるか、サポートされるJavaScriptテンプレート関数の1つに含まれます。`loadProduct()`、`loadProductCW()`、および`loadProductPW()`。

単純なURLリダイレクトの例を次に示します。

`href=http://www.adobe.com`

この例では、同じURLが`loadProduct()`関数で囲まれます。

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

画像マップの`HREF`属性にJavaScriptコードを追加すると、そのコードはクライアントのコンピューター上で実行されます。 したがって、JavaScriptコードがセキュアであることを確認してください。

## 情報パネルポップアップのアクティブ化 {#section-7aa036420af646d1ad8cdc388add0b57}

情報パネルを操作するために、画像マップには`ROLLOVER_KEY`属性が設定されています。 また、`href`属性を同時に設定します。そうしないと、外部URL処理が情報パネルのポップアップのアクティブ化に干渉します。

最後に、ビューア設定に`InfoPanelPopup.template`パラメーターと`InfoPanelPopup.infoServerUrl`パラメーターの適切な値（オプション）が含まれていることを確認します。

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTMLコードとJavaScriptコードがクライアントのコンピューター上で実行されることに注意してください。 したがって、このようなHTMLコードとJavaScriptコードは必ず安全にしてください。

## 内部ハイパーリンク {#section-6afa4fb2fe564c429e0201f019a95849}

画像マップをクリックすると、ビューア内で内部ページの入れ替えが実行されます。 この機能を使用するには、画像マップ内の`href`属性は次の特殊な形式になります。

` href=target: *`idx`*`

ここで、`*`idx`*`は、カタログスプレッドの0を基準とするインデックスです。

次に、eCatalog内の3Dスプレッドを指す画像マップの`href`属性の例を示します。

`href=target:2`
