---
description: 会社からプロジェクトを削除します。 アセットとプロジェクトの間のリンクは壊れますが、アセットは IPS からは削除されません。
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 9%

---

# deleteProject{#deleteproject}

会社からプロジェクトを削除します。 アセットとプロジェクトの間のリンクは壊れますが、アセットは IPS からは削除されません。

構文

## 認証済みユーザータイプ {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-00d1e00dd5014513a52b4e6b4f61de62}

**入力 (deleteProjectParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyName | `xsd:string` | はい | プロジェクトに関連付けられている会社の名前。 |
| projectHandle | `xsd:string` | はい | 削除するプロジェクトへのハンドル。 |

**出力 (deleteProjectReturn)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-e38507f1f7ec41b9a625f47390490254}

このコードの例では、会社のハンドルとプロジェクトのハンドルを、プロジェクトを削除するために IPS Web サービスサーバーに送信される deleteProjectParam のフィールドとして使用します。

**リクエスト**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**応答**

なし
