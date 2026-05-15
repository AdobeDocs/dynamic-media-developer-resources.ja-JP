---
description: 画像サーバープロキシを使用して、日本の電話機の画像のサイズを変更できます。
solution: Experience Manager
title: 画像サーバープロキシ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
TQID: 'https://experienceleague.adobe.com/wJ6wQsus1QmfFbZ4FCM1nAmPdWacySEWaV9vfAA1fyg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 0%

---

# 画像サーバープロキシ{#image-server-proxy}

画像サーバープロキシを使用して、日本の電話機の画像のサイズを変更できます。

## URL の形式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS プロキシのURL形式は、通常のIS リクエストと非常によく似ています。 プロキシに渡されたIS修飾子はすべて、Image Serverに渡されます。 IS修飾子に関する情報は、[HTTP プロトコルリファレンス ](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)で確認できます。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## プロキシ固有の修飾子リスト {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の幅として使用するデバイスの使用可能な幅の割合を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の高さとして使用できるデバイスの使用可能な高さの割合を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>応答サイズを制限するデバイスのMemory Limit Embedded Media プロパティの割合を指定します。 これはjpg応答にのみ適用されます。 応答サイズが指定されたパーセント内になるまで、画像の画質が低下します。 </p></td> 
 </tr> 
</table>

## 埋め込み画像のメモリ制限 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

デバイスがweb ページに埋め込むことができる画像のサイズに制限がある場合、応答形式がjpgである限り、画像サイズはそのサイズに制限されます。 プロキシは、デバイスに制限がない場合、応答を500 MBに制限します。

## バックエンド処理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

プロキシは、Device Atlas データファイルを1日1回ダウンロード、検証、および読み込みます。 検証では、異なるデバイスに対して異なるプロパティを引き出し、新しいデータを受け入れる前に想定される値と比較します。
