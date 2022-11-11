---
description: アセットハンドルリスト配列を使用してファイルをセットにグループ化します。
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 4%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

アセットハンドルリスト配列を使用してファイルをセットにグループ化します。

構文

## パラメータ {#section-939b2e6946a64238be3709fec2cd0b84}

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
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">セットの作成に使用されるアセットハンドルの配列。 <p>デフォルトでは、配列に含めることができるアセットの最大数は 1000 です。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> セットを保存するフォルダーのパス。 デフォルトで会社のルートフォルダに保存されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> アセットを公開するかどうかを示すフラグを設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreationOptions</span> </td> 
   <td colname="col3">アップロードしたファイルで実行できるセット生成スクリプトの配列。 詳しくは、 <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ジョブの自動電子メール通知を設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting Options**

この `emailSetting` パラメーターには次のオプションが含まれます。

| オプション | 戻り値 |
|---|---|
| `All` | 指定した受信者へのすべてのジョブ通知（エラー、警告、完了）。 |
| `Error` | 指定した受信者に対するジョブエラー。 |
| `ErrorAndWarning` | 指定した受信者に対するジョブのエラーと警告。 |
| `JobCompletion` | 指定した受信者へのジョブ完了通知。 |
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
