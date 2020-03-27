---
description: アセットの名前を変更します。
seo-description: アセットの名前を変更します。
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: f285d7e4-00df-4d90-a05a-71747a4c54cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameAsset{#renameasset}

アセットの名前を変更します。

>[!NOTE]
>
>このパラ `renameFiles` メーターは以前のリリースでは廃止され、から削除されまし `renameAsset`た。 仮想ファイルのパスは、新しいアセット名（ファイル拡張子を保持）に一致するように変更されますが、物理ファイルのパスは影響を受けません。 APIクライアントは、新しいAPIバージョンに更新する際に、このパラメーターへの参照を削除する必要があります。

## 認証されたユーザータイプ {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImpagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび書き込みアクセス権を持っている必要があります。

## パラメータ {#section-ef95a994106841e0ab346dd4cf672258}

**Input (renameAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | アセットが属する会社のハンドル。 |
| ` *`assetHandle`*` | `xsd:string` | はい | 名前を変更するアセットのハンドル。 |
| ` *`newName`*` | `xsd:string` | はい | アセットの新しい名前。 |
| ` *`validateName`*` | `xsd:boolean` | はい | がで、アセ `validateName` ットタ `true` イプが一意のIPS IDを必要とする場合、新しい名前がグローバルな一意性をチェックし、一意でな `renameAsset` い場合はエラーをスローします。 |

**出力(renameAssetReturn)**

IPS APIはこの操作に対する応答を返しません。 この要素に関する注意事項については、 `<ns1:validateName>` 要素の説明を参照してください。

## 例 {#section-a0ddffd62bec42e09069f22ceb486f8a}

このコード例では、アセットの名前を変更します

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
