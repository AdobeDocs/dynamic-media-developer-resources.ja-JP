---
description: 提供されたURLのリストをScene7 CDN(Content Distribution Network)プロバイダに転送し、HTTP応答の既存のキャッシュを無効にします。
seo-description: 提供されたURLのリストをScene7 CDN(Content Distribution Network)プロバイダに転送し、HTTP応答の既存のキャッシュを無効にします。
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# cdnCacheInvalidation{#cdncacheinvalidation}

提供されたURLのリストをScene7 CDN(Content Distribution Network)プロバイダに転送し、HTTP応答の既存のキャッシュを無効にします。

## cdnCacheInvalidation:バージョン情報 {#section-4f70d2bc79d64288b961836ab17e9690}

CDNキャッシュの無効化は、CDNネットワークを介して処理された後、Scene7ネットワーク上の現在公開されているデータに対して、これらのURLに対するすべてのHTTP要求を強制的に再検証します。 Scene7サービスのURL構造に接続されておらず、会社の作成時に割り当てられたScene7会社のルートIDと直接一致するURLは、要求全体のAPIエラーになります。 CDNが無効と見なす無効なURLがサポートしていない場合は、リクエスト全体のAPIエラーも発生します。

**使用頻度：ルール**

この機能の使用頻度を制御するルールは、Scene7のCDNパートナーによって制御されます。 CDNは、これらの無効化の応答性を低下させ、ユーザーに対するサービスの最適なパフォーマンスを維持するための裁量を保持します。 この機能の過剰使用をScene7に通知する場合は、会社単位または全体で機能を無効にする必要があります。

**確認電子メール**

Scene7 CDNパートナーからの確認電子メールは、リストの作成者に送信するか、その他5つまでの電子メールアドレスに送信できます。 APIは、電子メールで参照されているURLがクリアされたことをCDNネットワーク全体に通知された場合に、確認を送信します。 1回の通知でCDNパ `cdnCacheInvalidation` ートナーに提供できるURL数を超えた場合、1回の呼び出しで複数の電子メールを送信できます。 現在は、リクエストが100個を超えるが、CDNパートナーのリクエストに基づいて変更される可能性がある場合です。

**次の日付以降**

6.0

## 認証されたユーザータイプ {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## パラメータ {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** ( `cdnCacheInvalidationParam`)

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
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> 無効にするURLに関連付けられている会社へのハンドル。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span></span> </p> </td> 
   <td> <p> <span class="codeph"> タイプ：UrlArray</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> CDNキャッシュから無効にするURLのリストです。最大1,000個のURLが含まれます。 すべてのURLに、無効にするScene7の会社ルートIDが含まれている必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>パージ要求を参照するハンドル。 </p> <p>cdnCacheInvalidation <span class="codeph"></span> APIは、ほぼ直ちに（約5秒）キャッシュを無効にするようになりました。 したがって、通常、無効化ステータスのポーリングは不要になります。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>削除要求の完了までの推定秒数。 クライアントは、この時間まで待機してからステータスをポーリングする必要があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-f414361a58e84dfcbbac30a358d02125}

この例では、CDNキャッシュで無効にする4つのURLを要求します。 応答には、操作の成功の概要カウントと、クライアントがこの機能を使用するのを支援するためにCDNから直接提供されるエラーの詳細のリストが含まれます。

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

