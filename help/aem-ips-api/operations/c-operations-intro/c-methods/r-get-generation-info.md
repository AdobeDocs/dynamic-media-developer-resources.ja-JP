---
description: 渡されたパラメーターに基づいて、2種類の異なる情報を返します。 originatorHandleは、指定されたアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用した手順に関する情報を返します。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
TQID: 'https://experienceleague.adobe.com/MA0SJinQzPjDFkSXVRhH2e7A3Ry6HXoW--K-elv028M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 8%

---

# getGenerationInfo{#getgenerationinfo}

渡されたパラメーターに基づいて、2種類の異なる情報を返します。 originatorHandleは、指定されたアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用した手順に関する情報を返します。

構文

## 承認済みユーザータイプ {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-b7fa94c82147455888e8469fa5f6922b}

**入力（getGenerationInfoParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| コードフレーズ | `xsd:string` | はい | 会社のハンドルです。 |
| コードフレーズ | `xsd:string` | いいえ | この世代で使われたエンジン。 フォントスタイルを参照してください。 |
| コードフレーズ | `xsd:string` | いいえ | 生成されたアセットに対してクエリを実行するアセットのハンドル。 |
| コードフレーズ | `xsd:string` | いいえ | 生成で使用されるアセットとエンジンに対してクエリを実行するアセットのハンドル。 |
| コードフレーズ | `xsd:StringArray` | いいえ | 操作に含まれるプロパティ。 |
| コードフレーズ | `xsd:StringArray` | いいえ | 操作から除外されたプロパティ。 |

**出力（getGenerationInfoReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | はい | 生成情報の配列。 |

## 例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

このコードサンプルは、特定のアセットから生成されたアセットに関する情報を返します。 指定したアセットの生成に使用した手順に関する情報は取得されません。 簡潔にするために、応答は切り捨てられます。

**リクエスト**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**応答**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```

