---
title: UploadFile サーブレットへのHTTP POSTによるアセットのアップロード
description: アセットを [!DNL Dynamic Media] Classicにアップロードするには、1つ以上のHTTP POST リクエストが必要で、アップロードしたファイルに関連するすべてのログアクティビティを調整するジョブを設定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
TQID: 'https://experienceleague.adobe.com/-sHJjbnmxKSlU8TiOx96f1fgRUVWElHZ6KAqhy0HW0c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 716
ht-degree: 1%

---

# UploadFile サーブレットへのHTTP POSTによるアセットのアップロード{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

アセットをDynamic Media Classicにアップロードするには、1つ以上のHTTP POST リクエストが必要です。このリクエストは、アップロードされたファイルに関連するすべてのログアクティビティを調整するジョブを設定します。

UploadFile サーブレットにアクセスするには、次のURLを使用します。

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST リクエストは、同じIP アドレスから送信する必要があります。

**Dynamic Media地域のURLへのアクセス**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地域 </p> </th> 
   <th colname="col2" class="entry"> <p>実稼動URL </p> </th> 
   <th colname="col3" class="entry"> <p>ステージング URL （プリプロダクション開発およびテストに使用） </p> </th> 
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

アップロードジョブは、共通の`jobHandle`を使用して処理を同じジョブに関連付ける1つ以上のHTTP POSTで構成されます。 各リクエストは`multipart/form-data`でエンコードされ、次のフォームパーツで構成されます。

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST リクエストは、同じIP アドレスから送信する必要があります。

|  HTTP POST フォームパーツ  |  説明  |
|---|---|
| `auth`  |   必須。 認証とクライアント情報を指定するXML authHeader ドキュメント。 [SOAP](/help/aem-ips-api/c-wsdl-versions.md)の「**認証をリクエスト**」を参照してください。 |
| `file params`  |   オプション。 POST リクエストごとにアップロードする1つ以上のファイルを含めることができます。 各ファイル部分には、Content-Disposition ヘッダーにファイル名パラメーターを含めることができます。このヘッダーは、`uploadPostParams/fileName` パラメーターが指定されていない場合にIPSでターゲットファイル名として使用されます。 |

|  HTTP POST フォームパーツ   |  uploadPostParams要素名   |  種類   |  説明   |
|---|---|---|---|
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント）   |   `companyHandle`  |  `xsd:string`  | 必須。 ファイルのアップロード先の会社に対するハンドル。  |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `jobName`  |  `xsd:string`  | `jobName`または`jobHandle`が必要です。 アップロードジョブの名前。  |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `jobHandle`  |  `xsd:string`  | `jobName`または`jobHandle`が必要です。 前のリクエストで開始されたアップロードジョブへのハンドル。  |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `locale`  |  `xsd:string`  | オプション。 ローカライゼーション用の言語と国コード。  |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `description`  |  `xsd:string`  | オプション。 ジョブの説明。  |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `destFolder`  |  `xsd:string`  | オプション。 特に、ファイル名のフルパスをサポートしていないブラウザーやその他のクライアントの場合は、ファイル名プロパティのプレフィックスのターゲットフォルダーパスです。  |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `fileName`  |  `xsd:string`  | オプション。 ターゲットファイルの名前。 ファイル名プロパティを上書きします。 |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `endJob`  |  `xsd:boolean`  | オプション。 初期設定は false。 |
| `uploadParams` （必須）。 アップロードパラメーターを指定するXML `uploadParams` ドキュメント） | `uploadParams`  |  `types:UploadPostJob`  | 既存のアクティブなジョブに対する後続のリクエストの場合は、オプションです。 既存のジョブがある場合、`uploadParams`は無視され、既存のジョブアップロードパラメーターが使用されます。 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)を参照 |

`<uploadPostParams>` ブロック内には、含まれるファイルの処理を指定する`<uploadParams>` ブロックがあります。

[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)を参照してください。

`uploadParams` パラメーターは、同じジョブの一部として個々のファイルに対して変更できると仮定することもできますが、そうではありません。 ジョブ全体に同じ`uploadParams` パラメーターを使用します。

新しいアップロードジョブの最初のPOST リクエストでは、`jobName` パラメーターを指定する必要があります。好ましくは、後続のジョブステータスポーリングとジョブログクエリを簡素化するために一意のジョブ名を使用します。 同じアップロードジョブに対する追加のPOST リクエストでは、最初のリクエストから返された`jobHandle`値を使用して、`jobName`ではなく`jobHandle` パラメーターを指定する必要があります。

アップロードジョブの最後のPOST リクエストでは、`endJob` パラメーターをtrueに設定して、このジョブに対して将来のファイルがPOSTされないようにする必要があります。 これにより、POSTされたファイルがすべて取り込まれた直後にジョブを完了できます。 それ以外の場合、追加のPOST リクエストが30分以内に受信されない場合、ジョブはタイムアウトします。

## UploadPOST応答 {#section-421df5cc04d44e23a464059aad86d64e}

POST リクエストが成功した場合、XSDが次のように指定するので、応答の本文はXML `uploadPostReturn` ドキュメントです。

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

返された`jobHandle`は、同じジョブに対する後続のPOST要求に対して、`uploadPostParams`/`jobHandle` パラメーターで渡されます。 また、`getActiveJobs`操作でジョブの状態をポーリングしたり、`getJobLogDetails`操作でジョブログをクエリしたりすることもできます。

POST リクエストの処理中にエラーが発生した場合、応答本文は、[Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)で説明されているいずれかのAPI障害タイプで構成されます。

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

## POST応答の例 – 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## POST応答の例 – エラー {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
