---
description: 既存のプライマリ ソース画像アセットから派生した新しいアセットを作成します。
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
TQID: 'https://experienceleague.adobe.com/zREQqRBLpYJ30WoTEa2cmVplhQAlcqoBgzRIsMAy5sg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 7%

---

# createDerivedAsset{#createderivedasset}

既存のプライマリ ソース画像アセットから派生した新しいアセットを作成します。

構文

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

派生アセットは、所有者イメージの表現を変更するImage Server プロトコルコマンドを指定します。 `AdjustedView`派生タイプは、単一の画像に簡単な変更を適用するのに役立ちます（例えば、切り抜き長方形を指定して）。一方、`LayerView`は、テキストまたは追加の画像を含むマルチレイヤービューを作成するのに役立ちます。

画像コピー（[copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)を参照）とは異なり、派生画像はその所有者画像にリンクされます。 オーナー画像を変更すると、関連する派生アセットが変更されます。 所有者画像を削除すると、関連する派生画像が削除されます。

## 承認済みユーザータイプ {#authorized-user-types}

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
| companyHandle | `xsd:string` | はい | 新しいアセットの取得元となるアセットを含む会社へのハンドル。 |
| ownerHandle | `xsd:string` | はい | 新しい画像の派生元となるプライマリ画像アセットへのハンドル。 |
| folderHandle | `xsd:string` | はい | 新しい派生アセットが作成されるフォルダーへのハンドル。 |
| name | `xsd:string` | はい | 派生アセットの名前。 |
| タイプ | `xsd:string` | はい | 新しい派生アセットのアセットタイプ : `AdjustedView`または`LayerView`。 |
| urlModifier | `xsd:string` | いいえ | 画像サービングまたは画像レンダリングプロトコルコマンドは、リクエストの&#x200B;*前*&#x200B;または`urlPostApplyModifier` コマンドを適用しました。 |
| urlPostApplyModifier | `xsd:string` | いいえ | 画像サービングまたは画像レンダリングプロトコルコマンドは、リクエストに&#x200B;*after*&#x200B;または`urlPostApplyModifier` コマンドを適用しました。 |

**Output （createDerivedAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetHandle | `xsd:string` | はい | 派生アセットへのハンドル。 |

## 例 {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

サンプルコードでは、調整されたビューと`urlModifier`および`urlPostApplyModifier`が任意の値を持つ派生アセットが作成されます。 応答は、新しく派生したアセットにハンドルを返します。

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

