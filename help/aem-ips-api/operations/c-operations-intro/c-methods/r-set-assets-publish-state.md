---
description: アセットのバッチを公開する準備ができているかどうかを判断します。
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
TQID: 'https://experienceleague.adobe.com/VV11khRodimEOAdPB-6mHR-gIT4AMiKOKeuuH6J15VA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 10%

---

# setAssetsPublishState{#setassetspublishstate}

アセットのバッチを公開する準備ができているかどうかを判断します。

これは、[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)のバッチ バージョンです。

## 承認済みユーザータイプ {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーには、アセットへの読み取りおよび書き込みアクセス権が必要です。

## パラメーター {#section-3e49d7859f8647b990d75373cc8dbc24}

**入力（setAssetsPublishStateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | はい | アセットのパブリッシュステート値の配列。 |

**出力（setAssetsPublishStateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に更新されたアセットの数。 |
| warningCount | `xsd:int` | はい | 操作が更新しようとしたときに警告を生成したアセットの数。 |
| errorCount | `xsd:int` | はい | 操作が削除しようとしたときにエラーを生成したアセットの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 警告を生成したアセット更新に関連する詳細。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | エラーを生成したアセット更新に関連する詳細。 |

## 例 {#section-38cfdd3436214a06a1bae16875501d51}

このコードサンプルでは、アセットの公開状態を設定します。

**リクエスト**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**応答**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```
