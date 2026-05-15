---
description: Image Portalに関連するシステムプロパティの文字列値を取得します。
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
TQID: 'https://experienceleague.adobe.com/loaZvP3tI8neQ6ziLR-xKkkNqGGjD8Mq1jbeC8mJEQo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 9%

---

# getProperty{#getproperty}

Image Portalに関連するシステムプロパティの文字列値を取得します。

サポートされるシステムプロパティには、次のものがあります。

* `IpsVersion`: IPS バージョン番号。
* `IpsImageServerUrl`: IPS Image Serverの完全な外部URL プレフィックス。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: SVG アセットをレンダリングするためのURL プレフィックス。
* `SvgRenderEnabled`: `SvgRenderRootUrl`がSVG アセットをレンダリングできる場合はTrueです。

* `UploadPostMaxFileSize`: アップロード [!DNL POST]で許可されるファイルデータの最大サイズ （バイト単位）。 システムは、上限を超えるファイルを拒否します。

## 承認済みユーザータイプ {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**入力（getPropertyParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| name | `xsd:string` | はい | 取得するプロパティの名前。 |

**出力（getPropertyReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| value | `xsd:string` | はい | プロパティ値。 |

## 例 {#section-3f80a78dd60c404181b34d3a912d7a36}

このコードのサンプルでは、IPS プロパティ文字列定数を使用して、特定の値を返します。 この例では、IPS プロパティはIPS サーバーのバージョンです。

**リクエスト**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**応答**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
