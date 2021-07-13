---
description: ページラベルの管理
solution: Experience Manager
title: ページラベルの管理
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# ページラベルの管理{#managing-page-labels}

ビューアユーザーインターフェイスには、ページラベルが表示される場所が2つあります。サムネールモードと目次ドロップダウン

次の3つのタイプのラベルを定義できます。

* 作成者がSYMBOLローカライゼーションメカニズムを使用して定義するラベル。
* 作成者がバックエンドで(Dynamic Media Classic内で)定義したラベル。
* ビューアによって自動生成されるラベル。

シンボルベースのラベルは、`MediaSet.LABEL_XX[_YY]`シンボルと`MediaSet.LABEL_DELIM`シンボルを使用して定義されます。詳しくは、[ユーザインターフェイス要素のローカライゼーション](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)を参照してください。 このようなラベルは、eCatalog見開き全体に対して定義できます。この場合は、短いシンボル構文(`MediaSet.LABEL_XX`)を使用する必要があります。 または、完全なシンボル構文( `MediaSet.LABEL_XX_YY` )を使用して、各ページに個別に指定します。

eCatalog見開きの両方のページにラベルを定義すると、ビューアは`MediaSet.LABEL_DELIM`記号を使用してこれらのラベルを1つの文字列に連結します。 シンボルベースのラベルは、バックエンドで定義されたラベルや、ビューアによって自動生成されたラベルよりも優先されます。

Dynamic Media Classicで定義されたラベルは、個々のページ画像のUserDataレコードに保存されます。 シンボルベースのラベルと同じです。 eCatalog見開きの両方のページにラベルが定義されている場合、横置きモードで`MediaSet.LABEL_DELIM`記号を使用して連結されます。 Dynamic Media Classicラベルは、自動生成されたラベルよりも優先されますが、シンボルベースのラベルで上書きされます。

自動生成されるラベルは、eCatalog内のすべてのページに割り当てられる順次番号です。 シンボルベースのラベルが定義されている見開き、またはDynamic Media Classicのラベルが定義されている場合、自動生成されたラベルは無視されます。

目次では、`showdefault`パラメータを使用して自動生成されたラベルの表示を無効にすることができます。
