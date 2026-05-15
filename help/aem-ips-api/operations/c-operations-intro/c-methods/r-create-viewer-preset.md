---
description: ユーザーに表示される内容を決定するプリセットビューを作成します。 ビューアは、IPSで使用可能な任意のタイプにすることができます。 アセットが公開されると、プリセットビューが適用されます。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
TQID: 'https://experienceleague.adobe.com/0RlldrqgWyv0YeP-QqtiVqlDpWtGk60mOWf-w9ageYA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 11%

---

# createViewerPreset{#createviewerpreset}

ユーザーに表示される内容を決定するプリセットビューを作成します。 ビューアは、IPSで使用可能な任意のタイプにすることができます。 アセットが公開されると、プリセットビューが適用されます。

構文

## 承認済みユーザータイプ {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-aa6dc37e327541ebbfed7685cd8071ff}

**入力（createViewerPresetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ビューアプリセットとアセットを含む会社のハンドル。 |
| folderHandle | `xsd:string` | はい | アセットを含むフォルダーのハンドル。 |
| name | `xsd:string` | はい | ビューアー名： |
| タイプ | `xsd:string` | はい | ビューアータイプ： |
| configSettingArray | `types:ConfigSettingArray` | いいえ | プリセットを適用する画像の名前、値、ハンドルを含む配列。 |

**出力（createViewerPresetReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | はい | ビューアへのプリセットのハンドル。 |

## 例 {#section-c88ea63536f3461cbe4677ba53f875dd}

このコードサンプルでは、ビデオプレーヤープリセットを作成します。 応答は、プリセットへのハンドルを返します。

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**応答**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
