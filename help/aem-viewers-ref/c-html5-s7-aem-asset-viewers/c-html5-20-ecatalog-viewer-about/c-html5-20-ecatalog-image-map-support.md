---
title: 画像マップのサポート
description: eCatalog ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7a2a58f9-852e-4205-96bc-08332507b6cd
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 画像マップのサポート{#image-map-support}

eCatalog ビューアでは、メインビューの上にある画像マップアイコンのレンダリングがサポートされます。

マップアイコンの外観は、 [画像マップ効果](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-imagemapeffect.md#reference-261df27d1ed145c882b26b88e33a0289).

画像マップは、次の 3 つのアクションのいずれかを実行します。外部 Web ページ、情報パネルのポップアップのアクティベーション、内部ハイパーリンクにリダイレクトします。

## 外部 Web ページにリダイレクト {#section-32ebe3c3a7f74892a428c5d48801de4d}

この `href` 画像マップの属性に、外部リソースへの URL が含まれている（明示的に指定されているか、サポートされる次の JavaScript テンプレート関数の 1 つに含まれている）。 `loadProduct()`, `loadProductCW()`、および `loadProductPW()`.

単純な URL リダイレクトの例を次に示します。

`href=http://www.adobe.com`

この例では、同じ URL が `loadProduct()` 関数：

`href=javascript:loadProduct("http://www.adobe.com");void(0);`

JavaScript コードを `HREF` イメージマップの属性を指定すると、コードはクライアントのコンピューター上で実行されます。 そのため、JavaScript コードが安全であることを確認してください。

## 情報パネルポップアップのアクティベート {#section-7aa036420af646d1ad8cdc388add0b57}

情報パネルを操作するために、画像マップに `ROLLOVER_KEY` 属性セット。 また、 `href` 属性を使用しない場合は、外部 URL の処理が情報パネルのポップアップのアクティベーションに干渉します。

最後に、ビューア設定に、 `InfoPanelPopup.template` また、オプションで `InfoPanelPopup.infoServerUrl` パラメーター。

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されたHTMLコードおよび JavaScript コードがクライアントのコンピューターで実行されます。 そのため、このようなHTMLコードと JavaScript コードは必ず安全にしてください。

## 内部ハイパーリンク {#section-6afa4fb2fe564c429e0201f019a95849}

画像マップを選択すると、ビューア内で内部ページの入れ替えが実行されます。 この機能を使用するには、 `href` 画像マップの属性は、次の特殊な形式を持ちます。

` href=target: *`idx`*`

ここで、 `*`idx`*` は、カタログスプレッドの 0 を基準とするインデックスです。

次に、 `href` 属性は、eCatalog 内の 3D スプレッドを指す画像マップの場合は次のようになります。

`href=target:2`
