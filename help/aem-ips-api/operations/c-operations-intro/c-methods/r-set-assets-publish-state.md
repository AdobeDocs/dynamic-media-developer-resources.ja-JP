---
description: アセットのバッチを発行する準備ができているかどうかを指定します。
seo-description: アセットのバッチを発行する準備ができているかどうかを指定します。
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Scene7 Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---


# setAssetsPublishState{#setassetspublishstate}

アセットのバッチを発行する準備ができているかどうかを指定します。

これは、[setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563)のバッチバージョンです。

## 認証済みユーザータイプ{#section-0804726f683944dbbe9acfc3d35ccf25}

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

**入力(setAssetsPublishStateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| ` *`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | はい | アセットの公開状態値の配列。 |

**出力(setAssetsPublishStateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に更新されたアセットの数。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作が更新を試みたときに警告を生成したアセットの数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作がアセットを削除しようとしたときにエラーが発生したアセットの数。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 警告を生成したアセットの更新に関連付けられた詳細。 |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | エラーを生成したアセットの更新に関連付けられた詳細。 |

## 例 {#section-38cfdd3436214a06a1bae16875501d51}

次のコードのサンプルを使用すると、アセットのパブリケーション状態を設定できます。

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

