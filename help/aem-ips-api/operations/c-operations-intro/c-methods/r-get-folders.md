---
description: フォルダーパスで始まる、すべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダーを返します。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 8%

---

# getFolders{#getfolders}

フォルダーパスで始まる、すべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダーを返します。

## フォルダーの目的 {#section-66e344d5333f42f1b060a0cba25935c3}

フォルダーを使用して、サブフォルダーとアセットを整理できます。 すべてのフォルダー名とアセット名は一意である必要があります。 同じ名前を共有するフォルダーやアセットは、異なるフォルダー階層にある場合でも名前空間の競合を引き起こします。
構文

## 許可されたユーザーの種類 {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
>ユーザーがフォルダーのデータを返すには、フォルダーへの読み取りアクセス権が必要です。

## パラメータ {#section-0c1976503eaa418a9226b51667901176}

**入力(getFoldersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の取っ手。 |
| `*`accessUserHandle`*` | `xsd:string` | いいえ | 管理者が特定のユーザーとして実行する際に使用します。 |
| `*`accessGroupHandle`*` | `xsd:string` | いいえ | 特定のグループでフィルターします。 |
| `*`folderPath`*` | `xsd:string` | いいえ | フォルダーとすべてのサブフォルダーをリーフレベルに取得するルートフォルダー。 除外された場合は、会社のルートが使用されます。 |
| `*`assetTypeArray`*` | `types:StringArray` | いいえ | 指定されたアセットタイプのみを含むフォルダーを返します。 |
| `*`responseFieldArray`*` | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| `*`excludeFieldArray`*` | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**出力(getFoldersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | いいえ | フィルター条件に一致するフォルダーの配列。 応答は、最大100,000個のフォルダーに制限されます。 |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## 例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

このコードのサンプルを使用すると、会社のすべてのフォルダーと、各フォルダーに関する特定の情報を含む配列が返されます。

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
