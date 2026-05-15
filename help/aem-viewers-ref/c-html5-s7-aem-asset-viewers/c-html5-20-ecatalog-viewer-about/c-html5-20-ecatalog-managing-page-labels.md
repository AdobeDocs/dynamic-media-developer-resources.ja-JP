---
title: ページラベルの管理
description: ページラベルの管理
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b62b5cb8-6100-4d0f-afd8-e6daa6ce6539
TQID: 'https://experienceleague.adobe.com/4obpyT4BrqGz9n8KXh5DRM6J7Cp-Zji7z6-zyDHpXMc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 0%

---

# ページラベルの管理{#managing-page-labels}

ビューアユーザーインターフェイスには、ページラベルが表示される場所が2つあります。サムネールモードと目次ドロップダウンです。

定義できるラベルには、次の3つのタイプがあります。

* SYMBOL ローカライゼーションメカニズムを使用して作成者が定義したラベル。
* Dynamic Media Classic内のバックエンドで、オーサーが定義したラベル。
* ビューアによって自動的に生成されたラベル。

SYMBOL ベースのラベルは、[&#x200B; ユーザーインターフェイス要素のローカライゼーション &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)で説明されているように、`MediaSet.LABEL_XX[_YY]`および`MediaSet.LABEL_DELIM`個のSYMBOLを使用して定義されます。 このようなラベルは、e カタログスプレッド全体に対して定義できます。この場合は、短いSYMBOL構文（`MediaSet.LABEL_XX`）を使用する必要があります。 または、完全なSYMBOL構文（`MediaSet.LABEL_XX_YY`）を使用して、ページごとに個別に指定します。

カタログ スプレッドの両方のページのラベルを定義すると、ビューアは`MediaSet.LABEL_DELIM` SYMBOLを使用して、これらのラベルを1つの文字列に連結します。 シンボルベースのラベルは、バックエンドで定義されたラベルや、ビューアによって自動生成されたラベルよりも優先されます。

Dynamic Media Classicで定義されたラベルは、個々のページ画像のUserData レコードに格納されます。 SYMBOL ベースのラベルと同じです。 つまり、e カタログスプレッドの両方のページにラベルが定義されている場合、横モードで`MediaSet.LABEL_DELIM` シンボルを使用して連結されます。 Dynamic Media Classic ラベルは、自動生成されたラベルよりも優先されますが、SYMBOL ベースのラベルによって上書きされます。

自動生成されたラベルは、カタログ内のすべてのページに割り当てられる連続番号です。 SYMBOL ベースのラベルが定義されている場合やDynamic Media Classic ラベルが定義されている場合、自動生成されたラベルは特定のスプレッドに対して無視されます。

目次では、`showdefault` パラメーターを使用して自動生成されたラベルの表示を無効にすることができます。
