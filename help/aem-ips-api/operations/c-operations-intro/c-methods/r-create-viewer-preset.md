---
description: ユーザが何を表示できるかを決定するプリセットビューを作成します。 ビューアは、IPSで使用可能な任意の種類です。 プリセットビューは、アセットが公開されるときに適用されます。
seo-description: ユーザが何を表示できるかを決定するプリセットビューを作成します。 ビューアは、IPSで使用可能な任意の種類です。 プリセットビューは、アセットが公開されるときに適用されます。
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
topic: Scene7 Image Production System API
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createViewerPreset{#createviewerpreset}

ユーザが何を表示できるかを決定するプリセットビューを作成します。 ビューアは、IPSで使用可能な任意の種類です。 プリセットビューは、アセットが公開されるときに適用されます。

構文

## 認証されたユーザータイプ {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-aa6dc37e327541ebbfed7685cd8071ff}

**入力(createViewerPresetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | ビューアプリセットとアセットを含む会社のハンドル。 |
| ` *`folderHandle`*` | `xsd:string` | はい | アセットを含むフォルダーのハンドル。 |
| ` *`name`*` | `xsd:string` | はい | ビューア名 |
| ` *`type`*` | `xsd:string` | はい | ビューアタイプ. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | いいえ | プリセットを適用する画像の名前、値、ハンドルを含む配列。 |

**出力(createViewerPresetReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`viewerPresetHandle`*` | `xsd:string` | はい | ビューアに対するプリセットのハンドル。 |

## 例 {#section-c88ea63536f3461cbe4677ba53f875dd}

このコードサンプルを使用して、ビデオプレーヤープリセットを作成します。 応答はプリセットのハンドルを返します。

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

