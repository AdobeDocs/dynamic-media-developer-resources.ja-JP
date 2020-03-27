---
description: イメージサーバプロキシを使用して、日本語の電話用の画像のサイズを変更できます。
seo-description: イメージサーバプロキシを使用して、日本語の電話用の画像のサイズを変更できます。
seo-title: Image Serverプロキシ
solution: Experience Manager
title: Image Serverプロキシ
topic: Scene7 Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Image Serverプロキシ{#image-server-proxy}

イメージサーバプロキシを使用して、日本語の電話用の画像のサイズを変更できます。

## URL の形式 {#section-2e8c40b0547c4f99874cdf502b338940}

ISプロキシのURL形式は、通常のISリクエストと非常に似ています。 プロキシに渡されるIS修飾子はすべて、Image Serverに渡されます。 IS修飾子に関する情報は、『 [HTTP Protocol Reference』を参照してください](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## プロキシ固有の修飾子のリスト {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;数値&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の幅として使用するデバイスの使用可能な幅の割合を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;数値&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の高さとして使用するデバイスの使用可能な高さの割合を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;数値&gt;</span> </p></td> 
  <td class="stentry"> <p>デバイスの埋め込みメディアのメモリ制限プロパティの、応答サイズを制限する割合を指定します。 これはjpgの応答にのみ適用されます。 応答サイズが指定した割合内になるまで、画像の画質が低下します。 </p></td> 
 </tr> 
</table>

## 埋め込み画像のメモリ制限 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

デバイスでWebページに埋め込める画像のサイズに制限がある場合、応答形式がjpgである限り、画像のサイズはそのサイズに制限されます。 デバイスに制限がない場合、プロキシは応答を500 MBに制限します。

## バックエンド処理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

プロキシは、Device Atlasデータファイルを1日1回ダウンロード、検証、読み込みします。 新しいデータを受け入れる前に、検証では、デバイスごとに異なるプロパティを取り出し、期待値と比較します。
