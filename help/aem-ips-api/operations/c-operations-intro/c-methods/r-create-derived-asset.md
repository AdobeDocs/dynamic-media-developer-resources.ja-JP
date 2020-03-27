---
description: 既存のマスター画像アセットから派生する新しいアセットを作成します。
seo-description: 既存のマスター画像アセットから派生する新しいアセットを作成します。
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# createDerivedAsset{#createderivedasset}

既存のマスター画像アセットから派生する新しいアセットを作成します。

構文

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生アセットは、所有者画像の表現を変更するImage Serverプロトコルコマンドを指定します。 派生タ `AdjustedView` イプは、単一の画像に単純な変更（切り抜きの長方形を指定するなど）を適用するのに役立ち、テキストや追加の画像を含む多層ビューを `LayerView` 作成するのに役立ちます。

イメージコピー(copyImageを参照 [](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0))とは異なり、派生イメージは所有者イメージにリンクされます。 所有者の画像を変更すると、関連付けられた派生アセットが変更されます。 所有者画像を削除すると、関連付けられた派生画像がすべて削除されます。

## 認証されたユーザータイプ {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-5a0dde01cff6454da3646ea805c2be1e}

**入力(createDerivedAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 新しいアセットの派生元となるアセットを含む会社のハンドル。 |
| ` *`ownerHandle`*` | `xsd:string` | はい | 新しい画像の派生元となるマスター画像アセットのハンドル。 |
| ` *`folderHandle`*` | `xsd:string` | はい | 新しい派生アセットが作成されるフォルダーのハンドル。 |
| ` *`name`*` | `xsd:string` | はい | 派生アセットの名前。 |
| ` *`type`*` | `xsd:string` | はい | 新しい派生アセットのアセットタイプ：ま `AdjustedView` た `LayerView`は |
| ` *`urlModifier`*` | `xsd:string` | いいえ | 要求またはコマンドの前に適用される画像サービング *または* 画像レンダリングプロト `urlPostApplyModifier` コルコマンド。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | いいえ | 要求またはコマンドの後に適用される画像サービ *ング* または画像レンダリングプロト `urlPostApplyModifier` コルコマンド。 |

**出力(createDerivedAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | はい | 派生アセットのハンドル。 |

## 例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

サンプルコードは、調整されたビューと任意の値を持つ派生アセ `urlModifier` ットを `urlPostApplyModifier` 作成します。 応答は、新しく派生したアセットにハンドルを返します。

**リクエスト**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**応答**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```

