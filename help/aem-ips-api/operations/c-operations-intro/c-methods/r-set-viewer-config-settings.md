---
description: アセットにビューア設定を添付します。 これらは、ビューアプリセットまたはビューアのソースアセットです。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 11%

---

# setViewerConfigSettings{#setviewerconfigsettings}

アセットにビューア設定を添付します。 これらは、ビューアプリセットまたはビューアのソースアセットです。

構文

## 承認済みユーザータイプ {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-bcc8c83cc84141e8b1341be9133e8511}

**入力（setViewerConfigSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットのハンドル： |
| name | `xsd:string` | はい | アセット名。 |
| タイプ | `xsd:string` | はい | ビューア設定を適用するアセットのタイプ。 |
| configSettingArray | `types:ConfigSettingArray` | はい | アセットに適用された`ConfigSettings`の配列… |

**Output （setViewerConfigSettingsParam）**

IPS APIは、この操作に対する応答を返しません。
