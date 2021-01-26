---
description: フォルダーパスから開始する、すべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダを返します。
seo-description: フォルダーパスから開始する、すべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダを返します。
seo-title: getFolders
solution: Experience Manager
title: getFolders
topic: Dynamic Media Image Production System API
uuid: 06e9d745-b711-43e3-8dc6-93da66b981b1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 8%

---


# getFolders{#getfolders}

フォルダーパスから開始する、すべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000個のフォルダを返します。

## フォルダの目的{#section-66e344d5333f42f1b060a0cba25935c3}

フォルダーを使用すると、サブフォルダーとアセットを整理できます。 すべてのフォルダーとアセット名は一意である必要があります。 同じ名前を共有するフォルダーとアセットが、異なるフォルダー階層にある場合でも、名前空間の競合を引き起こします。
構文

## 認証済みユーザータイプ{#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
>ユーザーがフォルダーにデータを返すには、フォルダーへの読み取りアクセス権が必要です。

## パラメータ {#section-0c1976503eaa418a9226b51667901176}

**入力(getFoldersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`accessUserHandle`*` | `xsd:string` | いいえ | 管理者が特定のユーザーを装うために使用します。 |
| `*`accessGroupHandle`*` | `xsd:string` | いいえ | 特定のグループでフィルターします。 |
| `*`folderPath`*` | `xsd:string` | いいえ | フォルダーとすべてのサブフォルダーをリーフレベルに取得するルートフォルダーです。 除外した場合は、会社ルートが使用されます。 |
| `*`assetTypeArray`*` | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダを返します。 |
| `*`responseFieldArray`*` | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| `*`excludeFieldArray`*` | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**出力(getFoldersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | いいえ | フィルター条件に一致するフォルダーの配列です。 応答は最大100,000個のフォルダーに制限されます。 |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## 例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

次のコードの例は、会社のすべてのフォルダと各フォルダに関する特定の情報を含む配列を返します。

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

