---
description: アセットに関する検索文字列、キーワード、およびその他の情報を取得します。 応答には、アセットに関する追加情報が含まれています。
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

アセットに関する検索文字列、キーワード、およびその他の情報を取得します。 応答には、アセットに関する追加情報が含まれています。

構文

## 認証済みユーザータイプ {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-c1efda4bb15349a68b276bafee8c18fd}

**入力 (getSearchStringsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に対する取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットを処理します。 |

**出力 (getSearchStringsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | はい | アセット検索文字列の配列。 |

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
