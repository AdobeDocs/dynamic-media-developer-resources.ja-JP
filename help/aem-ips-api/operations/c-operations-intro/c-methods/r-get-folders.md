---
description: フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000 フォルダーを返します。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
TQID: 'https://experienceleague.adobe.com/155R9mUWjM5flIW9EdpyaxGIlyiCjWOubs90otdHgQ8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 7%

---

# getFolders{#getfolders}

フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders応答は、最大100,000 フォルダーを返します。

## フォルダーの目的 {#section-66e344d5333f42f1b060a0cba25935c3}

フォルダーを使用すると、サブフォルダーとアセットを整理できます。 フォルダー名とアセット名はすべて一意である必要があります。 同じ名前を共有するフォルダーとアセットは、異なるフォルダー階層にある場合でも、名前空間の競合を引き起こします。構文

## 承認済みユーザータイプ {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
>ユーザーは、フォルダーにデータを返すために、フォルダーへの読み取りアクセス権を持っている必要があります。

## パラメーター {#section-0c1976503eaa418a9226b51667901176}

**入力（getFoldersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドルです。 |
| accessUserHandle | `xsd:string` | いいえ | 管理者が特定のユーザーを偽装するために使用します。 |
| accessGroupHandle | `xsd:string` | いいえ | 特定のグループでフィルタリングします。 |
| folderPath | `xsd:string` | いいえ | フォルダーとすべてのサブフォルダーをリーフレベルに取得するためのルートフォルダー。 除外した場合は、会社ルートが使用されます。 |
| assetTypeArray | `types:StringArray` | いいえ | 指定したアセットタイプのみを含むフォルダーを返します。 |
| responseFieldArray | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| excludeFieldArray | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**出力（getFoldersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderArray | `types:FolderArray` | いいえ | フィルター条件に一致するフォルダーの配列。 応答は、最大100,000 フォルダーに制限されています。 |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## 例 {#section-b5cb06e9fb9945ad898dbdc3692b754e}

このコードサンプルは、会社のすべてのフォルダーと、各フォルダーに関する特定の情報を含む配列を返します。

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

