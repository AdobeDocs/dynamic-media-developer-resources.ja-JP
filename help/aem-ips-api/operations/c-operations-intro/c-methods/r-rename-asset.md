---
description: アセットの名前を変更します。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
TQID: 'https://experienceleague.adobe.com/m1AT0yP7u3PFZCs8uoFQxQoGNtfJe49vzGt8e3wTx8s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 5%

---

# renameAsset{#renameasset}

アセットの名前を変更します。

>[!NOTE]
>
>以前のリリースでは、`renameFiles` パラメーターは廃止され、`renameAsset`から削除されました。 仮想ファイルパスは、新しいアセット名に一致するように変更されますが（ファイル拡張子は保持されます）、物理ファイルパスは影響を受けません。 API クライアントは、新しいAPI バージョンに更新する際に、このパラメーターへの参照を削除する必要があります。

## 承認済みユーザータイプ {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りおよび書き込みアクセス権が必要です。

## パラメーター {#section-ef95a994106841e0ab346dd4cf672258}

**入力（renameAssetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アセットが属する会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 名前を変更するアセットへのハンドル。 |
| newName | `xsd:string` | はい | アセットの新しい名前。 |
| validateName | `xsd:boolean` | はい | `validateName`が`true`で、アセットタイプが一意のIPS IDを必要とする場合、新しい名前はグローバルな一意性をチェックされ、`renameAsset`は一意でない場合に障害をスローします。 |

**出力（renameAssetReturn）**

IPS APIは、この操作に対する応答を返しません。 この要素に関する注意事項については、`<ns1:validateName>`要素の説明を参照してください。

## 例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

このコードサンプルは、アセットの名前を変更します

**リクエスト**

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**応答**

なし
