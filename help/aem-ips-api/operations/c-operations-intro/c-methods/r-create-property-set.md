---
description: プロパティセットは、プロパティセットタイプに応じて、さまざまなIPS オブジェクトにアタッチできるアプリケーション固有の名前と値のペアのセットです。 プロパティ セットの種類で、複数のセットをオブジェクトに添付することが許可されておらず（PropertySetType/allowMultipleisfalse）、オブジェクトに同じ種類の関連セットが既に含まれている場合、新しいセットが既存のセットに置き換えられます。
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
TQID: 'https://experienceleague.adobe.com/kMRKY0OQPDLsPpPDtTQpxwTBiBu3dco37mSxR7khfgg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 6%

---

# createPropertySet{#createpropertyset}

プロパティセットは、プロパティセットタイプに応じて、さまざまなIPS オブジェクトにアタッチできるアプリケーション固有の名前と値のペアのセットです。 プロパティ セットの種類で、複数のセットをオブジェクトに添付することが許可されておらず（PropertySetType/allowMultipleisfalse）、オブジェクトに同じ種類の関連セットが既に含まれている場合、新しいセットが既存のセットに置き換えられます。

構文

## 承認済みユーザータイプ {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-25258e75f5f3419bad165c797eb6cd8e}

**入力（createPropertySetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | プロパティセットタイプへのハンドル。 |
| primaryOwnerHandle | `xsd:string` | はい | プロパティセットのプライマリオーナーへのハンドル。 |
| secondaryOwnerHandle | `xsd:string` | いいえ | プロパティセットのセカンダリオーナーへのハンドル。 |
| propertyArray | `types:PropertyArray` | はい | プロパティの配列。 |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**出力（createPropertySetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| setHandle | `xsd:string` | はい | 新しいプロパティセットへのハンドル。 |

## 例 {#section-4e1f5b2883664bc88f590fcd253df22b}

このコード サンプルでは、プロパティの名前と値を含むプロパティ セットを作成します。 応答は、新しいプロパティセットへのハンドルを返します。

**リクエスト**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**応答**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```
