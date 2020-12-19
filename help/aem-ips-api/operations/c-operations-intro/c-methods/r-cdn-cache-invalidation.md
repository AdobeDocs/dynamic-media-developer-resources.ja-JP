---
description: 提供されたURLのリストをScene7CDN(Content Distribution Network)プロバイダーに転送し、HTTP応答の既存のキャッシュを無効にします。
seo-description: 提供されたURLのリストをScene7CDN(Content Distribution Network)プロバイダーに転送し、HTTP応答の既存のキャッシュを無効にします。
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 3%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

提供されたURLのリストをScene7CDN(Content Distribution Network)プロバイダーに転送し、HTTP応答の既存のキャッシュを無効にします。

## cdnCacheInvalidation:{#section-4f70d2bc79d64288b961836ab17e9690}について

CDNキャッシュの無効化は、CDNネットワークを介して処理された後、これらのURLに対するすべてのHTTP要求を、Scene7ネットワーク上の現在の公開済みデータに対して再検証するように強制します。 会社の作成時に割り当てられたScene7サービスのURL構造に接続されていないURLで、Scene7会社のルートIDと直接一致するURLは、リクエスト全体のAPIエラーになります。 CDNがサポートしない無効なURLで、無効と見なすものは、リクエスト全体のAPIエラーにもなります。

**使用頻度：ルール**

この機能の使用頻度を制御するルールは、Scene7のCDNパートナーが制御します。 CDNは、これらの無効化の応答性を低下させ、ユーザーに対するサービスの最適なパフォーマンスを維持するための裁量を保持します。 この機能の過度の使用をScene7に通知した場合は、会社ごとに、または全体を通じて、この機能を無効にする必要があります。

**確認電子メール**

Scene7CDNパートナーからの確認電子メールは、リストの作成者に送信するか、他の5つまでの電子メールアドレスに送信できます。 APIは、電子メール内で参照されているURLがクリアされたことをCDNネットワーク全体に通知された場合に、確認を送信します。 `cdnCacheInvalidation`への1回の呼び出しで、1回の通知でScene7がCDNパートナーに配信できるURL数を超えた場合に、複数の電子メールを送信できます。 現在、リクエストが100個を超えるが、CDNパートナーのリクエストに基づいて変更される可能性がある場合、この問題を修正しました。

**次の日付でサポート**

6.0

## 認証済みユーザータイプ{#section-0d7895e733d54fb68beb8d231a04e4c9}

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
   <td> <p> 無効にするURLに接続されている会社へのハンドルです。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> 型：UrlArray</span> </p> </td> 
   <td> <p> はい </p> </td> 
   <td> <p> CDNキャッシュから無効にするURLを最大1,000個リストします。 無効にするScene7会社のルートIDは、すべてのURLに含まれている必要があります。 </p> </td> 
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
   <td colname="col4"> <p>パージ要求を参照するハンドル。 </p> <p><span class="codeph"> cdnCacheInvalidation</span> APIは、キャッシュをほとんど直ちに無効にします（～5秒）。 したがって、通常、無効状態のポーリングは必要ありません。 </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>削除要求が完了するまでの推定秒数。 クライアントは、この時間を待ってからポーリング状態になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-f414361a58e84dfcbbac30a358d02125}

この例では、CDNキャッシュで無効にする4つのURLをリクエストします。 応答には、操作の成功の概要カウントと、CDNから直接提供されるエラーの詳細のリストが含まれ、この機能の使用を支援します。

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

