---
description: アセット画像に関連付けられているズームターゲットを設定します。 既存のズームターゲットが上書きされます。
solution: Experience Manager
title: setZoomTargets
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 1b4ac729-00cf-4ea2-9098-60b4af3c7e6d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 13%

---

# setZoomTargets{#setzoomtargets}

アセット画像に関連付けられているズームターゲットを設定します。 既存のズームターゲットが上書きされます。

構文

## 認証されたユーザータイプ {#section-c5e1863e9cb1426591bfea513620b6ab}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-161f8c733cc4439f94a06e12119d4226}

**入力(setZoomTargetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| `*`assetHandle`*` | `xsd:string` | はい | 設定するズームターゲットを持つアセット。 |
| `*`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | はい | ズームターゲット定義の配列。 |

**出力(setZoomTargetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`zoomTargetHandleArray`*` | `types:HandleArray` | はい | この操作で作成されたズームターゲットに対するハンドルのセット。 |

## 例 {#section-a2f14c7a1499443e96d099ea8a76c182}

このコード例では、名前、位置（x軸とy軸）、幅、高さでズームターゲットの配列を定義し、その配列をアセットに割り当てます。 応答には、新しく作成されたズームターゲットへのハンドルが含まれます。

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
