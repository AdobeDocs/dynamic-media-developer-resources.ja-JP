---
description: MetadataField/type、saveMetadataFieldParam/fieldType、およびcreateMetadataField/fieldTypeで使用されます。
solution: Experience Manager
title: メタデータフィールドタイプ
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
TQID: 'https://experienceleague.adobe.com/XFRmGmRc9iE5xmW0P2KfDzc-X-3TTrNYWkzNieSodQc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 2%

---

# メタデータフィールドタイプ{#metadata-field-types}

MetadataField/type、saveMetadataFieldParam/fieldType、およびcreateMetadataField/fieldTypeで使用されます。

構文

## 値 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]：値[!DNL `True`]と[!DNL `False`]に対して初期化された、変更不可能な辞書を持つ[!DNL `SingleFixedTag`]の特殊ケース。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]：閉じたディクショナリの0個以上の文字列値。 ディクショナリを変更できるのは管理者ユーザーのみです。
* [!DNL `MultiTag`]: 0個以上の文字列値。
* [!DNL `SingleFixedTag`]：閉じた辞書からの1つの文字列値。 ディクショナリにない値で`setAssetMetadata`または`batchSetAssetMetadata`が呼び出された場合、エラーが返されます。 ディクショナリを変更できるのは管理者ユーザーのみです。

* [!DNL `SingleTag`]：任意の1つの文字列値。
* [!DNL `String`]

