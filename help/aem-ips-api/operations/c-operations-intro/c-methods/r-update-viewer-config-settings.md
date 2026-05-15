---
description: SWF ビューアの設定を更新します。
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
TQID: 'https://experienceleague.adobe.com/YcfK5U6MKvmV2ulOQ3s2sOOBsgASSeslCIrk87xLAv8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 13%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

SWF ビューアの設定を更新します。

構文

## 承認済みユーザータイプ {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-29790d933fb24aa392d0cb2d52d1310f}

**入力（updateViewerConfigSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットのハンドル： |
| configSettingArray | `types:ConfigSettingArray` | はい | ビューアに適用する設定の配列。 |

**出力（updateViewerConfigSettingsReturn）**

IPS APIは、この操作に対する応答を返しません。
