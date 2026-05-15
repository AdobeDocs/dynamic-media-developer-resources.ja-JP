---
description: eCatalog Search Viewerでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされています。
solution: Experience Manager
title: 画像マップのサポート
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 58e7523f-1615-4da4-bb09-a995bf427bfc
TQID: 'https://experienceleague.adobe.com/NJMiADA-R6aTQyrhd-CCP8pGFY-rjcIRfxiQ-4cRmRk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 313
ht-degree: 0%

---

# 画像マップのサポート{#image-map-support}

eCatalog Search Viewerでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされています。

マップアイコンの表示は、[画像マップエフェクト ](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289)で説明されているように、CSSを使用して制御されます。

画像マップでは、外部web ページへのリダイレクト、情報パネルポップアップアクティベーション、内部ハイパーリンクの3つのアクションのいずれかを実行します。

## 外部web ページへのリダイレクト {#section-32ebe3c3a7f74892a428c5d48801de4d}

画像マップの`href`属性には、外部リソースへのURLが含まれています。これは、明示的に指定するか、サポートされているJavaScript テンプレート関数の1つにラップされます：`loadProduct()`、`loadProductCW()`、および`loadProductPW()`。

シンプルなURL リダイレクトの例を次に示します。

`href=http://www.adobe.com`

この例では、同じURLが`loadProduct()`関数でラップされています。

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

JavaScript コードを画像マップの`HREF`属性に追加すると、そのコードがクライアントのコンピューターで実行されることに注意してください。 したがって、JavaScript コードが安全であることを確認してください。

## 情報パネルのポップアップのアクティベーション {#section-7aa036420af646d1ad8cdc388add0b57}

情報パネルを操作するには、画像マップに`ROLLOVER_KEY`属性が設定されています。 また、同時に`href`属性を設定します。設定しない場合、外部URL処理によって情報パネルのポップアップアクティベーションが妨げられます。

最後に、ビューア設定に`InfoPanelPopup.template`およびオプションで`InfoPanelPopup.infoServerUrl` パラメーターの適切な値が含まれていることを確認します。

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTML コードとJavaScript コードがクライアントのコンピューターで実行されることに注意してください。 したがって、このようなHTML コードとJavaScript コードが安全であることを確認してください。

## 内部ハイパーリンク {#section-6afa4fb2fe564c429e0201f019a95849}

画像マップをクリックすると、ビューア内で内部ページスワップが実行されます。 この機能を使用するには、画像マップの`href`属性に次の特殊な形式があります。

` href=target: *`idx`*`

ここで、`*`idx`*`は、カタログ スプレッドのゼロ ベース インデックスです。

次に、eCatalogの3D スプレッドを指す画像マップの`href`属性の例を示します。

`href=target:2`
