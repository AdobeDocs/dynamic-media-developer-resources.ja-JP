---
description: フォルダーとサブフォルダーを階層ツリー構造で返します。 getFolderTreeの応答は、最大100,000個のフォルダーに制限されています
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---

# getFolderTree{#getfoldertree}

フォルダーとサブフォルダーを階層ツリー構造で返します。 getFolderTreeの応答は、最大100,000個のフォルダーに制限されています

構文

## 許可されたユーザーの種類 {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーがフォルダーのデータを返すには、フォルダーへの読み取りアクセス権が必要です。

## パラメータ {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**入力(getFolderTreeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |
| `*`accessUserHandle`*` | `xsd:string` | いいえ | 管理者のみが特定のユーザーとして実行する場合に使用します。 |
| `*`accessGroupHandle`*` | `xsd:string` | いいえ | 会社が属するグループを含む、特定のグループでフィルタリングするために使用します。 |
| `*`folderPath`*` | `xsd:string` | いいえ | フォルダーとすべてのサブフォルダーをリーフレベルに取得するルートフォルダー。 除外された場合は、会社のルートが使用されます。 |
| `*`深さ`*` | `xsd:int` | はい | 値が0の場合、最上位のフォルダーが取得されます。 その他の値は、ツリーに降りる深さを指定します。 |
| `*`assetTypeArray`*` | `types:StringArray` | いいえ | 指定されたアセットタイプのみを含むフォルダーを返します。 |
| `*`responseFieldArray`*` | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| `*`excludeFieldArray`*` | `types:StringArray` | いいえ | 応答で除外するフィールドのリストが含まれます。 |

**出力(getFolderTreeReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`フォルダ`*` | `types:folders` | いいえ | ツリー構造内のフォルダーの階層。 応答は最大100,000個のフォルダーに制限されます。 |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## 例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

このコードサンプルでは、会社のハンドルと深さパラメーターを使用して、応答が返す深さのレベルを決定します。 応答には、関連するフォルダーおよびサブフォルダー配列が含まれます。 深さの値を小さい数値に設定すると、フォルダーツリーの深さを検索できます。

**リクエスト**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**応答**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```
