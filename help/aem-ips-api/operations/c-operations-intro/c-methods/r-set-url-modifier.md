---
description: 指定したアセットの画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄することなく、アセットの表現を変更します。
seo-description: 指定したアセットの画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄することなく、アセットの表現を変更します。
seo-title: setUrlModifier
solution: Experience Manager
title: setUrlModifier
topic: Scene7 Image Production System API
uuid: ec423e57-338b-4a32-be5a-a73fa96712ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUrlModifier{#seturlmodifier}

指定したアセットの画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄することなく、アセットの表現を変更します。

画像サービングの場合、パラメータ内のコ `urlModifier` マンドは、修飾子カタログフィールドに公開され、要求URLで指定されたコマンドの前に適用されます。 のコマンドは `urlPostApplyModifier` カタログフィールドに `PostModifier` 公開され、要求URLまたは内のすべてのコマンドに優先しま `urlModifier`す。 画像レンダリングの場合、とのコマンドが連 `urlModifier` 結さ `urlPostApplyModifier` れ、修飾子カタログフィールドにパブリッシュされます。

## 認証されたユーザータイプ {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**入力(setUrlModifierParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| ` *`assetHandle`*` | `xsd:string` | はい | アセットハンドル。 |
| ` *`urlModifier`*` | `xsd:string` | いいえ | 要求またはコマンドの前に適用する画像サービングまたは画像レンダリングプロトコルコ `urlPostApplyModifier` マンド。 |
| ` *`urlPostApplyModifier`*` | `xsd:string` | いいえ | コマンドの後および要求後に適用する画像サービングまたは画像レンダリ `urlModifier` ングプロトコルコマンド。 |

**出力(setUrlModifierReturn)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-801d4b9b986443f59a5783a3d6bf44aa}

**リクエスト**

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**応答**

なし
