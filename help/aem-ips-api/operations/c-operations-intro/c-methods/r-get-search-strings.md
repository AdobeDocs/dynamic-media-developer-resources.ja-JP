---
description: アセットに関する検索文字列、キーワード、およびその他の情報を取得します。 応答には、アセットに関する追加情報が含まれます。
seo-description: アセットに関する検索文字列、キーワード、およびその他の情報を取得します。 応答には、アセットに関する追加情報が含まれます。
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Scene7 Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 14%

---


# getSearchStrings{#getsearchstrings}

アセットに関する検索文字列、キーワード、およびその他の情報を取得します。 応答には、アセットに関する追加情報が含まれます。

構文

## 認証済みユーザータイプ{#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-c1efda4bb15349a68b276bafee8c18fd}

**入力(getSearchStringsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | アセットのハンドル。 |

**出力(getSearchStringsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`searchStringArray`*` | `types:SearchStrings` | はい | アセット検索文字列の配列です。 |

## 例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

このコードサンプルは、アセット固有の検索文字列を返します。 応答は空の配列を返します。

**リクエスト**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**応答**

なし
