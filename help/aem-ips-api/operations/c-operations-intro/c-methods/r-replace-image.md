---
description: 画像アセットの画像データを置き換えます。
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 15%

---

# replaceImage{#replaceimage}

画像アセットの画像データを置き換えます。

構文

## 認証済みユーザータイプ {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**入力 (replaceImageParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyName | `xsd:string` | はい | 置き換える画像を含む会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 置き換えるアセットのハンドル。 |
| urlModifier | `xsd:string` | はい | 新しい画像データを生成する Image Server コマンド。 |

**出力 (replaceImageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | 新しいアセットを処理します。 |

## 例 {#section-cebb93576bde4cb98cb27356ca66783b}

このコードサンプルを使用すると、画像を置き換えて、 `urlModifier` 置き換え時に Image Server が何の操作も行わないように指定するコマンドを使用します。

**リクエスト**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**応答**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
