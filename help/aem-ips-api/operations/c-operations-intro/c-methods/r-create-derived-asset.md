---
description: 既存のプライマリソース画像アセットから派生する新しいアセットを作成します。
seo-description: 既存のプライマリソース画像アセットから派生する新しいアセットを作成します。
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
feature: Dynamic Mediaクラシック，SDK/API，アセット管理
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 8%

---


# createDerivedAsset{#createderivedasset}

既存のプライマリソース画像アセットから派生する新しいアセットを作成します。

構文

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生アセットは、所有者画像の表現を変更するImage Serverプロトコルコマンドを指定します。 `AdjustedView`派生型は、単一の画像に単純な変更を適用する場合（切り抜き長方形を指定する場合など）に役立ちます。`LayerView`は、テキストや追加の表示を含むマルチレイヤー画像の作成に役立ちます。

イメージコピー（[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)を参照）とは異なり、派生イメージは所有者イメージにリンクされます。 所有者の画像を変更すると、関連付けられた派生アセットが変更されます。 所有者画像を削除すると、関連付けられた派生画像はすべて削除されます。

## 認証済みユーザータイプ{#authorized-user-types}

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
| `*`companyHandle`*` | `xsd:string` | はい | 新しいアセットの派生元となるアセットを含む会社へのハンドル。 |
| `*`ownerHandle`*` | `xsd:string` | はい | 新しい画像の派生元となるプライマリ画像アセットへのハンドル。 |
| `*`folderHandle`*` | `xsd:string` | はい | 新しい派生アセットを作成するフォルダーへのハンドル。 |
| `*`name`*` | `xsd:string` | はい | 派生したアセットの名前。 |
| `*`type`*` | `xsd:string` | はい | 新しい派生アセットのアセットタイプ。`AdjustedView`または`LayerView`。 |
| `*`urlModifier`*` | `xsd:string` | いいえ | 要求または`urlPostApplyModifier`コマンドの前に&#x200B;*適用された画像サービングまたは画像レンダリングプロトコルコマンド。* |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | 要求または`urlPostApplyModifier`コマンドに&#x200B;*後ろに*&#x200B;適用された画像サービングまたは画像レンダリングプロトコルコマンド。 |

**出力(createDerivedAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | 派生したアセットのハンドル。 |

## 例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

サンプルコードは、表示を調整し、任意の値を持つ`urlModifier`と`urlPostApplyModifier`を持つ派生アセットを作成します。 応答は、新しく生成されたアセットにハンドルを返します。

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

