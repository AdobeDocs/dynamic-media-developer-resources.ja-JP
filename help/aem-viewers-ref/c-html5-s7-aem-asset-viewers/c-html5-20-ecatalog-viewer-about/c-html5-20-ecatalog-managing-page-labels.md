---
title: ページラベルの管理
description: ページラベルの管理
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# ページラベルの管理{#managing-page-labels}

ビューアユーザーインターフェイスには、ページラベルを表示する場所が 2 つあります。サムネールモードと目次ドロップダウンです。

次の 3 種類のラベルを定義できます。

* SYMBOL ローカリゼーションメカニズムを使用して作成者が定義したラベル。
* Dynamic Media Classic内のバックエンドで作成者が定義したラベル。
* ビューアによって自動的に生成されたラベル。

シンボルベースのラベルは、`MediaSet.LABEL_XX[_YY]` ユーザーインターフェイス要素のローカライズ `MediaSet.LABEL_DELIM` で説明されているように、[&#x200B; および &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) のシンボルを使用して定義されます。 このようなラベルは、ecatalog スプレッド全体に対して定義できます。その場合は、短い SYMBOL 構文（`MediaSet.LABEL_XX`）を使用する必要があります。 または、完全な SYMBOL 構文（`MediaSet.LABEL_XX_YY`）を使用して、ページごとに個別に指定します。

ecatalog スプレッドで両方のページのラベルを定義すると、ビューアはこれらのラベルを SYMBOL を使用して 1 つの文字列に連結 `MediaSet.LABEL_DELIM` ます。 シンボルベースのラベルは、バックエンドで定義されたラベルや、ビューアで自動生成されたラベルよりも優先されます。

Dynamic Media Classicで定義されたラベルは、個々のページ画像の UserData レコードに保存されます。 シンボル ベースのラベルと同じです。 つまり、ecatalog スプレッドの両方のページにラベルが定義されている場合、横向きモードでは SYMBOL を使用 `MediaSet.LABEL_DELIM` て連結されます。 Dynamic Media Classic ラベルは、自動生成されたラベルよりも優先されますが、シンボル ベースのラベルによって上書きされます。

自動生成されたラベルは、カタログ内のすべてのページに割り当てられる連続番号です。 SYMBOL-based ラベルが定義されている場合、またはDynamic Media Classic ラベルが定義されている場合、自動生成されたラベルは指定されたスプレッドで無視されます。

目次では、パラメーターを使用して、自動生成されたラベルの表示を無効にするこ `showdefault` ができます。
