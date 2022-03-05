---
description: 既存のプライマリソース画像アセットから派生する新しいアセットを作成します。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

既存のプライマリソース画像アセットから派生する新しいアセットを作成します。

構文

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生アセットは、所有者画像の表現を変更する Image Server プロトコルコマンドを指定します。 この `AdjustedView` 派生タイプは、単一の画像（切り抜きの長方形など）に簡単な変更を適用するのに役立ちますが、 `LayerView` は、テキストや追加の画像を含む多層ビューを作成するのに役立ちます。

画像コピーとは異なります ( [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)) の場合、派生画像はその所有者画像にリンクされます。 所有者の画像を変更すると、関連する派生アセットが変更されます。 所有者画像を削除すると、関連する派生画像がすべて削除されます。

## 認証済みユーザータイプ {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-5a0dde01cff6454da3646ea805c2be1e}

**入力 (createDerivedAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 新しいアセットの派生元となるアセットを含む会社へのハンドル。 |
| `*`ownerHandle`*` | `xsd:string` | はい | 新しい画像の派生元となるプライマリ画像アセットへのハンドル。 |
| `*`folderHandle`*` | `xsd:string` | はい | 新しい派生アセットが作成されるフォルダーのハンドル。 |
| `*`name`*` | `xsd:string` | はい | 派生アセットの名前。 |
| `*`type`*` | `xsd:string` | はい | 新しい派生アセットのアセットタイプ： `AdjustedView` または `LayerView`. |
| `*`urlModifier`*` | `xsd:string` | いいえ | 適用される画像サービングまたは画像レンダリングプロトコルコマンド *前* 要求または `urlPostApplyModifier` コマンド |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | 適用される画像サービングまたは画像レンダリングプロトコルコマンド *後* 要求に対して、または `urlPostApplyModifier` コマンド |

**出力 (createDerivedAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | はい | 派生アセットのハンドル。 |

## 例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

サンプルコードは、ビューを調整した派生アセットを作成し、 `urlModifier` および `urlPostApplyModifier` 任意の値を持つ。 応答は、新しく派生したアセットにハンドルを返します。

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
