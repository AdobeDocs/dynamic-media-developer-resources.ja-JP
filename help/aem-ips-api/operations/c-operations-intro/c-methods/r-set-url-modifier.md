---
description: 指定したアセットに対して、画像サービングまたは画像レンダリングプロトコルのコマンドを設定します。 これらのコマンドは、アセットを破棄せずにアセットの表示を変更します。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

指定したアセットに対して、画像サービングまたは画像レンダリングプロトコルのコマンドを設定します。 これらのコマンドは、アセットを破棄せずにアセットの表示を変更します。

画像サービングの場合、 `urlModifier` パラメータは「モディファイヤカタログ」フィールドにパブリッシュされ、リクエスト URL で指定されたコマンドの前に適用されます。 のコマンド `urlPostApplyModifier` が `PostModifier` カタログフィールドを使用し、リクエスト URL または `urlModifier`. 画像レンダリングの場合、 `urlModifier` および `urlPostApplyModifier` が連結され、「修飾子カタログ」フィールドにパブリッシュされます。

## 認証済みユーザータイプ {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**入力 (setUrlModifierParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社の取り扱い。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル。 |
| `*`urlModifier`*` | `xsd:string` | いいえ | 要求または要求の前に適用する画像サービングまたは画像レンダリングプロトコルコマンド `urlPostApplyModifier` コマンド |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | 後に適用する画像サービングまたは画像レンダリングプロトコルコマンド `urlModifier` およびリクエストコマンド |

**出力 (setUrlModifierReturn)**

IPS API はこの操作に対する応答を返しません。

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
