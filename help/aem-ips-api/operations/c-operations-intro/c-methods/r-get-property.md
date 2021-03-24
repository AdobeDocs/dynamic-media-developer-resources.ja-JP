---
description: 画像ポータルに関連するシステムプロパティのstring値を取得します。
solution: Experience Manager
title: getProperty
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 10%

---


# getProperty{#getproperty}

画像ポータルに関連するシステムプロパティのstring値を取得します。

次のシステムプロパティがサポートされます。

* `IpsVersion`:IPSバージョン番号。
* `IpsImageServerUrl`:IPS Image Serverの完全な外部URLプレフィックス。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:SVGアセットをレンダリングするためのURLプレフィックス。
* `SvgRenderEnabled`:SVGアセットをによってレンダリングできる場合はtrue `SvgRenderRootUrl`です。

* `UploadPostMaxFileSize`:アップロードで許可されるファイルデータの最大サイズ（バイト単位） [!DNL POST]。最大数を超えるファイルは拒否されます。

## 認証済みユーザータイプ{#section-2cd36bbd46ed414b8753569d5895530e}

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

**入力(getPropertyParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`name`*` | `xsd:string` | はい | 取得するプロパティの名前。 |

**出力(getPropertyReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`value`*` | `xsd:string` | はい | プロパティ値。 |

## 例 {#section-3f80a78dd60c404181b34d3a912d7a36}

このコードの例では、IPSプロパティの文字列定数を使用して特定の値を返します。 この例では、IPSプロパティはIPSサーバのバージョンです。

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

