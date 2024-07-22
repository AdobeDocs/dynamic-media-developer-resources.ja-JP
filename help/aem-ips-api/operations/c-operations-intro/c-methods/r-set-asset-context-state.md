---
description: 1 つ以上のアセットの公開状態を設定または更新します。 会社内の公開コンテキストごとに個別の公開状態を設定できます。
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 28d0a67b-3e36-43fc-800d-17c841dca3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 9%

---

# setAssetsContextState{#setassetscontextstate}

1 つ以上のアセットの公開状態を設定または更新します。 会社内の公開コンテキストごとに個別の公開状態を設定できます。

## 許可されているユーザータイプ {#section-815eb031f85143278c1560c18c5e3431}

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
>アセットを返すには、ユーザーに読み取りアクセス権が必要です。

## パラメーター {#section-009b9006de8e4c16ad657c47f28ace9f}

**入力（setAssetsContextStateParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に渡す。 |
| assetsContextHandle | `types:AssetsContextStateUpdateArray` | はい | アセットとその新しい公開状態の配列。 |

**出力（setAssetsContexStateReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| successCount | `xsd:int` | はい | アセット数が正常に変更されました。 |
| warningCount | `xsd:int` | はい | 操作でアセットを変更しようとしたときに生成された警告の数。 |
| errorCount | `xsd:int` | はい | 操作でアセットを変更しようとしたときに生成されたエラーの数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | いいえ | 操作がアセットを変更しようとしたときにアセットによって生成されたエラーの配列。 |

## 例 {#section-283a073f3cb14bcda5abed863c538aa4}

次のコードのサンプルでは、`NotMarkedForPublish` を使用してアセットの公開状態を設定します。

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
