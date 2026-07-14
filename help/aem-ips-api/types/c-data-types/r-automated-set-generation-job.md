---
description: アセットハンドルリスト配列を使用してファイルをセットにグループ化します。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
TQID: 'https://experienceleague.adobe.com/YHElzYMAYDta1hG2th30GNuz2IgFmN5OTUPx63K1p9o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 3%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

アセットハンドルリスト配列を使用してファイルをセットにグループ化します。

構文

## パラメーター {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">種類：HandleArray</span> </td> 
   <td colname="col3">セットの作成に使用されるアセットハンドルの配列。 <p>デフォルトでは、配列に含めることができるアセットの最大数は1000です。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> セットを保存するフォルダーへのパス。 デフォルトで会社のルートフォルダーに保存します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> アセットを公開するかどうかを示すフラグを設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph">種類：AutoSetCreationOptions</span> </td> 
   <td colname="col3">アップロードされたファイルで実行できるセット生成スクリプトの配列。 <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local">のAutoSetCreationOptions</a>を参照してください</td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ジョブの自動メール通知を設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting オプション**

`emailSetting` パラメーターには、次のオプションが含まれます。

| オプション | 返品 |
|---|---|
| `All` | 指定された受信者へのすべてのジョブ通知（エラー、警告、完了）。 |
| `Error` | 指定された受信者に対するジョブのエラー。 |
| `ErrorAndWarning` | 指定された受信者に対するジョブエラーと警告。 |
| `JobCompletion` | 指定された受信者へのジョブ完了通知。 |
| `None` | ジョブは、指定された受信者にジョブ通知を送信しません。 |

## 例 {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

