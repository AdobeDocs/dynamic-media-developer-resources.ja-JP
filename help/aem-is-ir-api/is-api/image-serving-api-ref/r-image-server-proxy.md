---
description: イメージサーバープロキシを使用して、日本語の電話用の画像のサイズを変更できます。
seo-description: イメージサーバープロキシを使用して、日本語の電話用の画像のサイズを変更できます。
seo-title: イメージサーバープロキシ
solution: Experience Manager
title: イメージサーバープロキシ
topic: Scene7 Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# イメージサーバプロキシ{#image-server-proxy}

イメージサーバープロキシを使用して、日本語の電話用の画像のサイズを変更できます。

## URL の形式 {#section-2e8c40b0547c4f99874cdf502b338940}

ISプロキシのURL形式は、通常のIS要求と非常に似ています。 プロキシに渡されるIS修飾子はすべて、Image Serverに渡されます。 IS修飾子に関する情報は、『[HTTPプロトコルリファレンス](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)』を参照してください。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## プロキシ固有の修飾子リスト{#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>デバイスで使用可能な画像の幅として使用する幅のパーセンテージを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>デバイスで使用可能な画像の高さとして使用する高さの割合を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>デバイスのMemory Limit Embedded Mediaプロパティの、応答サイズを制限するパーセンテージを指定します。 これは、jpgの応答にのみ適用されます。 画質は、応答サイズが指定したパーセンテージ内になるまで低下します。 </p></td> 
 </tr> 
</table>

## 埋め込み画像のメモリ制限{#section-52f7c69ed8a341ceabf92ceee19b0f36}

デバイスで、Webページに埋め込むことのできる画像のサイズに制限がある場合、応答形式がjpgである限り、画像のサイズはそのサイズに制限されます。 デバイスに制限がない場合、プロキシは応答を500 MBに制限します。

## バックエンド処理{#section-bdf7c294b6824de9969c97fc1f8aa6d3}

プロキシは、Device Atlasデータファイルを1日1回ダウンロード、検証および読み込みします。 新しいデータを受け入れる前に、検証によって異なるデバイスの異なるプロパティが取り出され、期待値と比較されます。
