---
description: 指定したアセットの画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄することなく、アセットの表現を変更します。
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
TQID: 'https://experienceleague.adobe.com/dcz-gnw7NjHKN7EvsGvSRDmu4dgCUo2PPr3GjYLVoOA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 175
ht-degree: 5%

---

# setUrlModifier{#seturlmodifier}

指定したアセットの画像サービングまたは画像レンダリングプロトコルコマンドを設定します。 これらのコマンドは、アセットを破棄することなく、アセットの表現を変更します。

画像サービングの場合、`urlModifier` パラメーターのコマンドは、修飾子カタログフィールドに公開され、リクエスト URLで指定されたコマンドよりも前に適用されます。 `urlPostApplyModifier`のコマンドは`PostModifier` カタログフィールドに公開され、リクエスト URLまたは`urlModifier`のコマンドを上書きします。 画像レンダリングの場合、`urlModifier`と`urlPostApplyModifier`のコマンドは連結され、修飾子カタログフィールドに公開されます。

## 承認済みユーザータイプ {#section-fefcd732ccf64c78956606538f96c73d}

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
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| assetHandle | `xsd:string` | はい | アセットのハンドル： |
| urlModifier | `xsd:string` | いいえ | 要求または`urlPostApplyModifier` コマンドの前に適用する画像サービングまたは画像レンダリング プロトコル コマンド。 |
| urlPostApplyModifier | `xsd:string` | いいえ | 画像サービングまたは画像レンダリング プロトコルのコマンドは、`urlModifier`および要求コマンドの後に適用されます。 |

**出力（setUrlModifierReturn）**

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
