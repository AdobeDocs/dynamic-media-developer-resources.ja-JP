---
description: 渡されたパラメーターに基づいて、2つの異なるタイプの情報を返します。 originatorHandleは、指定したアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用する手順に関する情報を返します。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 9%

---

# getGenerationInfo{#getgenerationinfo}

渡されたパラメーターに基づいて、2つの異なるタイプの情報を返します。 originatorHandleは、指定したアセットから生成されたアセットに関する情報を返します。 generateHandleは、指定したアセットまたはファイルの生成に使用する手順に関する情報を返します。

構文

## 許可されたユーザーの種類 {#section-9cc2216b32c74107be07aeacecc11401}

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
| `*`コードフレーズ`*` | `xsd:string` | はい | 会社の取っ手。 |
| `*`コードフレーズ`*` | `xsd:string` | いいえ | その世代で使われたエンジン。 フォントスタイルを参照してください。 |
| `*`コードフレーズ`*` | `xsd:string` | いいえ | 生成されたアセットに対してクエリを実行するアセットのハンドル。 |
| `*`コードフレーズ`*` | `xsd:string` | いいえ | 生成に使用されるアセットとエンジンを問い合わせるためのアセットのハンドル。 |
| `*`コードフレーズ`*` | `xsd:StringArray` | いいえ | 操作に含まれるプロパティ。 |
| `*`コードフレーズ`*` | `xsd:StringArray` | いいえ | 操作から除外されたプロパティ。 |

**出力(getGenerationInfoReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`generationArray`*` | `types:GenerationInfoArray` | はい | 生成情報の配列。 |

## 例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

このコードサンプルは、特定のアセットから生成されたアセットに関する情報を返します。 指定されたアセットの生成に使用される手順に関する情報は取得されません。 簡潔にするために応答は切り捨てられます。

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
