---
description: フォルダを作成します。
solution: Experience Manager
title: createFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 18%

---

# [!DNL createFolder]{#createfolder}

フォルダを作成します。

>[!NOTE]
>
>新しいフォルダは、 `/` をクリックして、会社のルートを示します。

構文

## 認証済みユーザータイプ {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、親フォルダーへの読み取り/書き込みアクセス権を持っている必要があります。

## パラメータ {#section-c00d8d89cf114886a535056f2a1bf892}

**入力 (createFolder)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い |
| folderPath | `xsd:string` | はい | フォルダとすべてのサブフォルダをリーフレベルで取得するために使用するルートフォルダ。 除外された場合は、会社のルートが使用されます。 |

**出力 (createFolderParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| folderHandle | `xsd:string` | はい | 新しいフォルダーのハンドル。 |

## 例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

このサンプルコードでは、会社のルートにフォルダーを作成します。 応答は、新しく作成されたフォルダーのハンドルを返します。

**リクエスト**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**応答**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
