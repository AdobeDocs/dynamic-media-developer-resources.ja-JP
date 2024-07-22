---
description: プロパティ セットは、プロパティ セットの種類に応じて、さまざまな IPS オブジェクトにアタッチできる名前と値のペアのアプリケーション固有のセットです。 プロパティ セット タイプによって、オブジェクトに複数のセットをアタッチできない（PropertySetType/allowMultipleisfalse）状態で、オブジェクトに同じタイプのセットが既に関連付けられている場合は、新しいセットが既存のセットに置き換わります。
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# createPropertySet{#createpropertyset}

プロパティ セットは、プロパティ セットの種類に応じて、さまざまな IPS オブジェクトにアタッチできる名前と値のペアのアプリケーション固有のセットです。 プロパティ セット タイプによって、オブジェクトに複数のセットをアタッチできない（PropertySetType/allowMultipleisfalse）状態で、オブジェクトに同じタイプのセットが既に関連付けられている場合は、新しいセットが既存のセットに置き換わります。

構文

## 許可されているユーザータイプ {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-25258e75f5f3419bad165c797eb6cd8e}

**入力（createPropertySetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | プロパティセットタイプへのハンドル。 |
| primaryOwnerHandle | `xsd:string` | はい | プロパティ セットのプライマリ所有者へのハンドル。 |
| secondaryOwnerHandle | `xsd:string` | いいえ | プロパティ セットのセカンダリ所有者へのハンドル。 |
| propertyArray | `types:PropertyArray` | はい | プロパティの配列。 |
| permissionArray | `types:PermissionUpdateArray` |  |  |

**Output （createPropertySetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| setHandle | `xsd:string` | はい | 新しいプロパティ セットへのハンドル。 |

## 例 {#section-4e1f5b2883664bc88f590fcd253df22b}

このコード例では、プロパティの名前と値を含むプロパティセットを作成します。 応答は、新しいプロパティセットへのハンドルを返します。

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
