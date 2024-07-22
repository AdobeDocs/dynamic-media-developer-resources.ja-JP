---
description: ズームターゲットの作成または編集。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 18%

---

# saveZoomTarget{#savezoomtarget}

ズームターゲットの作成または編集。

構文

## 許可されているユーザータイプ {#section-823cd9f0557045bca51da66768b5ba74}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-4a23983cae4e49a098e9bbe736933996}

**入力（saveZoomTargetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ズームターゲットを保存する会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | ズームターゲットのハンドル。 |
| zoom ターゲット ハンドル | `xsd:string` | いいえ | ズームターゲットを編集または作成します。 |
| name | `xsd:string` | はい | ズームターゲット名。 |
| x 位置 | `xsd:int` | はい | 左ピクセルの位置。 |
| yPosition | `xsd:int` | はい | 上位のピクセルの場所。 |
| 幅 | `xsd:int` | はい | ズームターゲットの幅。 |
| 高さ | `xsd:int` | はい | ズームターゲットの高さ。 |
| userData | `xsd:string` | はい | お客様固有の情報 任意のタイプのデータを含めることができます。 |

**出力（saveZoomTargetReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| zoom ターゲット ハンドル | `xsd:string` | はい | 新しく作成されたズームターゲットへのハンドル。 |

## 例 {#section-509c472c316549cdb228d7e1cfa8400a}

このコードサンプルでは、ズームターゲットを保存します。 応答は、ズームターゲットハンドルを返します。

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
