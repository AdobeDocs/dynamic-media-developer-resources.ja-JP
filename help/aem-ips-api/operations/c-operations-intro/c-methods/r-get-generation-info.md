---
description: 渡されたパラメーターに基づいて2種類の情報を返します。 originatorHandleは、指定したアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用された手順に関する情報を返します。
seo-description: 渡されたパラメーターに基づいて2種類の情報を返します。 originatorHandleは、指定したアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用された手順に関する情報を返します。
seo-title: getGenerationInfo
solution: Experience Manager
title: getGenerationInfo
topic: Scene7 Image Production System API
uuid: 4310a702-c08b-4479-9f57-9f2bc1d6b032
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getGenerationInfo{#getgenerationinfo}

渡されたパラメーターに基づいて2種類の情報を返します。 originatorHandleは、指定したアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用された手順に関する情報を返します。

構文

## 認証されたユーザータイプ {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-b7fa94c82147455888e8469fa5f6922b}

**入力(getGenerationInfoParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`コードフレーズ`*` | `xsd:string` | はい | 会社の取っ手。 |
| ` *`コードフレーズ`*` | `xsd:string` | いいえ | その世代で使用されたエンジン。 フォントスタイルを参照してください。 |
| ` *`コードフレーズ`*` | `xsd:string` | いいえ | 生成されたアセットを照会するアセットのハンドル。 |
| ` *`コードフレーズ`*` | `xsd:string` | いいえ | 生成時に使用されるアセットとエンジンを照会するアセットのハンドル。 |
| ` *`コードフレーズ`*` | `xsd:StringArray` | いいえ | 操作に含まれるプロパティ。 |
| ` *`コードフレーズ`*` | `xsd:StringArray` | いいえ | 操作から除外されるプロパティ。 |

**出力(getGenerationInfoReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`generationArray`*` | `types:GenerationInfoArray` | はい | 生成情報の配列。 |

## 例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

このコードサンプルを使用すると、特定のアセットから生成されたアセットに関する情報を返すことができます。 指定したアセットの生成に使用された手順に関する情報は取得されません。 応答は簡潔にするために切り捨てられます。

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

