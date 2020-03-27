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

---


# メタデータフィールドの種類{#metadata-field-types}

MetadataField/type、saveMetadataFieldParam/fieldTypeおよびcreateMetadataField/fieldTypeで使用されます。

構文

## 値 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:との値に初期化さ [!DNL `SingleFixedTag`] れた変更不可能なディクショナリを使用する場合の [!DNL `True`] 特例で [!DNL `False`]す。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:閉じたディクショナリから0個以上の文字列値。 辞書を変更できるのは管理者ユーザーのみです。
* [!DNL `MultiTag`]:0個以上の文字列値。
* [!DNL `SingleFixedTag`]:閉じたディクショナリからの単一の文字列値。 また `setAssetMetadata` はが `batchSetAssetMetadata` ディクショナリにない値で呼び出された場合、エラーが返されます。 辞書を変更できるのは管理者ユーザーのみです。

* [!DNL `SingleTag`]:任意の1つの文字列値。
* [!DNL `String`]

