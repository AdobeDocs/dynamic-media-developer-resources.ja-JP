---
description: 公開用にマークされたアセットの公開コンテキストを返します。
solution: Experience Manager
title: batchGetAssetPublishContexts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ba1f62a7-2698-4300-b6de-6d07ac764b0c
TQID: 'https://experienceleague.adobe.com/ei78NEtlPaqhT6Vf-jreBAxzfGcwGbxMLSsOfSb-Ym4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 13%

---

# batchGetAssetPublishContexts{#batchgetassetpublishcontexts}

公開用にマークされたアセットの公開コンテキストを返します。

構文

## 承認済みユーザータイプ {#section-d5362ca8a6ab42949cd648ba38dbf2f8}

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
>* すべてのユーザーは共有会社にアクセスできます。
>

## パラメーター {#section-1742fcb196224545b270eb8241f757a8}

**入力（batchGetAssetPublishContextsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社への取り扱い。 |
| assetHandleArray | ` `types:HandleArray&quot; | はい | アクティブな（パブリッシュ用にマークされた）コンテキスト用にクエリするアセットのリスト。 |

**出力（batchGetAssetPublishContextsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| assetPublishContextsArray | `types:assetPublishContextsArray` | はい | 各アセットが公開用にマークされた公開コンテキストの配列。 |

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

