---
description: 提供されたURLのリストをDynamic Media CDN（コンテンツ配布ネットワーク）プロバイダーに転送して、HTTP応答の既存のキャッシュを無効にします。
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 3%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

提供されたURLのリストをDynamic Media CDN（コンテンツ配布ネットワーク）プロバイダーに転送して、HTTP応答の既存のキャッシュを無効にします。

## cdnCacheInvalidation:について {#section-4f70d2bc79d64288b961836ab17e9690}

CDNキャッシュの無効化は、CDNネットワークを介して無効化要求が処理された後に、これらのURLに対するすべてのHTTP要求が、Dynamic Mediaネットワーク上の現在の公開済みデータに対して再検証されるようにします。 Dynamic MediaサービスのURL構造に接続されておらず、会社の作成時に割り当てられたDynamic Media会社のルートIDに直接一致するURLは、リクエスト全体でAPIエラーが発生します。 CDNが無効と見なすことをサポートしていない無効なURLは、また、リクエスト全体のAPIエラーになります。

**使用頻度：ルール**

この機能の使用頻度を制御するルールは、Dynamic MediaのCDNパートナーによって制御されます。 CDNは、ユーザーに対するサービスの最適なパフォーマンスを維持するために、これらの無効化の応答性を低下させる裁量を保持します。 Dynamic Mediaにこの機能の過度の使用が通知された場合は、会社ごと、またはサービス全体をまたいで、この機能を無効にする必要があります。

**確認Eメール**

Dynamic Media CDNパートナーからの確認Eメールは、リストの作成者に送信することも、他の5つまでのEメールアドレスに送信することもできます。 APIは、Eメールで参照されているURLがクリアされたことをCDNネットワーク全体に通知すると、確認を送信します。 `cdnCacheInvalidation`への1回の呼び出しで、指定されたURLの数が、Dynamic Mediaが1回の通知でCDNパートナーに配信できる数を超えた場合に、複数の電子メールを送信できます。 現在、リクエストが100個を超える場合に発生しますが、CDNパートナーのリクエストに基づいて変更される可能性があります。

**次の日からサポート**

6.0

## 許可されたユーザーの種類 {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## パラメータ {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

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
   <td> <p> 無効にするURLと関連付けられている会社へのハンドル。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 型：UrlArray[がた：UrlArray]</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> CDNキャッシュから無効化する最大1000個のURLのリスト。 無効化するDynamic Media会社のルートIDをすべてのURLに含める必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>パージリクエストを参照するハンドル。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> APIは、ほぼ即座にキャッシュを無効化します（約5秒）。 したがって、通常、無効化ステータスのポーリングは不要になりました。 </p> 
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

この例では、4つのURLをCDNキャッシュで無効化します。 応答には、操作の成功の概要カウントと、CDNから直接提供されるエラーの詳細のリストが含まれ、クライアントがこの機能を使用するのを支援します。

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
