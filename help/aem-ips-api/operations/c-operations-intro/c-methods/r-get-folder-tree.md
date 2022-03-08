---
description: フォルダとサブフォルダを階層ツリー構造で返します。 getFolderTree の応答は最大 100,000 個のフォルダーに制限されています
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 9%

---

# getFolderTree{#getfoldertree}

フォルダとサブフォルダを階層ツリー構造で返します。 getFolderTree の応答は最大 100,000 個のフォルダーに制限されています

構文

## 認証済みユーザータイプ {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーがフォルダーのデータを返すには、そのフォルダーへの読み取りアクセス権が必要です。

## パラメータ {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**入力 (getFolderTreeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| accessUserHandle | `xsd:string` | いいえ | 管理者のみが、特定のユーザーを装う場合に使用します。 |
| accessGroupHandle | `xsd:string` | いいえ | 会社が属するグループを含む、特定のグループでフィルタリングするために使用されます。 |
| folderPath | `xsd:string` | いいえ | フォルダとすべてのサブフォルダをリーフレベルで取得するルートフォルダ。 除外された場合は、会社のルートが使用されます。 |
| 深さ | `xsd:int` | はい | 値が 0 の場合は、最上位のフォルダーを取得します。 その他の値は、ツリーに降りる深さを指定します。 |
| assetTypeArray | `types:StringArray` | いいえ | 指定されたアセットタイプのみを含むフォルダーを返します。 |
| responseFieldArray | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| excludeFieldArray | `types:StringArray` | いいえ | 応答で除外するフィールドのリストが含まれます。 |

**出力 (getFolderTreeReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| フォルダ | `types:folders` | いいえ | ツリー構造内のフォルダーの階層。 応答は最大 100,000 個のフォルダーに制限されます。 |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## 例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

このコードサンプルでは、会社のハンドルと深さパラメーターを使用して、応答が返す深さのレベルを決定します。 応答には、関連するフォルダーおよびサブフォルダー配列が含まれます。 フォルダーツリーの深さを検索するには、深さの値を小さく設定します。

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
