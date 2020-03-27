---
description: フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダを返します。
seo-description: フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダを返します。
seo-title: getFolders
solution: Experience Manager
title: getFolders
topic: Scene7 Image Production System API
uuid: 06e9d745-b711-43e3-8dc6-93da66b981b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getFolders{#getfolders}

フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダを返します。

## フォルダの目的 {#section-66e344d5333f42f1b060a0cba25935c3}

フォルダを使用すると、サブフォルダとアセットを整理できます。 すべてのフォルダとアセット名は一意である必要があります。 同じ名前を共有するフォルダーとアセットは、異なるフォルダー階層にある場合でも、名前空間の競合の原因となります。
構文

## 認証されたユーザータイプ {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、フォルダー上のデータを返すために、フォルダーへの読み取りアクセス権を持っている必要があります。

## パラメータ {#section-0c1976503eaa418a9226b51667901176}

**Input (getFoldersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |
| ` *`accessUserHandle`*` | `xsd:string` | いいえ | 管理者が特定のユーザーを装うために使用します。 |
| ` *`accessGroupHandle`*` | `xsd:string` | いいえ | 特定のグループでフィルターします。 |
| ` *`folderPath`*` | `xsd:string` | いいえ | リーフレベルのフォルダーとすべてのサブフォルダーを取得するルートフォルダーです。 除外した場合は、会社のルートが使用されます。 |
| ` *`assetTypeArray`*` | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダを返します。 |
| ` *`responseFieldArray`*` | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| ` *`excludeFieldArray`*` | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**出力(getFoldersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`folderArray`*` | `types:FolderArray` | いいえ | フィルター条件に一致するフォルダーの配列です。 応答は最大100,000個のフォルダーに制限されます。 |
| ` *`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## 例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

このコードの例は、会社のすべてのフォルダと各フォルダに関する特定の情報を含む配列を返します。

**リクエスト**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**応答**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```

