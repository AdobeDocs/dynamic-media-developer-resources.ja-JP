---
description: ズームターゲットを作成または編集します。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 20%

---

# saveZoomTarget{#savezoomtarget}

ズームターゲットを作成または編集します。

構文

## 認証済みユーザータイプ {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-4a23983cae4e49a098e9bbe736933996}

**入力(saveZoomTargetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 保存するズームターゲットを持つ会社のハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | ズームターゲットのハンドル。 |
| `*`zoomTargetHandle`*` | `xsd:string` | いいえ | ズームターゲットを編集または作成します。 |
| `*`name`*` | `xsd:string` | はい | ズームターゲット名 |
| `*`xPosition`*` | `xsd:int` | はい | 左ピクセルの場所。 |
| `*`yPosition`*` | `xsd:int` | はい | 上のピクセル位置。 |
| `*`width`*` | `xsd:int` | はい | ズームターゲットの幅 |
| `*`height`*` | `xsd:int` | はい | ズームターゲットの高さ |
| `*`ユーザデータ`*` | `xsd:string` | はい | 顧客固有の情報。 任意のタイプのデータを含めることができます。 |

**出力(saveZoomTargetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | はい | 新しく作成されたズームターゲットを処理します。 |

## 例 {#section-509c472c316549cdb228d7e1cfa8400a}

このコードサンプルを使用すると、ズームターゲットを保存できます。 応答は、ズームターゲットハンドルを返します。

**リクエスト**

```java
<saveZoomTargetParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <name>My Zoom Target</name>
   <xPosition>2</xPosition>
   <yPosition>2</yPosition>
   <width>10</width>
   <height>10</height>
   <userData>My User Data</userData>
</saveZoomTargetParam>
```

**応答**

```java
<saveZoomTargetReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <zoomTargetHandle>34194|9|301</zoomTargetHandle>
</saveZoomTargetReturn>
```
