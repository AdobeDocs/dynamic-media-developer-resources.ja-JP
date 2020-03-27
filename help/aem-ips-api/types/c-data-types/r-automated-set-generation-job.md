---
description: アセットハンドルリスト配列を使用して、ファイルをセットにグループ化します。
seo-description: アセットハンドルリスト配列を使用して、ファイルをセットにグループ化します。
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
topic: Scene7 Image Production System API
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

アセットハンドルリスト配列を使用して、ファイルをセットにグループ化します。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：HandleArray</span> </td> 
   <td colname="col3">セットの作成に使用されるアセットハンドルの配列。 <p>デフォルトでは、配列に含めることができるアセットの最大数は1000です。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> セットを保存するフォルダのパス。 デフォルトで、会社のルートフォルダに保存します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> アセットを発行するかどうかを示すフラグを設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> autoSetCreationOptions <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AutoSetCreationOptions</span> </td> 
   <td colname="col3">アップロードされたファイルで実行できるセット生成スクリプトの配列。 AutoSetCreationOptionsを参照してく <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> ださい</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 電子メ <span class="varname"> ール設定</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>ジョブの自動電子メール通知を設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting Options**

このパラメ `emailSetting` ーターには、次のオプションが含まれます。

| オプション | 戻り値 |
|---|---|
| `All` | 指定された受信者に対するすべてのジョブ通知（エラー、警告、完了）。 |
| `Error` | 指定された受信者に対するジョブエラー。 |
| `ErrorAndWarning` | 指定された受信者に対するジョブエラーと警告。 |
| `JobCompletion` | 指定された受信者に対するジョブ完了の通知。 |
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

