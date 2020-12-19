---
description: プロパティセットは、名前と値のペアのアプリケーション固有のセットで、プロパティセットの種類に応じてさまざまなIPSオブジェクトにアタッチできます。 プロパティセットの種類で、複数のセットを1つのオブジェクトにアタッチできない場合(PropertySetType/allowMultipleisfalse)、オブジェクトに同じ種類の関連セットが既に存在する場合は、新しいセットによって既存のセットが置き換えられます。
seo-description: プロパティセットは、名前と値のペアのアプリケーション固有のセットで、プロパティセットの種類に応じてさまざまなIPSオブジェクトにアタッチできます。 プロパティセットの種類で、複数のセットを1つのオブジェクトにアタッチできない場合(PropertySetType/allowMultipleisfalse)、オブジェクトに同じ種類の関連セットが既に存在する場合は、新しいセットによって既存のセットが置き換えられます。
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Scene7 Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 6%

---


# createPropertySet{#createpropertyset}

プロパティセットは、名前と値のペアのアプリケーション固有のセットで、プロパティセットの種類に応じてさまざまなIPSオブジェクトにアタッチできます。 プロパティセットの種類で、複数のセットを1つのオブジェクトにアタッチできない場合(PropertySetType/allowMultipleisfalse)、オブジェクトに同じ種類の関連セットが既に存在する場合は、新しいセットによって既存のセットが置き換えられます。

構文

## 認証済みユーザータイプ{#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-25258e75f5f3419bad165c797eb6cd8e}

**入力(createPropertySetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | はい | プロパティセットタイプのハンドル。 |
| ` *`primaryOwnerHandle`*` | `xsd:string` | はい | プロパティセットの主所有者へのハンドル。 |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | いいえ | プロパティセットのセカンダリ所有者へのハンドル。 |
| ` *`propertyArray`*` | `types:PropertyArray` | はい | プロパティの配列。 |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**出力(createPropertySetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | はい | 新しいプロパティセットへのハンドル。 |

## 例 {#section-4e1f5b2883664bc88f590fcd253df22b}

次のコードのサンプルを使用すると、プロパティの名前と値を含むプロパティセットを作成できます。 応答は、新しいプロパティセットにハンドルを返します。

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

