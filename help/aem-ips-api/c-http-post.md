---
description: Dynamic Media ClassicにPOSTをアップロードする場合は、アップロードしたファイルに関連付けられているすべてのログアクティビティを調整するためのジョブを設定する1つ以上のHTTPアセットリクエストが必要になります。
solution: Experience Manager
title: HTTP POSTを使用したUploadFileサーブレットへのアセットのアップロード
feature: Dynamic Media Classic,SDK/API，アセット管理
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 3%

---

# HTTP POSTを使用したUploadFileサーブレットへのアセットのアップロード{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Dynamic Media ClassicにPOSTをアップロードする場合は、アップロードしたファイルに関連付けられているすべてのログアクティビティを調整するためのジョブを設定する1つ以上のHTTPアセットリクエストが必要になります。

次のURLを使用して、UploadFileサーブレットにアクセスします。

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>アップロードPOSTに対するすべてのジョブリクエストは、同じIPアドレスから作成する必要があります。

**Dynamic Media地域のアクセスURL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理的位置 </p> </th> 
   <th colname="col2" class="entry"> <p>実稼動URL </p> </th> 
   <th colname="col3" class="entry"> <p>ステージングURL（実稼動前の開発およびテストに使用） </p> </th> 
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
   <td colname="col1"> <p>Japan/Asia Pacific </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## アップロードジョブのワークフロー {#section-873625b9512f477c992f5cdd77267094}

アップロードジョブは、共通の`jobHandle`を使用して処理を同じジョブに関連付ける1つ以上のHTTP POSTで構成されます。 各要求は`multipart/form-data`エンコードされ、次のフォーム部分で構成されます。

>[!NOTE]
>
>アップロードPOSTに対するすべてのジョブリクエストは、同じIPアドレスから作成する必要があります。

|  HTTPPOSTフォーム部分  |  説明  |
|---|---|
| `auth`  |   必須. 認証情報とクライアント情報を指定するXML authHeaderドキュメント。 [SOAP](/help/aem-ips-api/c-wsdl-versions.md)の&#x200B;**Request authentication**&#x200B;を参照してください。 |
| `file params`  |   オプション. アップロードリクエストごとに、1つ以上のファイルを含めてPOSTできます。 `uploadPostParams/fileName`パラメータが指定されていない場合、各ファイル部分のContent-Dispositionヘッダーにfilenameパラメータを含めることができます。このパラメータは、IPSでターゲットファイル名として使用されます。 |

|  HTTPPOSTフォーム部分   |  uploadPostParams要素名   |  種類   |  説明   |
|---|---|---|---|
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント)   |   `companyHandle`  |  `xsd:string`  | 必須。ファイルのアップロード先の会社に対する処理。  |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `jobName`  |  `xsd:string`  | `jobName`または`jobHandle`が必要です。 アップロードジョブの名前。  |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `jobHandle`  |  `xsd:string`  | `jobName`または`jobHandle`が必要です。 前のリクエストで開始されたアップロードジョブの処理。  |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `locale`  |  `xsd:string`  | （オプション）ローカリゼーションの言語と国コード  |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `description`  |  `xsd:string`  | （オプション）ジョブの説明。  |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `destFolder`  |  `xsd:string`  | （オプション）filenameプロパティにプレフィックスするターゲットフォルダーパス。特に、ファイル名のフルパスをサポートしないブラウザーや他のクライアントの場合に使用します。  |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `fileName`  |  `xsd:string`  | （オプション）ターゲットファイルの名前。 filenameプロパティを上書きします。 |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `endJob`  |  `xsd:boolean`  | （オプション）初期設定は false。 |
| `uploadParams` (必須. アップロードパラメーターを指定するXML `uploadParams`ドキュメント) | `uploadParams`  |  `types:UploadPostJob`  | 既存のアクティブなジョブの後続のリクエストの場合はオプションです。 既存のジョブがある場合、`uploadParams`は無視され、既存のジョブアップロードパラメーターが使用されます。 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)を参照 |

`<uploadPostParams>`ブロック内には、インクルードされたファイルの処理を指定する`<uploadParams>`ブロックが含まれます。

[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)を参照してください。

`uploadParams`パラメーターは、同じジョブの一部として個々のファイルに対して変更される可能性があると想定するかもしれませんが、そうではありません。 ジョブ全体に同じ`uploadParams`パラメーターを使用します。

新しいアップロードジョブの最初のPOSTリクエストでは、`jobName`パラメーターを指定し、できれば一意のジョブ名を使用して、後続のジョブステータスポーリングとジョブログクエリを簡略化する必要があります。 同じアップロードジョブに対する追加のPOSTリクエストでは、最初のリクエストから返された`jobHandle`値を使用して、`jobName`ではなく`jobHandle`パラメーターを指定する必要があります。

アップロードジョブの最終POSTリクエストでは、`endJob`パラメーターをtrueに設定して、今後、このジョブに対してPOSTされるファイルがないようにする必要があります。 これにより、すべてのPOST済みファイルが取り込まれた直後にジョブを完了できます。 そうしないと、30分以内に追加のPOSTリクエストを受信しない場合、ジョブはタイムアウトします。

## UploadPOST応答 {#section-421df5cc04d44e23a464059aad86d64e}

POSTリクエストが成功した場合、応答本文はXML `uploadPostReturn`ドキュメントになります。XSDは以下で指定されています。

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

返された`jobHandle`は、同じジョブに対する後続のPOSTリクエストの`uploadPostParams`/ `jobHandle`パラメーターに渡されます。 また、`getActiveJobs`操作でジョブステータスをポーリングしたり、`getJobLogDetails`操作でジョブのログを照会したりする場合にも使用できます。

POSTリクエストの処理中にエラーが発生した場合、応答本文は[Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)で説明されているAPI障害タイプの1つで構成されます。

## POSTリクエストの例 {#section-810fe32abdb9426ba0fea488dffadd1e}

```
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

## POST応答の例 — 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## POST応答の例 — エラー {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
