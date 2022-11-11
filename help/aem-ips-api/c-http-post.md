---
title: HTTP POST を使用した UploadFile Servlet へのアセットのアップロード
description: へのアセットのアップロード [!DNL Dynamic Media] Classic には、ジョブを設定する 1 つ以上の HTTPPOSTリクエストが含まれ、アップロードされたファイルに関連付けられているすべてのログアクティビティを調整します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# HTTP POST を使用した UploadFile Servlet へのアセットのアップロード{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

アセットをDynamic Media Classicにアップロードする際には、アップロードしたファイルに関連付けられているすべてのログアクティビティを調整するためのジョブを設定する 1 つ以上の HTTPPOSTリクエストが必要になります。

次の URL を使用して、UploadFile サーブレットにアクセスします。

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>アップロードPOSTに対するすべてのジョブリクエストは、同じ IP アドレスから送信される必要があります。

**Dynamic Media地域のアクセス URL**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>地域 </p> </th> 
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

アップロードジョブは、共通の `jobHandle` を使用して、処理を同じジョブに関連付けます。 各リクエストは `multipart/form-data` エンコードされ、次のフォーム部分で構成されます。

>[!NOTE]
>
>アップロードPOSTに対するすべてのジョブリクエストは、同じ IP アドレスから送信される必要があります。

|  HTTPPOSTフォーム部分  |  説明  |
|---|---|
| `auth`  |   必須. 認証情報とクライアント情報を指定する XML authHeader ドキュメント。 詳しくは、 **認証をリクエスト** under [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   オプション. アップロードリクエストごとに、1 つ以上のファイルを含めてPOSTできます。 各ファイル部分には、Content-Disposition ヘッダーに filename パラメータを含めることができます。指定しない場合は、IPS でターゲットファイル名として使用されます。 `uploadPostParams/fileName` パラメーターが指定されています。 |

|  HTTPPOSTフォーム部分   |  uploadPostParams 要素名   |  種類   |  説明   |
|---|---|---|---|
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント )   |   `companyHandle`  |  `xsd:string`  | 必須。ファイルのアップロード先の会社に対する処理。  |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `jobName`  |  `xsd:string`  | 次のいずれか `jobName` または `jobHandle` が必要です。 アップロードジョブの名前。  |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `jobHandle`  |  `xsd:string`  | 次のいずれか `jobName` または `jobHandle` が必要です。 前のリクエストで開始されたアップロードジョブの処理。  |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `locale`  |  `xsd:string`  | （オプション）ローカリゼーション用の言語および国コード。  |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `description`  |  `xsd:string`  | （オプション）ジョブの説明。  |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `destFolder`  |  `xsd:string`  | （オプション）filename プロパティにプレフィックスするターゲットフォルダーのパス。特に、ファイル名でのフルパスをサポートしていないブラウザーや他のクライアントで使用されます。  |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `fileName`  |  `xsd:string`  | （オプション）ターゲットファイルの名前。 filename プロパティを上書きします。 |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `endJob`  |  `xsd:boolean`  | （オプション）初期設定は false。 |
| `uploadParams` (必須. XML `uploadParams` アップロードパラメーターを指定するドキュメント ) | `uploadParams`  |  `types:UploadPostJob`  | 既存のアクティブなジョブの後続のリクエストの場合はオプションです。 既存のジョブがある場合、 `uploadParams` が無視され、既存のジョブアップロードパラメーターが使用されます。 詳しくは、 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

内 `<uploadPostParams>` ブロックは `<uploadParams>` 含まれるファイルの処理を指定するブロック。

詳しくは、 [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

あなたは `uploadParams` パラメーターは、同じジョブの一部として、個々のファイルに対して変更される場合がありますが、そうではありません。 同じ `uploadParams` ジョブ全体のパラメーター。

新しいアップロードPOSTの最初のジョブリクエストでは、 `jobName` パラメータ。後続のジョブステータスのポーリングとジョブログのクエリを簡単にするために、一意のジョブ名を使用するのが望ましい。 同じアップロードPOSTに対する追加のジョブリクエストでは、 `jobHandle` パラメーターの代わりに `jobName`、 `jobHandle` 最初のリクエストから返された値。

アップロードPOSTの最終的なジョブリクエストでは、 `endJob` パラメーターを true に設定して、今後のファイルがこのジョブに POST されないようにします。 これにより、すべての POSTed ファイルが取り込まれた後すぐにジョブを完了できます。 それ以外の場合、30 分以内に追加のPOSTリクエストを受信しなかった場合、ジョブはタイムアウトします。

## UploadPOST 応答 {#section-421df5cc04d44e23a464059aad86d64e}

成功したPOSTリクエストの場合、応答本文は XML です `uploadPostReturn` ドキュメントの次の場所に XSD が指定されているとします。

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

この `jobHandle` 返された `uploadPostParams`/ `jobHandle` 同じジョブに対する以降のPOSTリクエストのパラメーター。 また、 `getActiveJobs` 操作を実行するか、 `getJobLogDetails` 操作。

POSTリクエストの処理中にエラーが発生した場合、応答本文は、 [障害](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## サンプルのPOSTリクエスト {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## POST応答の例 — 成功 {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## POST応答の例 — エラー {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
