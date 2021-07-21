---
description: MetadataField/type、saveMetadataFieldParam/fieldType、およびcreateMetadataField/fieldTypeで使用されます。
solution: Experience Manager
title: メタデータフィールドタイプ
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---

# メタデータフィールドタイプ{#metadata-field-types}

MetadataField/type、saveMetadataFieldParam/fieldType、およびcreateMetadataField/fieldTypeで使用されます。

構文

## 値 {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]:値とに初期化さ [!DNL `SingleFixedTag`] れた変更不可能な辞書を使用した場合の特 [!DNL `True`] 殊なケ [!DNL `False`]ース。

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]:閉じた辞書の文字列値が0個以上です。辞書を変更できるのは管理者ユーザーのみです。
* [!DNL `MultiTag`]:0個以上の文字列値。
* [!DNL `SingleFixedTag`]:閉じた辞書の単一の文字列値。`setAssetMetadata`または`batchSetAssetMetadata`が辞書にない値で呼び出されると、エラーが返されます。 辞書を変更できるのは管理者ユーザーのみです。

* [!DNL `SingleTag`]:任意の単一文字列値。
* [!DNL `String`]
