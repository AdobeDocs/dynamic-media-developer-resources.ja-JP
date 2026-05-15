---
description: IPS Web サービスは、IPS Web サービス コンポーネントがインストールされている任意のIPS インストールからアクセスされるWSDL （Web サービス記述言語）ドキュメントのセットでサポートされています。 各IPS API リリースには、バージョン管理されたターゲット XML名前空間を参照する新しいWSDL ファイルが含まれています。 以前のWSDL名前空間のバージョンもサポートされており、既存のアプリケーションとの下位互換性が可能です。
solution: Experience Manager
title: IPS Web Service WSDL バージョン
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
TQID: 'https://experienceleague.adobe.com/S-g6J7oZiuEbw-Y8Wk7IMy6vQmAQJiBVV7d-f8ZyrE0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1003
ht-degree: 0%

---

# IPS Web Service WSDL バージョン{#ips-web-service-wsdl-versions}

IPS Web サービスは、IPS Web サービス コンポーネントがインストールされている任意のIPS インストールからアクセスされるWSDL （Web サービス記述言語）ドキュメントのセットでサポートされています。 各IPS API リリースには、バージョン管理されたターゲット XML名前空間を参照する新しいWSDL ファイルが含まれています。 以前のWSDL名前空間のバージョンもサポートされており、既存のアプリケーションとの下位互換性が可能です。

## WSDL アクセス {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

次に示すように、Scene7 WSDLにアクセスします。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

`<IPS_webapp>`のデフォルト値は`scene7`です。

**サービスの場所**

サービス URLは、IPS Web サービス WSDL ドキュメントのサービス セクションで指定します。 サービス URLは通常、次の形式になります。

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ヨーロッパ、中東、アジア </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>日本/アジア太平洋 </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## サポートされているWSDL {#section-ebbba69880f94e9c823f1147974eb404}

最新バージョンのIPS APIの機能を使用する場合は、コードを変更する必要がある場合があることを忘れないでください。 IPS APIは、次のバージョンのWSDLをサポートしています。

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API リリースバージョン </p> </th> 
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

新機能を使用するために変更が必要な既存のアプリケーションは、最新のAPI バージョンにアップグレードする必要があり、既存のコードを変更する必要がある場合があります。 詳しくは、変更ログを参照してください。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**バインディング**

IPS API Web サービスは、SOAP バインディングのみをサポートしています。

**サポートされているトランスポート**

IPS API SOAP バインディングは、HTTP トランスポートのみをサポートします。 HTTPS POST メソッドを使用して、すべてのSOAP リクエストを行います。

**SOAP アクションヘッダー**

リクエストを処理するには、SOAPAction HTTP ヘッダーをリクエストされた操作の名前に設定します。 WSDL バインディングセクションの操作名属性で、名前を指定します。

**メッセージ形式**

document/literal スタイルは、XML スキーマ定義言語（[https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)）に基づき、WSDL ファイルで指定されたタイプを持つすべての入出力メッセージに使用されます。 すべてのタイプでは、WSDL ファイルで指定されたターゲット名前空間値を使用して、修飾名が必要です。

**認証を要求**

API要求で認証資格情報を渡す際に推奨される方法は、IPS API WSDLで定義されているように`authHeader`要素を使用することです。

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
   <td colname="col1"> <p> <span class="codeph"> ユーザー</span> </p> </td> 
   <td colname="col2"> <p> 有効なIPS ユーザーメール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パスワード </span> </p> </td> 
   <td colname="col2"> <p>ユーザーアカウントのパスワード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ロケール </span> </p> </td> 
   <td colname="col2"> <p> リクエストのオプションのロケール。 詳しくは、<b> ロケール </b>を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> アプリケーション名を呼び出しています。 このパラメーターはオプションですが、すべてのリクエストに含めることをお勧めします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> アプリケーションのバージョンを呼び出しています。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> 応答XMLのgzip圧縮を有効または無効にするオプションのフラグ。 デフォルトでは、HTTP Accept-Encoding ヘッダーがgzipのサポートを示す場合、応答はgzip圧縮されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 障害応答のHTTP ステータスコードを上書きするオプションのパラメーター。 デフォルトでは、フォールトレスポンスはHTTP ステータスコード 500 （内部サーバーエラー）を返します。 Adobe Flashなどの一部のクライアントプラットフォームでは、ステータスコード 200 （OK）が返されない限り、レスポンス本文を読み取ることができません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`authHeader`要素は、API バージョンに関係なく、常に名前空間`http://www.scene7.com/IpsApi/xsd`で定義されます。

次に、リクエスト SOAP ヘッダーで`authHeader`要素を使用する例を示します。

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

**その他のリクエスト認証方法**

何らかの理由でクライアントアプリケーションが`authHeader` SOAP ヘッダーを渡すことができない場合は、API リクエストでHTTP Basic認証（RFC 2617で指定）を使用して資格情報を指定することもできます。

HTTP Basic認証の場合、各SOAP POST リクエストのHTTP ヘッダーセクションには、次のフォームのヘッダーを含める必要があります。

`Authorization: Basic base64(<IPS_user_email>:<password>)`

ここで、`base64()`は標準のBase64 エンコーディングを適用し、`<IPS_user_email>`は有効なIPS ユーザーの電子メールアドレス、`<password>`はユーザーのパスワードです。

最初のリクエストでAuthorization ヘッダーを先制的に送信します。 リクエストに認証資格情報が含まれていない場合、`IpsApiService`はステータスコード `401 (Unauthorized)`で応答しません。 代わりに、`500 (Internal Server Error)`のステータスコードが、リクエストを認証できなかったことを示すSOAP fault bodyとともに返されます。

IPS 3.8より前は、SOAP ヘッダーによる認証は、名前空間`http://www.scene7.com/IpsApi`の`AuthUser`要素と`AuthPassword`要素を使用して実装されていました。 以下に例を挙げます。

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

このスタイルは後方互換性で引き続きサポートされていますが、`authHeader`要素を優先して非推奨（廃止予定）になっています。

**認証を要求**

呼び出し元の資格情報が認証された後、リクエストがチェックされ、呼び出し元が要求された操作を実行する権限を持っていることを確認します。 認証は、発信者のユーザーの役割に基づいて行われます。また、ターゲット企業、ターゲットユーザー、およびその他の操作パラメーターを確認する必要がある場合もあります。 さらに、Image Portal ユーザーは、特定のフォルダーおよびアセット操作を実行するために必要な権限を持つグループに属している必要があります。 操作参照セクションでは、各操作の承認要件について詳しく説明します。

**SOAPのリクエストと応答の例**

次の例は、HTTP ヘッダーを含む完全な`addCompany`操作を示しています。

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

**SOAPのエラー**

操作で例外条件が発生した場合、通常の応答の代わりに、SOAPのエラーがSOAP メッセージの本文として返されます。 例えば、管理者以外のユーザーが以前の`addCompany` リクエストを送信しようとすると、次の応答が返されます。

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
