---
description: フォルダを作成します。
seo-description: フォルダを作成します。
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: d64337d3ed7bd78c681c3022cda20012726d7ccc
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 20%

---


# [!DNL createFolder]{#createfolder}

フォルダを作成します。

>[!NOTE]
>
>会社のルートを示すフォルダを指定した場合でも、新しいフォルダはImagesフォルダ `/` の下位フォルダです。

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

**Input (createFolder)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社のハンドル |
| ` *`folderPath`*` | `xsd:string` | はい | リーフレベルのフォルダーとすべてのサブフォルダーを取得するために使用するルートフォルダーです。 除外した場合は、会社ルートが使用されます。 |

**出力(createFolderParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | はい | 新しいフォルダーのハンドル。 |

## 例 {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

次のサンプルコードは、会社ーのルートにフォルダーを作成します。 応答は、新しく作成されたフォルダーのハンドルを返します。

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

