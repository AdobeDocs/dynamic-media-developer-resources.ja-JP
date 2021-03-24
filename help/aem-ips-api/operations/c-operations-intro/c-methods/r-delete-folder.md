---
description: フォルダを削除します。
solution: Experience Manager
title: deleteFolder
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 10%

---


# deleteFolder{#deletefolder}

フォルダを削除します。

構文

## 認証済みユーザータイプ{#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、フォルダーとそのすべての子に対する読み取りと削除のアクセス権を持っている必要があります。

## パラメータ {#section-a793c98a481a4f26ab50bc69b16b57e7}

**入力(deleteFolderParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | フォルダーが属する会社ーのハンドル。 |
| `*`folderHandle`*` | `xsd:string` | はい | 削除するフォルダーのハンドル。 |

**出力(deleteFolderParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9d4617b322e8442d80e59be0f8714841}

次のサンプルコードは、会社ーのルートからフォルダーを削除します。 フォルダーハンドルが必要です。このハンドルは、別の操作から取得する必要があります。

**リクエスト**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

なし
