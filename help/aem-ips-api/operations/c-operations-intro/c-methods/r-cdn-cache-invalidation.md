---
description: 指定された URL のリストをDynamic Media CDN （コンテンツ配布ネットワーク）プロバイダーに転送して、HTTP 応答の既存のキャッシュを無効にします。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

指定された URL のリストをDynamic Media CDN （コンテンツ配布ネットワーク）プロバイダーに転送して、HTTP 応答の既存のキャッシュを無効にします。

## cdnCacheInvalidation：概要 {#section-4f70d2bc79d64288b961836ab17e9690}

CDN キャッシュの無効化は、これらの URL のすべての HTTP リクエストを、この無効化リクエストが CDN ネットワークを介して処理された後、Dynamic Media ネットワーク上の現在の公開済みデータに対して強制的に再検証します。 Dynamic Media サービスの URL 構造に接続されておらず、会社の作成時に割り当てられたDynamic Mediaの会社ルート ID と直接一致する URL があると、リクエスト全体で API エラーが発生します。 CDN でサポートされていない無効な URL が無効と見なされた場合も、リクエスト全体で API エラーが発生します。

**使用頻度：ルール**

この機能の使用頻度を制御するルールは、Dynamic Mediaの CDN パートナーによって制御されます。 CDN には、ユーザーに対するサービスの最適なパフォーマンスを維持するために、これらの無効化の応答性を低下させる裁量が保持されます。 この機能の過剰使用をDynamic Mediaに通知された場合、Adobeは、会社ごとに、またはサービス全体で機能を無効にする必要があります。

**確認メール**

Dynamic Media CDN パートナーからの確認メールは、リストの作成者に、または最大 5 つの他のメールアドレスに送信できます。 メールで参照されている URL がクリアされたことを CDN ネットワーク全体に通知すると、API は確認を送信します。 提供される URL の数が、1 回の通知でDynamic Mediaが CDN パートナーに配信できる数を超える場合、`cdnCacheInvalidation` への 1 回の呼び出しで複数のメールを送信できます。 現在のところ、リクエストが 100 個の URL を超える場合ですが、CDN パートナーのリクエストに基づいて変更される可能性があります。

**サポート開始済み**

6.0

## 許可されているユーザータイプ {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## パラメーター {#section-bd1ed2b7419945d19a2ebd5668499f72}

**入力** （`cdnCacheInvalidationParam`）

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> 必須 </b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> 無効にする URL に接続されている会社へのハンドル。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> のタイプ：UrlArray</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> CDN キャッシュから無効にする最大 1,000 個の URL のリスト。 すべての URL が、無効にするDynamic Mediaの会社ルート ID を含んでいる必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力** （`cdnCacheInvalidationReturn`）

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> 必須 </b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パージリクエストを参照するハンドル。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> API で、キャッシュをほぼ即座に（約 5 秒）無効化できるようになりました。 そのため、一般に、無効化ステータスのポーリングは不要になりました。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>消去要求の完了までの推定秒数です。 クライアントは、ポーリング状態の前にこの時間を待機する必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-f414361a58e84dfcbbac30a358d02125}

この例では、CDN キャッシュ内で無効にする 4 つの URL をリクエストします。 応答には、操作の成功の概要カウントと、クライアントがこの機能を使用するのを支援するために CDN から直接提供されるエラーの詳細のリストが含まれています。

`getCdnCacheInvalidationStatus` 操作。

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
