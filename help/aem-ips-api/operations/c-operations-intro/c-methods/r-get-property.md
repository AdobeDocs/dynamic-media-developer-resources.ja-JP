---
description: 画像ポータルに関連するシステムプロパティの文字列値を取得します。
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 12%

---

# getProperty{#getproperty}

画像ポータルに関連するシステムプロパティの文字列値を取得します。

次のシステムプロパティがサポートされています。

* `IpsVersion`:IPS バージョン番号。
* `IpsImageServerUrl`:IPS Image Server の完全な外部 URL プレフィックス。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:SVGアセットをレンダリングするための URL プレフィックス。
* `SvgRenderEnabled`:True を指定すると、SVGアセットは `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`:アップロードで許可されるファイルデータの最大サイズ（バイト単位） [!DNL POST]. 最大数を超えるファイルは拒否されます。

## 認証済みユーザータイプ {#section-2cd36bbd46ed414b8753569d5895530e}

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

**入力 (getPropertyParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| name | `xsd:string` | はい | 取得するプロパティの名前。 |

**出力 (getPropertyReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| value | `xsd:string` | はい | プロパティの値。 |

## 例 {#section-3f80a78dd60c404181b34d3a912d7a36}

このコード例では、IPS プロパティの文字列定数を使用して、特定の値を返します。 この例では、IPS プロパティは IPS サーバのバージョンです。

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
