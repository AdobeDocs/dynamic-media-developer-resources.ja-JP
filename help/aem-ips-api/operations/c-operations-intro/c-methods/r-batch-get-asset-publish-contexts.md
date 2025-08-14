---
description: 公開用にマークされたアセットの公開コンテキストを返します。
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 13%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

公開用にマークされたアセットの公開コンテキストを返します。

構文

## 許可されているユーザータイプ {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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
>* アセットを返すには、ユーザーに読み取りアクセス権が必要です。
>* すべてのユーザーは、共有会社にアクセスできます。
>

## パラメーター {#section-1742fcb196224545b270eb8241f757a8}

**入力（batchGetAssetPublishContextsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社に渡す。 |
| assetHandleArray | ` `types:HandleArray&quot; | はい | アクティブな（公開用にマークされた）コンテキストに対してクエリするアセットのリスト。 |

**出力（batchGetAssetPublishContextsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | はい | 各アセットが公開用にマークされるパブリッシュコンテキストの配列。 |

## 例 {#section-457f6809ccfa425b9a0976313d613f4e}

**リクエスト**

```java {.line-numbers}
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**応答**

```java {.line-numbers}
<batchGetAssetPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <assetPublishContextsArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <contextName>ImageServing</contextName>
          <contextType>ImageServing</contextType>
        </items>
      </publishContextArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <publishContextArray>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <contextName>Video</contextName>
          <contextType>Video</contextType>
        </items>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <contextName>ImageRendering</contextName>
          <contextType>ImageRendering</contextType>
        </items>
      </publishContextArray>
    </items>
  </assetPublishContextsArray>
</batchGetAssetPublishContextsReturn>
```
