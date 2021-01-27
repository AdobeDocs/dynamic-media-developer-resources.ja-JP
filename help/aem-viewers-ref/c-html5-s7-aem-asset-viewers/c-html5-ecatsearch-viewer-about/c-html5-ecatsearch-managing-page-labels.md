---
description: ページラベルの管理
solution: Experience Manager
title: ページラベルの管理
topic: Dynamic Media
uuid: 49444fe6-ef34-4e5b-a293-e23830a67b4d
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# ページラベルの管理{#managing-page-labels}

ビューアのユーザインターフェイスには、ページラベルが表示される場所が2つあります。サムネールモードと目次ドロップダウン

定義できるラベルには次の3つのタイプがあります。

* 作成者がシンボルローカライゼーションメカニズムを使用して定義するラベル。
* 作成者がバックエンド時に定義する、Dynamic Mediaクラシック内のラベル。
* ビューアによって自動生成されるラベル。

シンボルベースのラベルは、`MediaSet.LABEL_XX[_YY]`SYMBOLと`MediaSet.LABEL_DELIM` SYMBOLを使用して定義されます。これらのSYMBOLは、[ユーザインターフェイス要素のローカライゼーション](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)で説明されています。 このようなラベルは、eCatalog見開き全体に対して定義できます。定義する場合は、短いシンボル構文(`MediaSet.LABEL_XX`)を使用する必要があります。 または、完全なシンボル構文(`MediaSet.LABEL_XX_YY`)を使用して、各ページに対して個別に指定します。

eCatalog見開きの両方のページにラベルを定義する場合、ビューアでは、`MediaSet.LABEL_DELIM`記号を使用してこれらのラベルが1つの文字列に連結されます。 シンボルベースのラベルは、バックエンドで定義されたラベルや、ビューアによって自動的に生成されたラベルよりも優先されます。

Dynamic Mediaクラシックで定義されたラベルは、個々のページ画像のUserDataレコードに保存されます。 シンボルベースのラベルと同じです。 eCatalog見開きの両方のページにラベルが定義されている場合、ランドスケープモードでは`MediaSet.LABEL_DELIM`記号を使用してラベルが連結されます。 Dynamic Mediaクラシックのラベルは、自動生成されるラベルよりも優先されますが、シンボルベースのラベルによって上書きされます。

自動生成されるラベルは、eCatalog内のすべてのページに割り当てられる連番です。 シンボルベースのラベルが定義されているか、Dynamic Mediaクラシックのラベルが定義されている場合、自動的に生成されたラベルは、指定された見開きに対して無視されます。

目次では、`showdefault`パラメーターを使用して、自動生成されるラベルの表示を無効にすることができます。
