---
description: MetadataField/type、saveMetadataFieldParam/fieldType、および createMetadataField/fieldType で使用されます。
solution: Experience Manager
title: メタデータフィールドタイプ
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# メタデータフィールドタイプ{#metadata-field-types}

MetadataField/type、saveMetadataFieldParam/fieldType、および createMetadataField/fieldType で使用されます。

構文

## 値 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:～の特例 [!DNL `SingleFixedTag`] 値に初期化された変更不可能な辞書を使用 [!DNL `True`] および [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:閉じた辞書から 0 個以上の文字列値を取得します。 辞書を変更できるのは管理者ユーザーのみです。
* [!DNL `MultiTag`]:0 個以上の文字列値。
* [!DNL `SingleFixedTag`]:閉じた辞書からの単一の文字列値。 If `setAssetMetadata` または `batchSetAssetMetadata` が辞書にない値で呼び出されると、フォルトが返されます。 辞書を変更できるのは管理者ユーザーのみです。

* [!DNL `SingleTag`]:任意の単一文字列値。
* [!DNL `String`]
