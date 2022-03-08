---
description: ユーザーに表示する内容を決定するプリセットビューを作成します。 ビューアは、IPS で使用できる任意のタイプにすることができます。 プリセットビューは、アセットが公開される際に適用されます。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 13%

---

# createViewerPreset{#createviewerpreset}

ユーザーに表示する内容を決定するプリセットビューを作成します。 ビューアは、IPS で使用できる任意のタイプにすることができます。 プリセットビューは、アセットが公開される際に適用されます。

構文

## 認証済みユーザータイプ {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-aa6dc37e327541ebbfed7685cd8071ff}

**入力 (createViewerPresetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | ビューアプリセットとアセットを含む会社のハンドル。 |
| folderHandle | `xsd:string` | はい | アセットを含むフォルダーのハンドル。 |
| name | `xsd:string` | はい | ビューア名 |
| タイプ | `xsd:string` | はい | ビューアタイプ. |
| configSettingArray | `types:ConfigSettingArray` | いいえ | プリセットを適用する画像の名前、値、ハンドルを含む配列。 |

**出力 (createViewerPresetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | はい | ビューアに対するプリセットの処理。 |

## 例 {#section-c88ea63536f3461cbe4677ba53f875dd}

このコードサンプルは、ビデオプレーヤープリセットを作成します。 応答は、ハンドルをプリセットに返します。

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
