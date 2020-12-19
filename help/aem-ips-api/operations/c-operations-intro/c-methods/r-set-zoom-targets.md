---
description: アセット画像に関連付けられるズームターゲットを設定します。 既存のズームターゲットは上書きされます。
seo-description: アセット画像に関連付けられるズームターゲットを設定します。 既存のズームターゲットは上書きされます。
seo-title: setZoomTargets
solution: Experience Manager
title: setZoomTargets
topic: Scene7 Image Production System API
uuid: 5d0aecec-ebd8-4c69-9514-c29fae347ee6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 12%

---


# setZoomTargets{#setzoomtargets}

アセット画像に関連付けられるズームターゲットを設定します。 既存のズームターゲットは上書きされます。

構文

## 承認されたユーザータイプ{#section-c5e1863e9cb1426591bfea513620b6ab}

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
| ` *`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| ` *`assetHandle`*` | `xsd:string` | はい | ズームターゲットを設定するアセット。 |
| ` *`zoomTargetArray`*` | `types:ZoomTargetDefinitionArray` | はい | ズームターゲット定義の配列。 |

**出力(setZoomTargetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`zoomTargetHandleArray`*` | `types:HandleArray` | はい | この操作で作成されるズームターゲットのハンドルのセットです。 |

## 例 {#section-a2f14c7a1499443e96d099ea8a76c182}

次のコードの例では、名前、位置（x軸とy軸）、幅と高さでズームターゲットの配列を定義し、その配列をアセットに割り当てます。 応答には、新しく作成されたズームターゲットのハンドルが含まれます。

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

