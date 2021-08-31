---
description: IPS Webサービスは、IPS WebサービスコンポーネントがインストールされているIPSインストールからアクセスされるWSDL (Web Services Description Language)ドキュメントのセットによってサポートされます。 各IPS APIリリースには、バージョン管理されたターゲットXML名前空間を参照する新しいWSDLファイルが含まれています。 以前のWSDL名前空間バージョンも、既存のアプリケーションとの下位互換性を保つためにサポートされています。
solution: Experience Manager
title: IPS WebサービスWSDLバージョン
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 1%

---

# IPS WebサービスWSDLバージョン{#ips-web-service-wsdl-versions}

IPS Webサービスは、IPS WebサービスコンポーネントがインストールされているIPSインストールからアクセスされるWSDL (Web Services Description Language)ドキュメントのセットによってサポートされます。 各IPS APIリリースには、バージョン管理されたターゲットXML名前空間を参照する新しいWSDLファイルが含まれています。 以前のWSDL名前空間バージョンも、既存のアプリケーションとの下位互換性を保つためにサポートされています。

## WSDLアクセス {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

次に示すように、Scene7 WSDLにアクセスします。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

`<IPS_webapp>`のデフォルト値は`scene7`です。

**サービスの場所**

サービスURLは、IPS Web Service WSDLドキュメントのサービスセクションで指定されます。 サービスURLは、通常、次の形式です。

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ヨーロッパ、中東、アジア </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asia Pacific </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされるWSDL {#section-ebbba69880f94e9c823f1147974eb404}

最新バージョンのIPS APIで機能を使用する場合は、コードの変更が必要になる場合があります。 IPS APIは、次のバージョンのWSDLをサポートしています。

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>APIリリースバージョン </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API名前空間 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0より前 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

新機能を使用するために変更が必要な既存のアプリケーションは、最新のAPIバージョンにアップグレードし、既存のコードに変更を加える必要がある場合があります。 詳しくは、変更ログを参照してください。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**連結**

IPS API Webサービスは、SOAPバインディングのみをサポートします。

**サポートされる輸送**

IPS API SOAPバインディングは、HTTPトランスポートのみをサポートしています。 HTTPS要求方法を使用して、すべてのSOAPPOSTを行います。

**SOAPアクションヘッダー**

要求を処理するには、SOAPAction HTTPヘッダーに要求された操作の名前を設定します。 WSDL連結セクションの操作名属性で名前を指定します。

**メッセージの形式**

document/literalスタイルは、XMLスキーマ定義言語([https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/))に基づく、WSDLファイルで指定された型を持つすべての入力および出力メッセージに使用されます。 すべての型には、WSDLファイルで指定されたターゲット名前空間の値を使用して修飾名が必要です。

**認証のリクエスト**

APIリクエストに認証資格情報を渡す推奨される方法は、IPS API WSDLで定義されている`authHeader`要素を使用することです。

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**フィールド**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ユーザ </span> </p> </td> 
   <td colname="col2"> <p> 有効なIPSユーザー電子メール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パスワード </span> </p> </td> 
   <td colname="col2"> <p>ユーザーアカウントのパスワード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> リクエストのオプションのロケール。 詳しくは、<b>ロケール</b>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName  </span> </p> </td> 
   <td colname="col2"> <p> アプリケーション名を呼び出しています。 このパラメーターはオプションですが、すべてのリクエストに含めることをお勧めします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion  </span> </p> </td> 
   <td colname="col2"> <p> アプリケーションのバージョンを呼び出しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse  </span> </p> </td> 
   <td colname="col2"> <p> 応答XMLのgzip圧縮を有効または無効にするオプションのフラグです。 デフォルトでは、HTTP Accept-Encodingヘッダーがgzipのサポートを示している場合、応答はgzip形式で圧縮されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode  </span> </p> </td> 
   <td colname="col2"> <p> 障害応答のHTTPステータスコードを上書きするオプションのパラメーター。 デフォルトでは、フォルト応答はHTTPステータスコード500（内部サーバーエラー）を返します。 AdobeFlashを含む一部のクライアントプラットフォームは、ステータスコード200(OK)が返されない限り、応答本文を読み取れません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`authHeader`要素は、APIバージョンに関係なく、常に名前空間`http://www.scene7.com/IpsApi/xsd`で定義されます。

次に、要求SOAPヘッダーで`authHeader`要素を使用する例を示します。

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**その他の要求認証方法**

何らかの理由でクライアントアプリケーションが`authHeader` SOAPヘッダーを渡すことができない場合、API要求は、HTTP基本認証（RFC 2617で指定）を使用して資格情報を指定することもできます。

HTTP基本認証の場合、各SOAPPOST要求のHTTPヘッダーセクションには、次の形式のヘッダーを含める必要があります。

`Authorization: Basic base64(<IPS_user_email>:<password>)`

ここで、`base64()`は標準のBase64エンコーディングを適用し、`<IPS_user_email>`は有効なIPSユーザーの電子メールアドレス、`<password>`はユーザーのパスワードです。

最初のリクエストでAuthorizationヘッダーを先に送信します。 リクエストに認証資格情報が含まれていない場合、`IpsApiService`は`401 (Unauthorized)`というステータスコードで応答しません。 代わりに、`500 (Internal Server Error)`のステータスコードがSOAP障害本文と共に返され、要求が認証できなかったことが示されます。

IPS 3.8より前は、SOAPヘッダーを介した認証は、名前空間`http://www.scene7.com/IpsApi`の`AuthUser`要素と`AuthPassword`要素を使用して実装されていました。 例：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

このスタイルは後方互換性のために引き続きサポートされますが、`authHeader`要素は非推奨（廃止予定）となっています。

**承認のリクエスト**

呼び出し元の資格情報が認証されると、要求元が要求された操作を実行する権限を持っていることを確認するために要求がチェックされます。 承認は、呼び出し元のユーザーの役割に基づいており、場合によっては、ターゲット会社、ターゲットユーザー、その他の操作パラメーターの確認も必要になります。 さらに、画像ポータルユーザーは、特定のフォルダーおよびアセット操作を実行するために必要な権限を持つグループに属している必要があります。 操作のリファレンスの節では、各操作の認証要件の詳細を説明します。

**SOAP要求と応答のサンプル**

次の例は、HTTPヘッダーを含む完全な`addCompany`操作を示しています。

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

対応する応答は次のとおりです。

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP障害**

操作で例外条件が発生した場合、SOAP障害が通常の応答の代わりにSOAPメッセージの本文として返されます。 例えば、管理者以外のユーザーが以前の`addCompany`リクエストを送信しようとすると、次の応答が返されます。

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
