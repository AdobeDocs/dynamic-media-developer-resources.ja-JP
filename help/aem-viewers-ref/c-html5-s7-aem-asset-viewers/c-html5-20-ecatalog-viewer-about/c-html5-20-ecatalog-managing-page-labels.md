---
title: ページラベルの管理
description: ページラベルの管理
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ページラベルの管理{#managing-page-labels}

ビューアユーザーインターフェイスには、ページラベルが表示される場所が 2 つあります。サムネールモードと目次ドロップダウン。

次の 3 種類のラベルを定義できます。

* 作成者が SYMBOL ローカライゼーションメカニズムを使用して定義したラベル。
* 作成者がバックエンドのDynamic Media Classic内で定義したラベル。
* ビューアによって自動的に生成されるラベル。

シンボルベースのラベルは、 `MediaSet.LABEL_XX[_YY]` および `MediaSet.LABEL_DELIM` の説明に従って、SYMBOL を [ユーザーインターフェイス要素のローカライゼーション](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). このようなラベルは eCatalog 見開き全体に対して定義できます。この場合、短い SYMBOL 構文 ( `MediaSet.LABEL_XX`) をクリックします。 または、完全なシンボル構文 ( `MediaSet.LABEL_XX_YY`) をクリックします。

eCatalog 見開きの両方のページにラベルを定義すると、ビューアは、 `MediaSet.LABEL_DELIM` シンボル。 シンボルベースのラベルは、バックエンドで定義されたラベルや、ビューアによって自動的に生成されたラベルよりも優先されます。

Dynamic Media Classicで定義されたラベルは、個々のページ画像の UserData レコードに保存されます。 シンボルベースのラベルと同じです。 eCatalog 見開きの両方のページにラベルが定義されている場合、 `MediaSet.LABEL_DELIM` 横長モードのシンボル。 Dynamic Media Classicのラベルは、自動生成されたラベルよりも優先されますが、シンボルベースのラベルによって上書きされます。

自動生成されるラベルは、eCatalog 内のすべてのページに割り当てられる順番の番号です。 シンボルベースのラベルが定義されているか、Dynamic Media Classicのラベルが定義されている場合、指定された見開きに対して自動生成されたラベルは無視されます。

目次では、 `showdefault` パラメーター。
