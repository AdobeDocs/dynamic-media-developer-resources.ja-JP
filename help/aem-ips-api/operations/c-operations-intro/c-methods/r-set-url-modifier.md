---
description: 指定したアセットに対する画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 次の各コマンドは、アセットを破棄することなくアセットの表現を変更します。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 7%

---


# setUrlModifier{#seturlmodifier}

指定したアセットに対する画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 次の各コマンドは、アセットを破棄することなくアセットの表現を変更します。

画像サービングでは、`urlModifier`パラメーターのコマンドは、修飾子カタログフィールドに公開され、要求URLで指定されたコマンドの前に適用されます。 `urlPostApplyModifier`内のコマンドは、`PostModifier`カタログフィールドに発行され、要求URLまたは`urlModifier`内のすべてのコマンドが上書きされます。 画像レンダリングの場合、`urlModifier`と`urlPostApplyModifier`のコマンドが連結され、修飾子カタログフィールドに公開されます。

## 認証済みユーザータイプ{#section-fefcd732ccf64c78956606538f96c73d}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル |
| `*`urlModifier`*` | `xsd:string` | いいえ | 要求または`urlPostApplyModifier`コマンドの前に適用する画像サービングまたは画像レンダリングプロトコルコマンド。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | `urlModifier`およびrequestコマンドの後に適用する画像サービングまたは画像レンダリングプロトコルコマンド。 |

**出力(setUrlModifierReturn)**

IPS APIは、この操作に対する応答を返しません。

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
