---
description: 指定されたURLのリストをDynamic Media CDN （コンテンツ配信ネットワーク）プロバイダーに転送し、HTTP応答の既存のキャッシュを無効にします。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
TQID: 'https://experienceleague.adobe.com/EiiTKlBO9it1WQXYW2ed-4Vo5qi2YSlR2SageNHMUqI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 472
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

指定されたURLのリストをDynamic Media CDN （コンテンツ配信ネットワーク）プロバイダーに転送し、HTTP応答の既存のキャッシュを無効にします。

## cdnCacheInvalidation：概要 {#section-4f70d2bc79d64288b961836ab17e9690}

CDN キャッシュの無効化により、これらのURLに対するすべてのHTTP リクエストは、この無効化リクエストがCDN ネットワークを通じて処理された後、Dynamic Media ネットワーク上の現在の公開データに対して強制的に再検証されます。 Dynamic Media サービスのURL構造に接続されておらず、会社の作成時に割り当てられたDynamic Media会社のルート IDに直接一致しないURLは、リクエスト全体のAPI障害になります。 CDNが無効と見なす無効なURLも、リクエスト全体のAPI障害になります。

**使用頻度：ルール**

この機能の使用頻度を管理するルールは、Dynamic MediaのCDN パートナーによって制御されます。 CDNは、ユーザーに対するサービスの最適なパフォーマンスを維持するために、これらの無効化の応答性を低下させる裁量を保持します。 Dynamic Mediaにこの機能の過剰な使用が通知された場合、Adobeは、会社ごとに、またはサービス全体で機能を無効にする必要があります。

**確認メール**

Dynamic Media CDN パートナーからの確認メールは、リストの作成者または他の最大5つのメールアドレスに送信できます。 このAPIは、メールで参照されているURLがクリアされたことをCDN ネットワーク全体に通知したときに確認を送信します。 指定されたURLの数が、1つの通知でDynamic MediaがCDN パートナーに配信できる数を超える場合、`cdnCacheInvalidation`への単一呼び出しは複数のメールを送信できます。 現在は、リクエストが100 URLを超えているが、CDN パートナーのリクエストに基づいて変更される可能性がある場合です。

**以降サポートされています**

6.0

## 承認済みユーザータイプ {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## パラメーター {#section-bd1ed2b7419945d19a2ebd5668499f72}

**入力** （`cdnCacheInvalidationParam`）

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>名</b> </th> 
   <th class="entry"> <b> タイプ </b> </th> 
   <th class="entry"> <b>が必要</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> 無効にするURLに接続されている会社へのハンドル。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph">種類：UrlArray</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> CDN キャッシュから無効にする最大1000個のURLのリスト。 すべてのURLには、無効化するDynamic Media会社のルート IDが含まれている必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output** （`cdnCacheInvalidationReturn`）

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>名</b> </th> 
   <th class="entry"> <b> タイプ </b> </th> 
   <th class="entry"> <b>が必要</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">無効化ハンドル </span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パージ要求を参照するハンドル。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> APIは、ほぼ即座に（約5秒）キャッシュを無効化するようになりました。 そのため、無効化ステータスのポーリングは一般的に不要になります。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">推定秒数</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パージ要求の完了までの推定秒数。 クライアントは、ステータスをポーリングする前に、この時間を待つ必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-f414361a58e84dfcbbac30a358d02125}

この例では、CDN キャッシュで4つのURLの無効化をリクエストしています。 応答には、操作の成功の概要数と、この機能の使用をクライアントが支援するためにCDNから直接提供されたエラーの詳細のリストが含まれます。

`getCdnCacheInvalidationStatus`操作。

**リクエスト**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**応答**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

