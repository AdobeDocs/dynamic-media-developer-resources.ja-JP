---
description: 公開用にマークされたアセットの公開コンテキストを返します。
solution: Experience Manager
title: batchGetAssetPublishContexts
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 16%

---


# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

公開用にマークされたアセットの公開コンテキストを返します。

構文

## 認証済みユーザータイプ{#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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
>* すべてのユーザーは共有会社ーにアクセスできます。

>



## パラメータ {#section-1742fcb196224545b270eb8241f757a8}

**入力(batchGetAssetPublishContextsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 会社へのハンドル。 |
| `*`assetHandleArray`*` | ` `types:HandleArray&quot; | はい | アクティブな（公開用にマークされた）コンテキストにクエリするアセットのリスト。 |

**出力(batchGetAssetPublishContextsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetPublishContextsArray`*` | `types:assetPublishContextsArray` | はい | 各アセットが公開用にマークされる公開コンテキストの配列。 |

## 例 {#section-457f6809ccfa425b9a0976313d613f4e}

**リクエスト**

```java
<batchGetAssetPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetHandleArray>
    <items>a|27007</items>
    <items>a|27008</items>
  </assetHandleArray>
</batchGetAssetPublishContextsParam>
```

**応答**

```java
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

