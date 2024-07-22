---
description: フォルダーとサブフォルダーを階層ツリー構造で返します。 getFolderTree 応答は最大 100,000 フォルダーに制限されています
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# getFolderTree{#getfoldertree}

フォルダーとサブフォルダーを階層ツリー構造で返します。 getFolderTree 応答は最大 100,000 フォルダーに制限されています

構文

## 許可されているユーザータイプ {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>データを返すには、ユーザーにフォルダーへの読み取りアクセス権が必要です。

## パラメーター {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**入力（getFolderTreeParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社へのハンドル。 |
| accessUserHandle | `xsd:string` | いいえ | 管理者が特定のユーザーとして実行する場合にのみ使用します。 |
| accessGroupHandle | `xsd:string` | いいえ | 会社が属するもののいずれかを含む、特定のグループでフィルタリングするために使用されます。 |
| folderPath | `xsd:string` | いいえ | フォルダーとリーフレベルまでのすべてのサブフォルダーを取得するルートフォルダー。 除外する場合は、会社ルートが使用されます。 |
| 深さ | `xsd:int` | はい | 値が 0 の場合は、最上位フォルダーを取得します。 その他の値は、ツリーに降りる深度を指定します。 |
| assetTypeArray | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダーを返します。 |
| responseFieldArray | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| excludeFieldArray | `types:StringArray` | いいえ | 応答で除外するフィールドのリストが含まれます。 |

**出力（getFolderTreeReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| フォルダ | `types:folders` | いいえ | ツリー構造におけるフォルダーの階層。 応答は最大 100,000 個のフォルダーに制限されます。 |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## 例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

このコードサンプルでは、会社ハンドルと depth パラメーターを使用して、応答が返す深度レベルを決定します。 応答には、関連するを持つフォルダーとサブフォルダー配列が含まれます。 深さの値を小さい数に設定すると、フォルダーツリーをさらに深く検索できます。

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
