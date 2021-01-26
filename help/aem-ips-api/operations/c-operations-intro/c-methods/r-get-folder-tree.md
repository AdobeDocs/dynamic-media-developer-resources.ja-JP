---
description: 階層ツリー構造のフォルダとサブフォルダを返します。 getFolderTreeの応答は、最大100,000個のフォルダーに制限されています
seo-description: 階層ツリー構造のフォルダとサブフォルダを返します。 getFolderTreeの応答は、最大100,000個のフォルダーに制限されています
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
topic: Dynamic Media Image Production System API
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 8%

---


# getFolderTree{#getfoldertree}

階層ツリー構造のフォルダとサブフォルダを返します。 getFolderTreeの応答は、最大100,000個のフォルダーに制限されています

構文

## 認証済みユーザータイプ{#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーがフォルダーにデータを返すには、フォルダーへの読み取りアクセス権が必要です。

## パラメータ {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**入力(getFolderTreeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`accessUserHandle`*` | `xsd:string` | いいえ | 管理者が特定のユーザーを装うためにのみ使用します。 |
| `*`accessGroupHandle`*` | `xsd:string` | いいえ | 会社が属するグループを含む、特定のグループでフィルターするために使用します。 |
| `*`folderPath`*` | `xsd:string` | いいえ | フォルダーとすべてのサブフォルダーをリーフレベルに取得するルートフォルダーです。 除外した場合は、会社ルートが使用されます。 |
| `*`深さ`*` | `xsd:int` | はい | 値が0の場合、最上位フォルダーが取得されます。 その他の値は、木に降りる深さを指定します。 |
| `*`assetTypeArray`*` | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダを返します。 |
| `*`responseFieldArray`*` | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| `*`excludeFieldArray`*` | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**出力(getFolderTreeReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`フォルダ`*` | `types:folders` | いいえ | ツリー構造内のフォルダの階層。 応答は最大100,000個のフォルダーに制限されます。 |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## 例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

このコードのサンプルでは、会社ハンドルと深さパラメーターを使用して、応答が返す深さのレベルを決定します。 応答には、関連するフォルダーとサブフォルダー配列が含まれます。 深さの値を小さい値に設定すると、フォルダツリーを深く探すことができます。

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

