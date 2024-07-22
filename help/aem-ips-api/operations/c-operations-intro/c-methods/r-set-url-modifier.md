---
description: 指定したアセットの画像サービングまたは画像レンダリングのプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄せずに、アセットの表現を変更します。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 5%

---

# setUrlModifier{#seturlmodifier}

指定したアセットの画像サービングまたは画像レンダリングのプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄せずに、アセットの表現を変更します。

画像サービングの場合、`urlModifier` パラメーターのコマンドは修飾子カタログ フィールドで公開され、リクエスト URL で指定されたコマンドの前に適用されます。 `urlPostApplyModifier` のコマンドは、`PostModifier` カタログフィールドに公開され、リクエスト URL や `urlModifier` のコマンドを上書きします。 画像レンダリングの場合、`urlModifier` と `urlPostApplyModifier` のコマンドが連結され、[ モディファイヤ カタログ ] フィールドにパブリッシュされます。

## 許可されているユーザータイプ {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**入力（setUrlModifierParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| assetHandle | `xsd:string` | はい | アセットハンドル。 |
| urlModifier | `xsd:string` | いいえ | リクエストコマンドまたはリク `urlPostApplyModifier` ストコマンドの前に適用する画像サービングまたは画像レンダリングプロトコルコマンド。 |
| urlPostApplyModifier | `xsd:string` | いいえ | 画像およびリクエストコマンドの後に適用する画像サービングまたは画像レンダリン `urlModifier` プロトコルコマンド。 |

**出力（setUrlModifierReturn）**

IPS API は、この操作に対して応答を返しません。

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
