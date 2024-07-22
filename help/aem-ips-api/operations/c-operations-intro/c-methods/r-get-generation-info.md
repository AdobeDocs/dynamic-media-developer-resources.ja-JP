---
description: 渡されたパラメーターに基づいて、2 つの異なるタイプの情報を返します。 originatorHandle は、指定したアセットから生成されたアセットに関する情報を返します。 generateHandle は、指定したアセットまたはファイルの生成に使用された手順に関する情報を返します。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 8%

---

# getGenerationInfo{#getgenerationinfo}

渡されたパラメーターに基づいて、2 つの異なるタイプの情報を返します。 originatorHandle は、指定したアセットから生成されたアセットに関する情報を返します。 generateHandle は、指定したアセットまたはファイルの生成に使用された手順に関する情報を返します。

構文

## 許可されているユーザータイプ {#section-9cc2216b32c74107be07aeacecc11401}

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
| コードフレーズ | `xsd:string` | はい | 会社へのハンドル。 |
| コードフレーズ | `xsd:string` | いいえ | 世代で使用されたエンジン。 フォントスタイルを参照してください。 |
| コードフレーズ | `xsd:string` | いいえ | 生成されたアセットをクエリするアセットのハンドル。 |
| コードフレーズ | `xsd:string` | いいえ | 生成で使用されるアセットとエンジンをクエリするアセットのハンドル。 |
| コードフレーズ | `xsd:StringArray` | いいえ | 操作に含まれるプロパティ。 |
| コードフレーズ | `xsd:StringArray` | いいえ | 操作から除外されたプロパティ。 |

**出力（getGenerationInfoReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | はい | 世代情報の配列。 |

## 例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

このコードサンプルは、特定のアセットから生成されたアセットに関する情報を返します。 指定したアセットの生成に使用された手順に関する情報は取得しません。 簡潔にするために、応答は切り捨てられます。

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
