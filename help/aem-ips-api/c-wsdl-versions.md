---
description: IPS Web サービスは、IPS Web サービスコンポーネントがインストールされている IPS インストールからアクセスされる WSDL (Web Services Description Language) ドキュメントのセットによってサポートされます。 各 IPS API リリースには、バージョン管理されたターゲット XML 名前空間を参照する新しい WSDL ファイルが含まれています。 以前の WSDL 名前空間バージョンも、既存のアプリケーションとの下位互換性を保つためにサポートされていました。
solution: Experience Manager
title: IPS Web サービス WSDL のバージョン
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 1%

---

# IPS Web サービス WSDL のバージョン{#ips-web-service-wsdl-versions}

IPS Web サービスは、IPS Web サービスコンポーネントがインストールされている IPS インストールからアクセスされる WSDL (Web Services Description Language) ドキュメントのセットによってサポートされます。 各 IPS API リリースには、バージョン管理されたターゲット XML 名前空間を参照する新しい WSDL ファイルが含まれています。 以前の WSDL 名前空間バージョンも、既存のアプリケーションとの下位互換性を保つためにサポートされていました。

## WSDL アクセス {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

次に示すように、Scene7 WSDL にアクセスします。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

のデフォルト値 `<IPS_webapp>` 次に該当 `scene7`.

**サービスの場所**

サービス URL は、IPS Web Service WSDL ドキュメントのサービスセクションで指定されます。 サービス URL は、通常、次の形式です。

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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

## サポートされる WSDL {#section-ebbba69880f94e9c823f1147974eb404}

最新バージョンの IPS API で機能を使用する場合は、コードの変更が必要になる場合があります。 IPS API は、次のバージョンの WSDL をサポートしています。

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API リリースバージョン </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API 名前空間 </p> </th> 
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
   <td colname="col1"> <p>4.0 以前 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

新機能を使用するために変更が必要な既存のアプリケーションは、最新の API バージョンにアップグレードする必要があり、既存のコードを変更する必要がある場合があります。 詳細は、変更ログを参照してください。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**連結**

IPS API Web サービスは、SOAP バインディングのみをサポートします。

**サポートされるトランスポート**

IPS API SOAP バインディングは、HTTP トランスポートのみをサポートしています。 HTTPS リクエストメソッドを使用して、すべての SOAPPOSTを実行します。

**SOAP アクションヘッダー**

要求を処理するには、SOAPAction HTTP ヘッダーに要求された操作の名前を設定します。 WSDL 結合セクションの操作名属性で、名前を指定します。

**メッセージの形式**

document/literal スタイルは、XML スキーマ定義言語 ( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)) をクリックし、WSDL ファイルで指定します。 すべての型には、WSDL ファイルで指定されたターゲット名前空間の値を使用して修飾名が必要です。

**認証をリクエスト**

API リクエストに認証資格情報を渡す推奨される方法は、 `authHeader` 要素が IPS API WSDL で定義されている。

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
   <td colname="col2"> <p> 有効な IPS ユーザ電子メール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> パスワード </span> </p> </td> 
   <td colname="col2"> <p>ユーザーアカウントのパスワード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> 要求のオプションのロケールです。 詳しくは、 <b>ロケール</b> 」を参照してください。 </p> </td> 
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
   <td colname="col2"> <p> 応答 XML の gzip 圧縮を有効または無効にするオプションのフラグです。 デフォルトでは、HTTP Accept-Encoding ヘッダーが gzip のサポートを示している場合、応答は gzip 形式で圧縮されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 障害応答の HTTP ステータスコードを上書きするオプションのパラメーターです。 デフォルトでは、障害応答は HTTP ステータスコード 500（内部サーバーエラー）を返します。 AdobeFlashを含む一部のクライアントプラットフォームは、ステータスコード 200(OK) が返されない限り、応答本文を読み取れません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

The `authHeader` 要素は常に名前空間で定義されます `http://www.scene7.com/IpsApi/xsd`（API バージョンとは無関係）

次に、 `authHeader` 要素が SOAP 要求ヘッダーに含まれている：

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

何らかの理由でクライアントアプリケーションが `authHeader` SOAP ヘッダー、API リクエストは、HTTP 基本認証（RFC 2617 で指定）を使用して資格情報を指定することもできます。

HTTP Basic 認証の場合、各 SOAP 認証要求の HTTP ヘッダーセクションには、次の形式のPOSTを含める必要があります。

`Authorization: Basic base64(<IPS_user_email>:<password>)`

ここで、 `base64()` は、標準の Base64 エンコーディングを適用します。 `<IPS_user_email>` は、有効な IPS ユーザの電子メールアドレス、および `<password>` は、ユーザーのパスワードです。

最初のリクエストで事前に Authorization ヘッダーを送信します。 リクエストに認証資格情報が含まれていない場合、 `IpsApiService` 次のステータスコードで応答しない： `401 (Unauthorized)`. 代わりに、 `500 (Internal Server Error)` は、リクエストが認証できなかったことを示す SOAP フォルト本文と共に返されます。

IPS 3.8 以前は、SOAP ヘッダーによる認証は、 `AuthUser` および `AuthPassword` 名前空間の要素 `http://www.scene7.com/IpsApi`. 以下に例を挙げます。

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

このスタイルは後方互換性のために引き続きサポートされますが、非推奨（廃止予定）となり、 `authHeader` 要素を選択します。

**認証をリクエスト**

呼び出し元の資格情報が認証されると、リクエストがチェックされ、呼び出し元がリクエストされた操作を実行する権限を持っているかが確認されます。 認証は、呼び出し元のユーザーの役割に基づいており、ターゲットの会社、ターゲットのユーザー、その他の操作パラメーターの確認も必要になる場合があります。 また、画像ポータルユーザーは、特定のフォルダーおよびアセット操作を実行するために必要な権限を持つグループに属している必要があります。 操作のリファレンスの節では、各操作の認証要件の詳細を説明します。

**SOAP リクエストと応答のサンプル**

次の例は、完全な `addCompany` 操作（HTTP ヘッダーを含む）:

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

対応する応答は次のようになります。

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

**SOAP 障害**

操作で例外条件が発生した場合、SOAP 障害が通常の応答の代わりに SOAP メッセージの本文として返されます。 例えば、管理者以外のユーザーが `addCompany` リクエストの場合、次の応答が返されます。

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
