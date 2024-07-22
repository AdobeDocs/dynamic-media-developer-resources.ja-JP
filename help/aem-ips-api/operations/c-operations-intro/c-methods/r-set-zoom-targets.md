---
description: アセット画像に関連付けられたズームターゲットを設定します。 既存のズームターゲットを上書きします。
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 11%

---

# setZoomTargets{#setzoomtargets}

アセット画像に関連付けられたズームターゲットを設定します。 既存のズームターゲットを上書きします。

構文

## 認証済みユーザータイプ {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-161f8c733cc4439f94a06e12119d4226}

**入力（setZoomTargetsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| assetHandle | `xsd:string` | はい | 設定するズームターゲットを持つアセット。 |
| zoomTargetArray | `types:ZoomTargetDefinitionArray` | はい | ズームターゲット定義の配列。 |

**出力（setZoomTargetsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| zoomTargetHandleArray | `types:HandleArray` | はい | この操作によって作成されたズーム ターゲットへのハンドルのセットです。 |

## 例 {#section-a2f14c7a1499443e96d099ea8a76c182}

このコードサンプルでは、名前、位置（X 軸と Y 軸）、幅、高さでズームターゲットの配列を定義し、その配列をアセットに割り当てます。 応答には、新しく作成されたズームターゲットへのハンドルが含まれます。

**リクエスト**

```java
<setZoomTargetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <zoomTargetArray>
      <items>
         <name>zoomTarget2</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
      <items>
         <name>zoomTarget3</name>
         <xPosition>40</xPosition>
         <yPosition>40</yPosition>
         <width>400</width>
         <height>400</height>
      </items>
   </zoomTargetArray>
</setZoomTargetsParam>
```

**応答**

```java
<setZoomTargetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zoomTargetHandleArray>
      <items>a|947|9|41</items>
      <items>a|948|9|42</items>
   </zoomTargetHandleArray>
</setZoomTargetsReturn>
```
