---
description: アセットの名前を変更します。
solution: Experience Manager
title: renameAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fff3c1-1b48-4d86-8a81-f75be00fc329
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 7%

---

# renameAsset{#renameasset}

アセットの名前を変更します。

>[!NOTE]
>
>この `renameFiles` パラメーターは以前のリリースで非推奨となり、から削除されました `renameAsset`. 仮想ファイルのパスは、新しいアセット名（ファイル拡張子を維持）に一致するように変更されますが、物理ファイルのパスは影響を受けません。 API クライアントは、新しい API バージョンに更新する際に、このパラメーターへの参照を削除する必要があります。

## 認証済みユーザータイプ {#section-cc27ad713c6d498b8f056850b20976f4}

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

**入力 (renameAssetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アセットが属する会社のハンドル。 |
| assetHandle | `xsd:string` | はい | 名前を変更するアセットのハンドル。 |
| newName | `xsd:string` | はい | アセットの新しい名前。 |
| validateName | `xsd:boolean` | はい | この `validateName` が `true` また、アセットタイプには一意の IPS ID が必要です。その後、新しい名前がグローバルに一意であるかどうかがチェックされます。 `renameAsset` 一意でない場合はエラーをスローします。 |

**出力 (renameAssetReturn)**

IPS API はこの操作に対する応答を返しません。 詳しくは、 `<ns1:validateName>` 要素を参照してください。

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
