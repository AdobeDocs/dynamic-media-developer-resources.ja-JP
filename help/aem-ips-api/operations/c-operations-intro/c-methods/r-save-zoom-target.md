---
description: ズームターゲットを作成または編集します。
seo-description: ズームターゲットを作成または編集します。
seo-title: saveZoomTarget
solution: Experience Manager
title: saveZoomTarget
topic: Dynamic Media Image Production System API
uuid: 197f7a2a-39ea-41cc-8e3a-76f9fe1b37d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 20%

---


# saveZoomTarget{#savezoomtarget}

ズームターゲットを作成または編集します。

構文

## 認証済みユーザータイプ{#section-823cd9f0557045bca51da66768b5ba74}

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
| `*`companyHandle`*` | `xsd:string` | はい | 保存するズームターゲットを含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | ズームターゲットのハンドル。 |
| `*`zoomTargetHandle`*` | `xsd:string` | いいえ | ズームターゲットを編集または作成します。 |
| `*`name`*` | `xsd:string` | はい | ズームターゲット名 |
| `*`xPosition`*` | `xsd:int` | はい | 左ピクセルの位置 |
| `*`yPosition`*` | `xsd:int` | はい | 上部のピクセル位置。 |
| `*`width`*` | `xsd:int` | はい | ズームターゲットの幅 |
| `*`height`*` | `xsd:int` | はい | ズームターゲットの高さ |
| `*`ユーザデータ`*` | `xsd:string` | はい | 顧客固有の情報。 任意の種類のデータを含めることができます。 |

**出力(saveZoomTargetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`zoomTargetHandle`*` | `xsd:string` | はい | 新しく作成されたズームターゲットのハンドル |

## 例 {#section-509c472c316549cdb228d7e1cfa8400a}

このコードのサンプルを使用して、ズームターゲットを保存します。 応答は、ズームターゲットハンドルを返します。

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

