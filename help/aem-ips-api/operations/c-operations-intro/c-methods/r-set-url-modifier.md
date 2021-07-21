---
description: 指定したアセットに対して、画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄せずにアセットの表現を変更します。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# setUrlModifier{#seturlmodifier}

指定したアセットに対して、画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄せずにアセットの表現を変更します。

画像サービングの場合、`urlModifier`パラメーターのコマンドは「修飾子カタログ」フィールドに公開され、要求URLで指定されたコマンドの前に適用されます。 `urlPostApplyModifier`内のコマンドは、`PostModifier`カタログフィールドに公開され、リクエストURLまたは`urlModifier`内のコマンドが上書きされます。 画像レンダリングの場合、`urlModifier`と`urlPostApplyModifier`のコマンドが連結され、モディファイヤカタログフィールドにパブリッシュされます。

## 許可されたユーザーの種類 {#section-fefcd732ccf64c78956606538f96c73d}

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
| `*`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| `*`assetHandle`*` | `xsd:string` | はい | アセットハンドル。 |
| `*`urlModifier`*` | `xsd:string` | いいえ | 要求または`urlPostApplyModifier`コマンドの前に適用する画像サービングまたは画像レンダリングプロトコルコマンド。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | いいえ | `urlModifier`の後に適用する画像サービングまたは画像レンダリングプロトコルコマンドと、コマンドを要求します。 |

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
