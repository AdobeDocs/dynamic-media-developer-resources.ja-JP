---
description: 指定したアセットに関連付けられているすべてのビューア設定を取得します。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
TQID: 'https://experienceleague.adobe.com/GeSAS1EP7Q6EgsQltyC-TVnxS0zusuKxKs6QL8wfLWw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 20%

---

# getViewerConfigSettings{#getviewerconfigsettings}

指定したアセットに関連付けられているすべてのビューア設定を取得します。

構文

## 承認済みユーザータイプ {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-7d06abf3d707494c8a1270c7fa1477f1}

**入力（getViewerConfigSettingsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| assetHandle | `xsd:string` | はい | アセットを処理します。 |

**Output （getViewerCoinfigSettingsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| タイプ | `xsd:string` | はい | 設定設定が適用されるビューアータイプ。 |
| configSettingsArray | `types:ConfigSettingsArray` | はい | ビューア設定の配列。 |

