---
description: IPS Web サービスは、IPS Web サービスコンポーネントがインストールされている IPS インストールからアクセスする WSDL （Web Services Description Language） ドキュメントのセットによってサポートされています。 各 IPS API リリースには、バージョン管理されたターゲット XML 名前空間を参照する新しい WSDL ファイルが含まれています。 既存のアプリケーションとの下位互換性を保つために、以前のバージョンの WSDL 名前空間もサポートされています。
solution: Experience Manager
title: IPS Web サービス WSDL のバージョン
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# IPS Web サービス WSDL のバージョン{#ips-web-service-wsdl-versions}

IPS Web サービスは、IPS Web サービスコンポーネントがインストールされている IPS インストールからアクセスする WSDL （Web Services Description Language） ドキュメントのセットによってサポートされています。 各 IPS API リリースには、バージョン管理されたターゲット XML 名前空間を参照する新しい WSDL ファイルが含まれています。 既存のアプリケーションとの下位互換性を保つために、以前のバージョンの WSDL 名前空間もサポートされています。

## WSDL アクセス {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

以下に示すように、Scene7 WSDL にアクセスします。

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

`<IPS_webapp>` のデフォルト値は `scene7` です。

**サービスの場所**

サービス URL は、IPS web サービス WSDL ドキュメントのサービスセクションで指定されます。 サービス URL は、通常、次の形式で指定します。

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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

最新バージョンの IPS API の機能を使用する場合は、コードを変更する必要がある場合があります。 IPS API では、次のバージョンの WSDL がサポートされています。

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
   <td colname="col1"> <p>4.0 より前 </p> </td> 
   <td colname="col2"> <p> <span class="codeph">.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

新しい機能を使用するために変更が必要な既存のアプリケーションは、最新の API バージョンにアップグレードする必要があり、既存のコードを変更する必要が生じる場合があります。 詳しくは、変更ログを参照してください。

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**バインディング**

IPS API web サービスは、SOAP バインディングのみをサポートしています。

**サポートされるトランスポート**

IPS API SOAP バインディングは、HTTP トランスポートのみをサポートしています。 すべてのSOAP リクエストは HTTPS POST メソッドを使用して行います。

**SOAP アクションヘッダー**

リクエストを処理するには、SOAPAction HTTP ヘッダーをリクエストされた操作の名前に設定します。 WSDL 結合セクションの操作名属性が名前を指定します。

**メッセージの形式**

ドキュメント/リテラルスタイルは、XML スキーマ定義言語（[https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)）に基づき、WSDL ファイルで指定された型を持つすべての入力および出力メッセージで使用されます。 すべてのタイプには、WSDL ファイルで指定されたターゲット名前空間の値を使用して、修飾名が必要です。

**認証をリクエスト**

API リクエストで認証資格情報を渡すための推奨される方法は、IPS API WSDL で定義された `authHeader` 要素を使用することです。

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
   <td colname="col1"> <p> <span class="codeph"> user </span> </p> </td> 
   <td colname="col2"> <p> 有効な IPS ユーザーメール。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password </span> </p> </td> 
   <td colname="col2"> <p>ユーザーアカウントのパスワード。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> リクエストのオプションのロケール。 詳しくは、<b> ロケール </b> を参照してください。 </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p> 応答 XML の gzip 圧縮を有効または無効にするオプションのフラグ。 HTTP Accept-Encoding ヘッダーが gzip のサポートを示している場合、デフォルトでは、応答は gzip で圧縮されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> 障害応答の HTTP ステータスコードを上書きするオプションのパラメーター。 デフォルトでは、障害応答は HTTP ステータスコード 500 （内部サーバーエラー）を返します。 Adobe Flash を含む一部のクライアントプラットフォームでは、ステータスコード 200 （OK）が返されない限り、応答本文を読み取ることができません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`authHeader` 要素は、API のバージョンに関係なく、常に名前空間 `http://www.scene7.com/IpsApi/xsd` で定義されます。

リクエスト SOAP ヘッダーで `authHeader` 要素を使用する例を次に示します。

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

何らかの理由でクライアントアプリケーションが `authHeader` SOAP ヘッダーを渡すことができない場合、API リクエストは、HTTP 基本認証（RFC 2617 で指定）を使用して資格情報を指定することもできます。

HTTP 基本認証の場合、各SOAP POST リクエストの HTTP ヘッダーセクションには、

`Authorization: Basic base64(<IPS_user_email>:<password>)`

`base64()` は標準の Base64 エンコーディングを適用します。`<IPS_user_email>` は有効な IPS ユーザーのメールアドレスで、`<password>` はユーザーのパスワードです。

最初のリクエストで Authorization ヘッダーを事前に送信します。 認証資格情報がリクエストに含まれていない場合、`IpsApiService` はステータスコード `401 (Unauthorized)` で応答しません。 代わりに、`500 (Internal Server Error)` のステータスコードが、リクエストを認証できなかったことを示すSOAP フォールト本文と共に返されます。

IPS 3.8 以前は、名前空間 `AuthUser` の `AuthPassword` 要素と `http://www.scene7.com/IpsApi` 要素を使用して、SOAP Header を介した認証が実装されていました。 以下に例を挙げます。

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

このスタイルは後方互換性のために引き続きサポートされますが、`authHeader` 要素を優先して非推奨になりました。

**リクエストの認証**

呼び出し元の資格情報が認証されると、リクエストがチェックされ、呼び出し元がリクエストされた操作を実行する権限を持っていることが確認されます。 認証は呼び出し元のユーザーの役割に基づいており、ターゲットの会社、ターゲットユーザー、その他の操作パラメーターの確認が必要になる場合もあります。 また、Image Portal ユーザーは、特定のフォルダーおよびアセット操作を実行するために必要な権限を持つグループに属している必要があります。 操作のリファレンスセクションでは、各操作の認証要件の詳細を説明します。

**SOAPのリクエストと応答のサンプル**

次の例は、HTTP ヘッダーを含む、完全な `addCompany` 操作を示しています。

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

対応する応答：

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

**SOAP フォールト**

オペレーションが例外条件に遭遇すると、通常のレスポンスの代わりにSOAPメッセージの本文としてSOAP障害が返される。 例えば、管理者以外のユーザーが前の `addCompany` リクエストを送信しようとすると、次の応答が返されます。

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
