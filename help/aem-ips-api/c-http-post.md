---
title: HTTP POST を使用した UploadFile サーブレットへのアセットのアップロード
description: ' [!DNL Dynamic Media] Classic へのアセットのアップロードには 1 つ以上の HTTP POST リクエストが必要で、アップロードされたファイルに関連付けられたすべてのログアクティビティを調整するジョブを設定します。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# HTTP POST を使用した UploadFile サーブレットへのアセットのアップロード{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Dynamic Media Classicへのアセットのアップロードには 1 つ以上の HTTP POST リクエストが関与し、アップロードされたファイルに関連付けられたすべてのログアクティビティを調整するジョブを設定します。

次の URL を使用して、UploadFile サーブレットにアクセスします。

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>アップロードジョブのすべての POST リクエストは、同じ IP アドレスから送信する必要があります。

**Dynamic Media 地域のアクセス URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理的位置 </p> </th> 
   <th colname="col2" class="entry"> <p>実稼動 URL </p> </th> 
   <th colname="col3" class="entry"> <p>ステージング URL （実稼動前の開発およびテストに使用） </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>北米 </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ヨーロッパ、中東、アジア </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本/アジア太平洋 </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## アップロードジョブのワークフロー {#section-873625b9512f477c992f5cdd77267094}

アップロードジョブは、共通の `jobHandle` を使用して処理を同じジョブに関連付ける 1 つ以上の HTTP POST で構成されます。 各リクエストは `multipart/form-data` にエンコードされ、次のフォーム部分で構成されます。

>[!NOTE]
>
>アップロードジョブのすべての POST リクエストは、同じ IP アドレスから送信する必要があります。

|  HTTP POST フォーム部分  |  説明  |
|---|---|
| `auth`  |   必須。 認証およびクライアント情報を指定する XML authHeader ドキュメント。 **2&rbrace;SOAP** の「リクエスト認証 [」を参照してください。](/help/aem-ips-api/c-wsdl-versions.md) |
| `file params`  |   オプション。 POST リクエストごとに、アップロードする 1 つ以上のファイルを含めることができます。 各ファイル部分には、Content-Disposition ヘッダーに filename パラメーターを含めることができます。このパラメーターは、`uploadPostParams/fileName` パラメーターが指定されていない場合に、IPS でターゲットファイル名として使用されます。 |

|  HTTP POST フォーム部分   |  uploadPostParams 要素名   |  タイプ   |  説明   |
|---|---|---|---|
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント）   |   `companyHandle`  |  `xsd:string`  | 必須。 ファイルのアップロード先の会社を表すハンドル。  |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `jobName`  |  `xsd:string`  | `jobName` または `jobHandle` のいずれかが必要です。 アップロードジョブの名前。  |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `jobHandle`  |  `xsd:string`  | `jobName` または `jobHandle` のいずれかが必要です。 前のリクエストで開始されたアップロードジョブへのハンドル。  |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `locale`  |  `xsd:string`  | オプション。 ローカライゼーションの言語と国コード。  |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `description`  |  `xsd:string`  | オプション。 ジョブの説明。  |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `destFolder`  |  `xsd:string`  | オプション。 ファイル名プロパティのプレフィックスとして使用されるターゲットフォルダーパス。特に、ファイル名でフルパスをサポートしていないブラウザーや他のクライアントの場合に有効です。  |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `fileName`  |  `xsd:string`  | オプション。 ターゲットファイルの名前。 filename プロパティを上書きします。 |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `endJob`  |  `xsd:boolean`  | オプション。 初期設定は false。 |
| `uploadParams` （必須。 アップロードパラメーターを指定する XML `uploadParams` ドキュメント） | `uploadParams`  |  `types:UploadPostJob`  | 既存のアクティブなジョブに対する後続のリクエストである場合はオプションです。 既存のジョブがある場合、`uploadParams` は無視され、既存のジョブアップロードパラメーターが使用されます。 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) を参照してください |

`<uploadPostParams>` ブロック内には、含まれるファイルの処理を指定する `<uploadParams>` ブロックがあります。

[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) を参照してください。

`uploadParams` のパラメータは、同じジョブの一部として個々のファイルに対して変更される可能性があると仮定しますが、そうではありません。 ジョブ全体に同じ `uploadParams` パラメーターを使用します。

新しいアップロードジョブに対する最初の POST リクエストでは、`jobName` パラメーターを指定する必要があります。一意のジョブ名を使用して、その後のジョブステータスのポーリングやジョブログのクエリを簡略化することをお勧めします。 同じアップロードジョブに対する追加の POST リクエストでは、最初のリクエストから返された `jobHandle` 値を使用して、`jobName` ではなく `jobHandle` パラメーターを指定する必要があります。

アップロードジョブの最後の POST リクエストでは、`endJob` パラメーターを true に設定して、このジョブに対して今後ファイルが POST されないようにする必要があります。 これにより、すべての POSTed ファイルが取り込まれた直後にジョブが完了します。 それ以外の場合、30 分以内に追加の POST リクエストを受信しないと、ジョブはタイムアウトします。

## UploadPOST 応答 {#section-421df5cc04d44e23a464059aad86d64e}

POST リクエストが成功した場合、応答本文は XML `uploadPostReturn` ドキュメントになります。これは、XSD が以下で指定するからです。

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

返された `jobHandle` は、同じジョブに対する後続の POST リクエストの `uploadPostParams`/ `jobHandle` パラメーターに渡されます。 また、`getActiveJobs` 操作でジョブステータスをポーリングしたり、`getJobLogDetails` 操作でジョブのログをクエリしたりすることもできます。

POST リクエストの処理中にエラーが発生した場合、応答本文は、[ フォールト ](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b) に説明されているように、API フォールトタイプの 1 つで構成されます。

## POST リクエストの例 {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## POST 応答の例 – 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## POST 応答の例 – エラー {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
