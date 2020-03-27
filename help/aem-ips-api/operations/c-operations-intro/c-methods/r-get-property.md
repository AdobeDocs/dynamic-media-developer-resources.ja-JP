---
description: Image Portalに関連するシステムプロパティの文字列値を取得します。
seo-description: Image Portalに関連するシステムプロパティの文字列値を取得します。
seo-title: getProperty
solution: Experience Manager
title: getProperty
topic: Scene7 Image Production System API
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getProperty{#getproperty}

Image Portalに関連するシステムプロパティの文字列値を取得します。

次のシステム・プロパティがサポートされています。

* `IpsVersion`:IPSバージョン番号。
* `IpsImageServerUrl`:IPS Image Serverの完全な外部URLプレフィックス。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:SVGアセットのレンダリングのURLプレフィックス。
* `SvgRenderEnabled`:SVGアセットをによってレンダリングできる場合はtrueで `SvgRenderRootUrl`す。

* `UploadPostMaxFileSize`:アップロードで許可されるファイルデータの最大サイズ（バイト） [!DNL POST]。 最大数を超えるファイルは拒否されます。

## 認証されたユーザータイプ {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Input (getPropertyParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`name`*` | `xsd:string` | はい | 取得するプロパティの名前。 |

**出力(getPropertyReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`value`*` | `xsd:string` | はい | プロパティ値。 |

## 例 {#section-3f80a78dd60c404181b34d3a912d7a36}

このコード例では、IPSプロパティの文字列定数を使用して特定の値を返します。 この例では、IPSプロパティはIPSサーバのバージョンです。

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

