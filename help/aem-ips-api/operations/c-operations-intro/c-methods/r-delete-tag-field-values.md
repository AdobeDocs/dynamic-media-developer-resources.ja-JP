---
description: タグフィールドの辞書からタグフィールドの値を削除します。
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
TQID: 'https://experienceleague.adobe.com/SRTriQHWMLXJtkGeS-sCDZE3-1bu1TKNkKjxgESYOi4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 10%

---

# deleteTagFieldValues{#deletetagfieldvalues}

タグフィールドの辞書からタグフィールドの値を削除します。

## 承認済みユーザータイプ {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-5db64a6ae238426395bc760b83587260}

**入力（deleteTagFieldValuesParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| fieldHandle | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| valueArray | `types:StringArray` | はい | フィールドの辞書から削除するタグ値の配列。 |

**出力（deleteTagFieldValuesParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-92f9e575a6da491caa09e264b4d6ee55}

**リクエスト**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**応答**

なし
