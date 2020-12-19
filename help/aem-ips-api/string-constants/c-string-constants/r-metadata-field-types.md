---
description: MetadataField/type、saveMetadataFieldParam/fieldTypeおよびcreateMetadataField/fieldTypeで使用されます。
seo-description: MetadataField/type、saveMetadataFieldParam/fieldTypeおよびcreateMetadataField/fieldTypeで使用されます。
seo-title: メタデータフィールドの種類
solution: Experience Manager
title: メタデータフィールドの種類
topic: Scene7 Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '107'
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

