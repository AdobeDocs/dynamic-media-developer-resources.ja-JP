---
description: 既存のプライマリソース画像アセットから派生した新しいアセットを作成します。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 7%

---

# createDerivedAsset{#createderivedasset}

既存のプライマリソース画像アセットから派生した新しいアセットを作成します。

構文

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生アセットでは、所有者画像の表現を変更する Image Server プロトコルコマンドを指定します。 `AdjustedView` 派生タイプは、単一の画像に単純な変更を適用する（切り抜き長方形を指定するなど）のに役立ち、`LayerView` は、テキストや追加の画像を含む多層ビューを作成するのに役立ちます。

画像コピー（[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0) を参照）とは異なり、派生画像はその所有者画像にリンクされます。 所有者画像を変更すると、関連する派生アセットが変更されます。 所有者画像を削除すると、関連付けられた派生画像がすべて削除されます。

## 許可されているユーザータイプ {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-5a0dde01cff6454da3646ea805c2be1e}

**入力（createDerivedAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 新しいアセットの派生元であるアセットを含む会社へのハンドル。 |
| ownerHandle | `xsd:string` | はい | 新しい画像の派生元となるプライマリ画像アセットへのハンドル。 |
| folderHandle | `xsd:string` | はい | 新しい派生アセットが作成されるフォルダーへのハンドル。 |
| name | `xsd:string` | はい | 派生アセットの名前。 |
| タイプ | `xsd:string` | はい | 新しい派生アセットのアセットタイプ：`AdjustedView` または `LayerView`。 |
| urlModifier | `xsd:string` | いいえ | 画像サービングまたは画像レンダリングプロトコルのコマンドが *前* 要求または `urlPostApplyModifier` のコマンドに適用された。 |
| urlPostApplyModifier | `xsd:string` | いいえ | 画像サービングまたは画像レンダリングプロトコルのコマンドが *後* リクエストまたは `urlPostApplyModifier` のコマンドに適用された。 |

**出力（createDerivedAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | 派生アセットへのハンドル。 |

## 例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

サンプルコードでは、調整済みビューと任意の値を持つ `urlModifier` と `urlPostApplyModifier` を持つ派生アセットを作成します。 応答は、新しく派生したアセットにハンドルを返します。

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
