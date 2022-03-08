---
description: フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders 応答は、最大 100,000 個のフォルダーを返します。
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# getFolders{#getfolders}

フォルダーパスから始まるすべてのフォルダーとサブフォルダーを返します。 getFolders 応答は、最大 100,000 個のフォルダーを返します。

## フォルダーの目的 {#section-66e344d5333f42f1b060a0cba25935c3}

フォルダーを使用して、サブフォルダーとアセットを整理できます。 すべてのフォルダーとアセット名は一意である必要があります。 同じ名前を共有するフォルダーやアセットは、異なるフォルダー階層にある場合でも、名前空間の競合を引き起こします。
構文

## 認証済みユーザータイプ {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
>ユーザーがフォルダーのデータを返すには、そのフォルダーへの読み取りアクセス権が必要です。

## パラメータ {#section-0c1976503eaa418a9226b51667901176}

**入力 (getFoldersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| accessUserHandle | `xsd:string` | いいえ | 管理者が特定のユーザーを装うために使用します。 |
| accessGroupHandle | `xsd:string` | いいえ | 特定のグループでフィルターします。 |
| folderPath | `xsd:string` | いいえ | フォルダとすべてのサブフォルダをリーフレベルで取得するルートフォルダ。 除外された場合は、会社のルートが使用されます。 |
| assetTypeArray | `types:StringArray` | いいえ | 指定されたアセットタイプのみを含むフォルダーを返します。 |
| responseFieldArray | `types:StringArray` | いいえ | 応答に含めるフィールドのリストが含まれます。 |
| excludeFieldArray | `types:StringArray` | いいえ | 応答から除外するフィールドのリストが含まれます。 |

**出力 (getFoldersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderArray | `types:FolderArray` | いいえ | フィルター条件に一致するフォルダーの配列。 応答は最大 100,000 個のフォルダーに制限されます。 |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

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
