---
description: 'null'
seo-description: 'null'
seo-title: ページラベルの管理
solution: Experience Manager
title: ページラベルの管理
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ページラベルの管理{#managing-page-labels}

ビューアのユーザインターフェイスでは、ページラベルが表示される場所は2つあります。サムネールモードと目次のドロップダウン

定義できるラベルには3種類あります。

* 作成者がシンボルローカリゼーションメカニズムを使用して定義するラベル。
* SPS内のバックエンドで作成者が定義したラベル。
* ビューアによって自動生成されるラベル。

シンボルベースのラベルは、ユーザインターフェイス要素のロ `MediaSet.LABEL_XX[_YY]` ーカリゼーションで説 `MediaSet.LABEL_DELIM` 明されているとおりに、お [よびシンボルを使用して定義されま](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)す。 このようなラベルは、eCatalog見開き全体に対して定義できます。定義する場合は、短いシンボル構文( `MediaSet.LABEL_XX`)を使用します。 または、完全なシンボル構文( `MediaSet.LABEL_XX_YY`)を使用して、各ページに対して個別に指定します。

eCatalog見開きの両方のページのラベルを定義すると、ビューアは、 `MediaSet.LABEL_DELIM` SYMBOLを使用して、これらのラベルを1つの文字列に連結します。 シンボルベースのラベルは、バックエンドで定義されたラベルや、ビューアによって自動生成されたラベルよりも優先されます。

SPSで定義されたラベルは、個々のページ画像のUserDataレコードに保存されます。 シンボルベースのラベルと同じです。 つまり、eCatalog見開きの両方のページにラベルが定義されている場合、ラベルは横置きモードの `MediaSet.LABEL_DELIM` SYMBOLを使用して連結されます。 SPSラベルは、自動生成されるラベルよりも優先されますが、シンボルベースのラベルによって上書きされます。

自動生成されるラベルは、eCatalog内のすべてのページに割り当てられる連番です。 シンボルベースのラベルが定義されているか、SPSラベルが定義されている場合、自動的に生成されたラベルは、指定された見開きに対して無視されます。

目次では、パラメータを使用して自動生成されたラベルの表示を無効にすることがで `showdefault` きます。
