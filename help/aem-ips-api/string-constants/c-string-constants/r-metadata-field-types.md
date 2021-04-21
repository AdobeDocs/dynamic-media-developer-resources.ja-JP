---
description: MetadataField/type、saveMetadataFieldParam/fieldTypeおよびcreateMetadataField/fieldTypeで使用されます。
solution: Experience Manager
title: メタデータフィールドの種類
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# メタデータフィールドの種類{#metadata-field-types}

MetadataField/type、saveMetadataFieldParam/fieldTypeおよびcreateMetadataField/fieldTypeで使用されます。

構文

## 値 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:との特殊なケースで、値 [!DNL `SingleFixedTag`] とに初期化された変更不可のディクショナリを [!DNL `True`] 使用し [!DNL `False`]ます。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:閉じたディクショナリから0個以上の文字列値を取得します。辞書を変更できるのは管理者ユーザーのみです。
* [!DNL `MultiTag`]:0個以上の文字列値。
* [!DNL `SingleFixedTag`]:閉じたディクショナリからの単一の文字列値。`setAssetMetadata`または`batchSetAssetMetadata`が、ディクショナリにない値で呼び出されると、エラーが返されます。 辞書を変更できるのは管理者ユーザーのみです。

* [!DNL `SingleTag`]:任意の1つの文字列値。
* [!DNL `String`]

