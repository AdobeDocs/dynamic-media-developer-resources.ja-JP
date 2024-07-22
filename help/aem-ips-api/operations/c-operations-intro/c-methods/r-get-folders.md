---
description: フォルダーパスで始まるすべてのフォルダーとサブフォルダーを返します。 getFolders 応答は、最大 100,000 個のフォルダーを返します。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 7%

---

# getFolders{#getfolders}

フォルダーパスで始まるすべてのフォルダーとサブフォルダーを返します。 getFolders 応答は、最大 100,000 個のフォルダーを返します。

## フォルダーの目的 {#section-66e344d5333f42f1b060a0cba25935c3}

フォルダーを使用すると、サブフォルダーとアセットを整理できます。 すべてのフォルダー名とアセット名は一意である必要があります。 同じ名前を共有するフォルダーとアセットは、異なるフォルダー階層にある場合でも、名前空間の競合を引き起こします。
構文

## 許可されているユーザータイプ {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
>データを返すには、ユーザーにフォルダーへの読み取りアクセス権が必要です。

## パラメーター {#section-0c1976503eaa418a9226b51667901176}

**入力（getFoldersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社へのハンドル。 |
| accessUserHandle | `xsd:string` | いいえ | 管理者が特定のユーザーとして実行する場合に使用します。 |
| accessGroupHandle | `xsd:string` | いいえ | 特定のグループでフィルタリングします。 |
| folderPath | `xsd:string` | いいえ | フォルダーとリーフレベルまでのすべてのサブフォルダーを取得するルートフォルダー。 除外する場合は、会社ルートが使用されます。 |
| assetTypeArray | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダーを返します。 |
| responseFieldArray | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| excludeFieldArray | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**Output （getFoldersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderArray | `types:FolderArray` | いいえ | フィルター条件に一致するフォルダーの配列。 応答は、最大 100,000 フォルダーに制限されています。 |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## 例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

このコードサンプルでは、会社のすべてのフォルダーと各フォルダーに関する特定の情報を含んだ配列を返します。

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
