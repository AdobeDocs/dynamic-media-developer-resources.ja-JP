---
description: アセットのバッチを公開する準備ができているかどうかを判断します。
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 10%

---

# setAssetsPublishState{#setassetspublishstate}

アセットのバッチを公開する準備ができているかどうかを判断します。

これは、[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563) のバッチバージョンです。

## 許可されているユーザータイプ {#section-0804726f683944dbbe9acfc3d35ccf25}

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
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | はい | アセットの公開状態値の配列。 |

**出力（setAssetsPublishStateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | 正常に更新されたアセットの数。 |
| warningCount | `xsd:int` | はい | 操作で更新しようとしたときに警告が生成されたアセットの数です。 |
| errorCount | `xsd:int` | はい | 操作で削除しようとしたときにエラーが生成されたアセットの数です。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 警告が生成されたアセット更新に関連付けられた詳細。 |
| errorDetailArray | `types:AssetOperationFaultArray` | いいえ | エラーを生成したアセット更新に関連付けられている詳細。 |

## 例 {#section-38cfdd3436214a06a1bae16875501d51}

次のコードのサンプルでは、アセットの公開状態を設定します。

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
