---
description: アセットのバッチを公開する準備ができているかどうかを指定します。
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 12%

---

# setAssetsPublishState{#setassetspublishstate}

アセットのバッチを公開する準備ができているかどうかを指定します。

これは、 [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## 認証済みユーザータイプ {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーは、アセットに対する読み取りおよび書き込みアクセス権を持っている必要があります。

## パラメータ {#section-3e49d7859f8647b990d75373cc8dbc24}

**入力 (setAssetsPublishStateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | はい | アセットの公開状態値の配列。 |

**出力 (setAssetsPublishStateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に更新されたアセットの数。 |
| warningCount | `xsd:int` | はい | 操作が更新を試みたときに警告が発生したアセットの数。 |
| errorCount | `xsd:int` | はい | 操作が削除を試みたときにエラーが発生したアセットの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 警告を生成したアセットの更新に関連する詳細。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | エラーを発生させたアセットの更新に関連する詳細。 |

## 例 {#section-38cfdd3436214a06a1bae16875501d51}

このコードサンプルは、アセットの公開状態を設定します。

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
