---
description: アセットをScene7プロダクションシステムにアップロードするには、アップロードしたファイルに関連付けられたすべてのログアクティビティを調整するためにジョブを設定する1つ以上のHTTPPOST要求が必要です。
seo-description: アセットをScene7プロダクションシステムにアップロードするには、アップロードしたファイルに関連付けられたすべてのログアクティビティを調整するためにジョブを設定する1つ以上のHTTPPOST要求が必要です。
seo-title: HTTP POSTを使用したUploadFileサーブレットへのアセットのアップロード
solution: Experience Manager
title: HTTP POSTを使用したUploadFileサーブレットへのアセットのアップロード
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: 5d738b675975251dc3491ac7ae533eda082df134
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 3%

---


# HTTP POSTを使用したアセットのUploadFile Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}へのアップロード

アセットをScene7プロダクションシステムにアップロードするには、アップロードしたファイルに関連付けられたすべてのログアクティビティを調整するためにジョブを設定する1つ以上のHTTPPOST要求が必要です。

次のURLを使用してUploadFileサーブレットにアクセスします。

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST要求は、同じIPアドレスから送信される必要があります。

**Scene7地域のアクセスURL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理的位置 </p> </th> 
   <th colname="col2" class="entry"> <p>実稼動URL </p> </th> 
   <th colname="col3" class="entry"> <p>ステージングURL（実稼働前の開発およびテストに使用） </p> </th> 
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

## アップロードジョブ{#section-873625b9512f477c992f5cdd77267094}のワークフロー

アップロードジョブは、共通の`jobHandle`を使用して処理を同じジョブに関連付ける1つ以上のHTTP POSTで構成されます。 各リクエストは`multipart/form-data`エンコードされ、次のフォーム部分で構成されます。

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST要求は、同じIPアドレスから送信される必要があります。

|  HTTPPOSTフォーム部分  |  説明  |
|---|---|
| `auth`  |   必須. 認証とクライアント情報を指定するXML authHeaderドキュメント。 「[SOAP](/help/aem-ips-api/c-wsdl-versions.md)の下の&#x200B;**認証を要求**」を参照してください。 |
| `file params`  |   オプション. POST要求ごとに、アップロードするファイルを1つ以上含めることができます。 `uploadPostParams/fileName`パラメータが指定されていない場合、各ファイルパーツにはContent-Dispositionヘッダにfilenameパラメータを含めることができます。このパラメータは、IPSでターゲットファイル名として使用されます。 |

|  HTTPPOSTフォーム部分   |  uploadPostParams要素名   |  種類   |  説明   |
|---|---|---|---|
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント)   |   `companyHandle`  |  `xsd:string`  | 必須。ファイルのアップロード先の会社へのハンドル。  |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `jobName`  |  `xsd:string`  | `jobName`または`jobHandle`が必要です。 アップロードジョブの名前。  |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `jobHandle`  |  `xsd:string`  | `jobName`または`jobHandle`が必要です。 以前の要求で開始されたアップロードジョブへのハンドル。  |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `locale`  |  `xsd:string`  | （オプション）ローカライゼーションの言語および国コード。  |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `description`  |  `xsd:string`  | （オプション）ジョブの説明。  |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `destFolder`  |  `xsd:string`  | （オプション）ファイル名プロパティのプレフィックスにするターゲットフォルダーのパス。特に、ファイル名のフルパスをサポートしていないブラウザーや他のクライアントの場合に使用します。  |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `fileName`  |  `xsd:string`  | （オプション）ターゲットファイルの名前。 filenameプロパティを上書きします。 |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `endJob`  |  `xsd:boolean`  | （オプション）初期設定は false。 |
| `uploadParams` (必須. (アップロードパラメータを指定するXML `uploadParams`ドキュメント) | `uploadParams`  |  `types:UploadPostJob`  | 既存のアクティブなジョブに対する後続の要求の場合はオプションです。 既存のジョブがある場合、`uploadParams`は無視され、既存のジョブアップロードパラメーターが使用されます。 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)を参照 |

`<uploadPostParams>`ブロック内には`<uploadParams>`ブロックがあり、含まれるファイルの処理を指定します。

[UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)を参照してください。

`uploadParams`パラメーターは、同じジョブの一部として個々のファイルに対して変更できると想定することもできますが、そうではありません。 ジョブ全体で同じ`uploadParams`パラメーターを使用します。

新しいアップロードジョブに対する最初のPOST要求では、`jobName`パラメーターを指定する必要があります。できれば、一意のジョブ名を使用して、以降のジョブステータスのポーリングとジョブログのクエリを簡素化します。 同じアップロードジョブに対する追加のPOSTリクエストでは、`jobName`の代わりに`jobHandle`パラメーターを指定し、最初のリクエストから返された`jobHandle`値を使用する必要があります。

アップロードジョブに対する最終POSTリクエストでは、`endJob`パラメーターをtrueに設定し、今後、このジョブに対してファイルがPOSTされないようにする必要があります。 これにより、すべてのPOSTedファイルが取り込まれた後すぐにジョブを完了できます。 それ以外の場合は、30分以内に追加のPOST要求が受信されない場合、ジョブはタイムアウトします。

## UploadPOST応答{#section-421df5cc04d44e23a464059aad86d64e}

POSTリクエストが成功した場合、応答本文はXML `uploadPostReturn`ドキュメントになります。XSDは次のように指定します。

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

返された`jobHandle`は、同じジョブに対する後続のPOSTリクエストの`uploadPostParams`/ `jobHandle`パラメーターに渡されます。 また、`getActiveJobs`操作でジョブステータスをポーリングしたり、`getJobLogDetails`操作でジョブログをクエリしたりする場合にも使用できます。

POST要求の処理中にエラーが発生した場合、応答本文は、[Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)で説明されているAPI障害タイプの1つで構成されます。

## POSTリクエストの例{#section-810fe32abdb9426ba0fea488dffadd1e}

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

## POSTレスポンスの例 — success {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## POST応答の例 — エラー{#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

