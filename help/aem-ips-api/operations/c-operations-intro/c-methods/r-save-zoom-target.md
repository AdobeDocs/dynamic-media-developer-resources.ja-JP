---
description: ズームターゲットを作成または編集します。
solution: Experience Manager
title: saveZoomTarget
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 595fd5c8-4e98-4c1a-b396-c8e170aaf454
TQID: 'https://experienceleague.adobe.com/rw-joRwkyumLI261ifPiWTeIgy4mvx-4MpgmaKcX5-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 18%

---

# saveZoomTarget{#savezoomtarget}

ズームターゲットを作成または編集します。

構文

## 承認済みユーザータイプ {#section-823cd9f0557045bca51da66768b5ba74}

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
| companyHandle | `xsd:string` | はい | 保存するズームターゲットを持つ会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | ズームターゲットへのハンドル。 |
| zoomTargetHandle | `xsd:string` | いいえ | ズームターゲットを編集または作成します。 |
| name | `xsd:string` | はい | ズームターゲット名。 |
| xPosition | `xsd:int` | はい | 左ピクセルの位置。 |
| yPosition | `xsd:int` | はい | 最上位のピクセルの場所： |
| 幅 | `xsd:int` | はい | ターゲット幅をズームします。 |
| 高さ | `xsd:int` | はい | ターゲットの高さをズームします。 |
| userData | `xsd:string` | はい | 固有の情報を受け取ることができます。 任意のタイプのデータを含めることができます。 |

**出力（saveZoomTargetReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| zoomTargetHandle | `xsd:string` | はい | 新しく作成したズームターゲットに対するハンドル。 |

## 例 {#section-509c472c316549cdb228d7e1cfa8400a}

このコードサンプルは、ズームターゲットを保存します。 応答は、ズームターゲットハンドルを返します。

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
