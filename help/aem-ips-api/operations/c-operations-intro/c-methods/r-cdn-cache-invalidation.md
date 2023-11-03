---
description: 提供された URL のリストをDynamic Media CDN（コンテンツ配布ネットワーク）プロバイダーに転送して、HTTP 応答の既存のキャッシュを無効にします。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 3%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

提供された URL のリストをDynamic Media CDN（コンテンツ配布ネットワーク）プロバイダーに転送して、HTTP 応答の既存のキャッシュを無効にします。

## cdnCacheInvalidation：概要 {#section-4f70d2bc79d64288b961836ab17e9690}

CDN キャッシュの無効化により、CDN ネットワークを介して無効化要求が処理された後、これらの URL に対するすべての HTTP 要求が、Dynamic Mediaネットワーク上の現在の公開済みデータに対して再検証されます。 Dynamic Mediaサービスの URL 構造に接続されておらず、会社の作成時に割り当てられたDynamic Media会社のルート ID と直接一致する URL は、リクエスト全体の API エラーの原因となります。 CDN が無効と見なすことをサポートしていない無効な URL は、また、リクエスト全体の API エラーになります。

**使用頻度：ルール**

この機能の使用頻度を制御するルールは、Dynamic Mediaの CDN パートナーが制御します。 CDN は、ユーザーに対するサービスの最適なパフォーマンスを維持するために、これらの無効化の応答性を低下させるための裁量を保持します。 Dynamic Mediaにこの機能の過剰使用が通知された場合、Adobeは、会社単位で、またはサービス全体をまたいで、この機能を無効にする必要があります。

**確認メール**

Dynamic Media CDN パートナーからの確認 E メールは、リストの作成者に送信することも、他の 5 つまでの E メールアドレスに送信することもできます。 API は、電子メールで参照されている URL がクリアされたことを CDN ネットワーク全体に通知すると、確認を送信します。 への 1 回の呼び出し `cdnCacheInvalidation` は、提供された URL の数が、Dynamic Mediaが 1 回の通知で CDN パートナーに配信できる数を超えた場合に、複数の電子メールを送信できます。 現在のところ、リクエストが 100 個を超える場合に該当しますが、CDN パートナーのリクエストに基づいて変更される可能性があります。

**次の日からサポート**

6.0

## 認証済みユーザータイプ {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## パラメーター {#section-bd1ed2b7419945d19a2ebd5668499f72}

**入力** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 名前</b> </th> 
   <th class="entry"> <b> 種類</b> </th> 
   <th class="entry"> <b> 必須</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> 無効にする URL と関連付けられている会社へのハンドル。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types:UrlArray</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> CDN キャッシュから無効にする URL の最大 1,000 個のリスト。 無効にするには、すべての URL にDynamic Media会社のルート ID が含まれている必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 名前</b> </th> 
   <th class="entry"> <b> 種類</b> </th> 
   <th class="entry"> <b> 必須</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パージリクエストを参照するハンドル。 </p> <p>The <span class="codeph"> cdnCacheInvalidation</span> API は、ほぼ即座にキャッシュを無効化するようになりました（約 5 秒）。 そのため、通常、無効化ステータスに対するポーリングは必要なくなりました。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パージリクエストが完了するまでの推定秒数。 クライアントは、この時間待ってからステータスをポーリングする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-f414361a58e84dfcbbac30a358d02125}

この例では、CDN キャッシュで無効化する 4 つの URL をリクエストします。 応答には、操作の成功の概要カウントと、CDN から直接提供されるエラーの詳細のリストが含まれ、クライアントがこの機能を使用するのを支援します。

`getCdnCacheInvalidationStatus` 操作.

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
