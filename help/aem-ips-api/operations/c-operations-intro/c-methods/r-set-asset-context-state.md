---
description: 1つ以上のアセットの公開状態を設定または更新します。 会社の公開コンテキストごとに個別の公開状態を設定できます。
seo-description: 1つ以上のアセットの公開状態を設定または更新します。 会社の公開コンテキストごとに個別の公開状態を設定できます。
seo-title: setAssetsContextState
solution: Experience Manager
title: setAssetsContextState
topic: Scene7 Image Production System API
uuid: 4b94f9ea-3f7b-45ee-9381-6434f2bc4e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetsContextState{#setassetscontextstate}

1つ以上のアセットの公開状態を設定または更新します。 会社の公開コンテキストごとに個別の公開状態を設定できます。

## 認証されたユーザータイプ {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>アセットを返すには、読み取りアクセス権が必要です。

## パラメータ {#section-009b9006de8e4c16ad657c47f28ace9f}

**入力(setAssetsContextStateParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の取り扱い。 |
| ` *`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | はい | アセットと新しい公開状態の配列。 |

**出力(setAssetsContextStateReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | はい | 正常に変更されたアセットの数。 |
| ` *`warningCount`*` | `xsd:int` | はい | 操作がアセットを変更しようとしたときに生成された警告の数です。 |
| ` *`errorCount`*` | `xsd:int` | はい | 操作でアセットの変更が試みられたときに生成されたエラーの数です。 |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | いいえ | 操作が変更を試みたときにアセットによって生成されたエラーの配列です。 |

## 例 {#section-283a073f3cb14bcda5abed863c538aa4}

次のコード例は、を使用してアセットのパブリケーション状態を設定しま `NotMarkedForPublish`す。

**リクエスト**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**応答**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

