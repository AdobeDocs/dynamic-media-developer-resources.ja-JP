---
description: アセットをScene7 Production Systemにアップロードするには、アップロードされたファイルに関連付けられたすべてのログアクティビティを調整するジョブを設定する1つ以上のHTTP POST要求が必要です。
seo-description: アセットをScene7 Production Systemにアップロードするには、アップロードされたファイルに関連付けられたすべてのログアクティビティを調整するジョブを設定する1つ以上のHTTP POST要求が必要です。
seo-title: HTTP POSTを使用したアセットのUploadFileサーブレットへのアップロード
solution: Experience Manager
title: HTTP POSTを使用したアセットのUploadFileサーブレットへのアップロード
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# HTTP POSTを使用したアセットのUploadFileサーブレットへのアップロード{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

アセットをScene7 Production Systemにアップロードするには、アップロードされたファイルに関連付けられたすべてのログアクティビティを調整するジョブを設定する1つ以上のHTTP POST要求が必要です。

次のURLを使用して、UploadFileサーブレットにアクセスします。

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST要求は、同じIPアドレスから送信される必要があります。

**Scene7領域のURLへのアクセス**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地理的な場所 </p> </th> 
   <th colname="col2" class="entry"> <p>実稼働URL </p> </th> 
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

## アップロードジョブのワークフロー {#section-873625b9512f477c992f5cdd77267094}

アップロードジョブは、処理を同じジョブに関連付けるために共通のHTTP POSTを `jobHandle` 使用する1つ以上のHTTP POSTで構成されます。 各リクエストはエンコ `multipart/form-data` ードされ、次のフォームの部分で構成されます。

>[!NOTE]
>
>アップロードジョブに対するすべてのPOST要求は、同じIPアドレスから送信される必要があります。

| HTTP POSTフォームの部分|説明||-|-||`auth`|必須。 認証とクライアント情報を指定するXML authHeaderドキュメント。 **SOAPのRequest authentication** を参照し [てください](/help/aem-ips-api/c-wsdl-versions.md)。 |
|`file params` |  オプション. 各POSTリクエストでアップロードするファイルを1つ以上含めることができます。 各ファイルパーツは、Content-Dispositionヘッダにfilenameパラメータを含めることができます。このパラメータは、パラメータが指定されていない場合にIPSでターゲットファイル名として使 `uploadPostParams/fileName` 用されます。 |

| HTTP POSTフォームパーツ| uploadPostParams要素名|タイプ|説明||-|-|-|-||`uploadParams` (必須。 アップロード `uploadParams` パラメーターを指定するXMLドキュメ `companyHandle`ント) |`xsd:string`| Required。 ファイルのアップロード先の会社に対する処理。 |
|`uploadParams` (必須. アップロード `uploadParams` パラメータを指定するXMLドキュメント)|`jobName`|`xsd:string`| Exther `jobName` or `jobHandle` is required. アップロードジョブの名前。 |
|`uploadParams` (必須. アップロード `uploadParams` パラメータを指定するXMLドキュメント)|`jobHandle`|`xsd:string`| Exther `jobName` or `jobHandle` is required. 以前の要求で開始されたアップロードジョブの処理。 |
|`uploadParams` (必須. アップロー `uploadParams` ドパラメーターを指定するXMLドキュメント)|`locale`|`xsd:string`|オプション。 ローカライズの言語と国コード。 |
|`uploadParams` (必須. アップロー `uploadParams` ドパラメーターを指定するXMLドキュメント)|`description`|`xsd:string`|オプション。 ジョブの説明。 |
|`uploadParams` (必須. アップロー `uploadParams` ドパラメーターを指定するXMLドキュメント)|`destFolder`|`xsd:string`|オプション。 ファイル名のプロパティに対するプレフィックスを付けるターゲットフォルダーのパス。特に、ファイル名のフルパスをサポートしていないブラウザーや他のクライアントの場合。 |
|`uploadParams` (必須. アップロー `uploadParams` ドパラメーターを指定するXMLドキュメント)|`fileName`|`xsd:string`|オプション。 ターゲットファイルの名前。 filenameプロパティを上書きします。 |
|`uploadParams` (必須. アップロー `uploadParams` ドパラメーターを指定するXMLドキュメント)|`endJob`|`xsd:boolean`|オプション。 初期設定は false。|
|`uploadParams` (必須. アップロード `uploadParams` パラメーターを指定するXMLドキュメント)|`uploadParams`|`types:UploadPostJob`|既存のアクティブなジョブに対する後続のリクエストの場合はオプションです。 既存のジョブがある場合、は無視 `uploadParams` され、既存のジョブアップロードパラメータが使用されます。 UploadPostJobを参 [照](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

ブロック内 `<uploadPostParams>` には、含めるフ `<uploadParams>` ァイルの処理を指定するブロックが含まれます。

UploadPostJobを参照し [てください](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)。

パラメータは、同じジョブの `uploadParams` 一部として個々のファイルに対して変更される可能性があると想定する場合もありますが、そうではありません。 ジョブ全体に同じパ `uploadParams` ラメーターを使用します。

新しいアップロードジョブに対する最初のPOST要求では、パラメータを指定する必要があります。可能な場合は、一意のジョブ名を使用して、後続のジョブステータスのポーリングとジョブログのクエリを単純化する必要があります。 `jobName` 同じアップロードジョブに対する追加のPOSTリクエストでは、最初のリクエス `jobHandle` トから返される値を使 `jobName`用して、ではなく、パ `jobHandle` ラメーターを指定する必要があります。

アップロードジョブに対する最後のPOST要求では、このパラメータ `endJob` ーをtrueに設定し、今後、このジョブに対してPOSTされるファイルがないようにする必要があります。 これにより、すべてのPOSTファイルが取り込まれた直後にジョブを完了できます。 それ以外の場合は、30分以内に追加のPOST要求を受信しなかった場合、ジョブはタイムアウトになります。

## UploadPOSTの応答 {#section-421df5cc04d44e23a464059aad86d64e}

POSTリクエストが成功した場合、応答本文はXMLドキュメ `uploadPostReturn` ントになります。XSDは次のように指定します。

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

返され `jobHandle` た値は、同じジョブに対す `uploadPostParams`るその後のPOST `jobHandle` リクエストの/パラメーターに渡されます。 また、操作でジョブのステータスをポーリングしたり、操作でジ `getActiveJobs` ョブログをクエリーしたりする場合にも使用で `getJobLogDetails` きます。

POST要求の処理中にエラーが発生した場合、応答本文は、障害で説明されているいずれかのAPI障害タイプで構成さ [れます](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)。

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

