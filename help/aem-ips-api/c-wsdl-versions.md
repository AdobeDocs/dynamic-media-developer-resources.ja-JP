---
description: IPS Webサービスは、IPS WebサービスコンポーネントがインストールされているIPSインストールからアクセスされるWSDL (Web Services Description Language)ドキュメントのセットによってサポートされます。 各IPS APIリリースには、バージョン付きのターゲットXML名前空間を参照する新しいWSDLファイルが含まれています。 以前のWSDL名前空間バージョンも、既存のアプリケーションとの後方互換性を保つためにサポートされていました。
seo-description: IPS Webサービスは、IPS WebサービスコンポーネントがインストールされているIPSインストールからアクセスされるWSDL (Web Services Description Language)ドキュメントのセットによってサポートされます。 各IPS APIリリースには、バージョン付きのターゲットXML名前空間を参照する新しいWSDLファイルが含まれています。 以前のWSDL名前空間バージョンも、既存のアプリケーションとの後方互換性を保つためにサポートされていました。
seo-title: IPS WebサービスのWSDLバージョン
solution: Experience Manager
title: IPS WebサービスのWSDLバージョン
topic: Scene7 Image Production System API
uuid: 3443bb91-1663-4686-b20a-94c372f0026e
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# IPS WebサービスのWSDLバージョン{#ips-web-service-wsdl-versions}

IPS Webサービスは、IPS WebサービスコンポーネントがインストールされているIPSインストールからアクセスされるWSDL (Web Services Description Language)ドキュメントのセットによってサポートされます。 各IPS APIリリースには、バージョン付きのターゲットXML名前空間を参照する新しいWSDLファイルが含まれています。 以前のWSDL名前空間バージョンも、既存のアプリケーションとの後方互換性を保つためにサポートされていました。

## WSDLアクセス {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

次に示すように、Scene7 WSDLにアクセスします。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

のデフォルト値 `<IPS_webapp>` はです `scene7`。

**サービスの場所**

サービスURLは、IPS Web Service WSDLドキュメントのサービスセクションで指定されます。 サービスURLは、通常次の形式で指定します。

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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

最新バージョンのIPS APIの機能を使用する場合は、コードの変更が必要になる場合があります。 IPS APIは、次のバージョンのWSDLをサポートします。

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
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0より前 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

新機能を使用するために変更する必要がある既存のアプリケーションは、最新のAPIバージョンにアップグレードする必要があり、既存のコードを変更する必要がある場合があります。 詳しくは、変更ログを参照してください。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**連結**

IPS API Webサービスは、SOAPバインディングのみをサポートします。

**サポートされる輸送**

IPS API SOAPバインディングは、HTTPトランスポートのみをサポートします。 HTTPS POSTメソッドを使用して、すべてのSOAP要求を作成します。

**SOAPアクションヘッダー**

リクエストを処理するには、SOAPAction HTTPヘッダーをリクエストされた操作の名前に設定します。 「WSDL連結」セクションの操作名属性で名前を指定します。

**メッセージの形式**

document/literalスタイルは、XMLスキーマ定義言語( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/))に基づき、WSDLファイルで指定された型を持つすべての入力および出力メッセージに使用されます。 すべての型で、WSDLファイルで指定されたターゲット名前空間の値を使用して修飾名が必要です。

**認証の要求**

API要求で認証資格情報を渡すには、IPS API WSDLで定義されている要 `authHeader` 素を使用する方法をお勧めします。

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
   <td colname="col2"> <p> 有効なIPSユーザの電子メール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パスワード </span> </p> </td> 
   <td colname="col2"> <p>ユーザーアカウントのパスワード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> リクエストのオプションのロケール。 See <b>Locale</b> for details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> 呼び出し元のアプリケーション名。 このパラメーターはオプションですが、すべてのリクエストに含めることをお勧めします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> アプリケーションのバージョンを呼び出しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> 応答XMLのgzip圧縮を有効または無効にするオプションのフラグ。 デフォルトでは、HTTP Accept-Encodingヘッダーがgzipのサポートを示している場合、応答はgzip圧縮されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 障害応答のHTTPステータスコードを上書きするオプションのパラメーター。 デフォルトでは、障害応答はHTTPステータスコード500（内部サーバーエラー）を返します。 Adobe Flashを含む一部のクライアントプラットフォームは、ステータスコードが200(OK)に返されない限り、応答本文を読み取れません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

APIのバ `authHeader` ージョンに関係なく、要素は常 `http://www.scene7.com/IpsApi/xsd`に名前空間で定義されます。

次に、要求SOAPヘッダーで要素を使 `authHeader` 用する例を示します。

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

何らかの理由でクライアントアプリケーションが `authHeader` SOAPヘッダーを渡せない場合、API要求はHTTP基本認証（RFC 2617で指定）を使用して秘密鍵証明書も指定できます。

HTTP基本認証の場合、各SOAP POST要求のHTTPヘッダーセクションには、次のフォームのヘッダーが含まれている必要があります。

`Authorization: Basic base64(<IPS_user_email>:<password>)`

は、 `base64()` 標準Base64エンコーディングを適 `<IPS_user_email>` 用します。は、有効なIPSユーザの電子メールアドレスで、は `<password>` ユーザのパスワードです。

最初の要求で、事前に認証ヘッダーを送信します。 認証資格情報が要求に含まれていない場合、 `IpsApiService` はのステータスコードで応答しませ `401 (Unauthorized)`ん。 代わりに、のステータスコードが、要 `500 (Internal Server Error)` 求を認証できなかったことを示すSOAP障害本体と共に返されます。

IPS 3.8より前は、SOAPヘッダを介した認証は、名前空間の要素と要素を `AuthUser` 使用し `AuthPassword` て実装されていまし `http://www.scene7.com/IpsApi`た。 例：

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

このスタイルは、後方互換性のために引き続きサポートされていますが、この要素を優先して廃止され `authHeader` ました。

**認証の要求**

呼び出し元の資格情報が認証された後、要求はチェックされ、呼び出し元が要求された操作を実行する権限を持っていることが確認されます。 認証は、呼び出し元のユーザーの役割に基づいて行われます。また、ターゲットとなる会社、ターゲットとなるユーザー、その他の操作パラメーターの確認が必要な場合もあります。 また、Image Portalユーザは、特定のフォルダおよびアセットの操作を実行するために必要な権限を持つグループに属している必要があります。 「操作の参照」セクションでは、各操作の認証要件の詳細を説明しています。

**SOAPリクエストと応答の例**

次の例は、HTTPヘッダーを含む完 `addCompany` 全な操作を示しています。

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

そして対応する応答：

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

操作が例外条件を検出すると、通常の応答の代わりにSOAPエラーがSOAPメッセージの本文として返されます。 例えば、管理者以外のユーザーが以前のリクエストを送信しようとす `addCompany` ると、次の応答が返されます。

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

