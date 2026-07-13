---
description: 階層構造のツリー構造のフォルダーとサブフォルダーを返します。 getFolderTree応答は、最大100,000 フォルダーに制限されています
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
TQID: 'https://experienceleague.adobe.com/mQG2mkd1VPM1pKrzUr3L3dYCNb-N2-x0qu8B059CY90'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 262
ht-degree: 8%

---

# getFolderTree{#getfoldertree}

階層構造のツリー構造のフォルダーとサブフォルダーを返します。 getFolderTree応答は、最大100,000 フォルダーに制限されています

構文

## 承認済みユーザータイプ {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、フォルダーにデータを返すために、フォルダーへの読み取りアクセス権を持っている必要があります。

## パラメーター {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**入力（getFolderTreeParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |
| accessUserHandle | `xsd:string` | いいえ | 管理者が特定のユーザーになりすますために使用します。 |
| accessGroupHandle | `xsd:string` | いいえ | 特定のグループ（会社が属するものを含む）でフィルタリングするために使用されます。 |
| folderPath | `xsd:string` | いいえ | フォルダーとすべてのサブフォルダーをリーフレベルに取得するためのルートフォルダー。 除外した場合は、会社ルートが使用されます。 |
| 深さ | `xsd:int` | はい | 値が0の場合、最上位のフォルダーが取得されます。 その他の値は、ツリーに降下する深度を指定します。 |
| assetTypeArray | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダーを返します。 |
| responseFieldArray | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| excludeFieldArray | `types:StringArray` | いいえ | 応答で除外するフィールドのリストが含まれます。 |

**出力（getFolderTreeReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| フォルダ | `types:folders` | いいえ | ツリー構造内のフォルダーの階層。 応答は、最大100,000個のフォルダーに制限されています。 |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## 例 {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

このコードサンプルでは、企業ハンドルと深度パラメーターを使用して、応答が返す必要がある深度レベルを決定します。 応答には、関連するフォルダーとサブフォルダーの配列が含まれています。 フォルダーツリーをより深く検索するには、深度の値を小さい数値に設定します。

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

