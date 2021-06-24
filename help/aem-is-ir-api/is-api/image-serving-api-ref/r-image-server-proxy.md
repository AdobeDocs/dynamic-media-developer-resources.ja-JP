---
description: Image Serverプロキシを使用して、日本の携帯電話の画像のサイズを変更できます。
solution: Experience Manager
title: Image Serverプロキシ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Image Serverプロキシ{#image-server-proxy}

Image Serverプロキシを使用して、日本の携帯電話の画像のサイズを変更できます。

## URL の形式 {#section-2e8c40b0547c4f99874cdf502b338940}

ISプロキシのURL形式は、通常のISリクエストと非常に似ています。 プロキシに渡されるIS修飾子は、Image Serverを通じて渡されます。 IS修飾子の情報は、[HTTPプロトコルリファレンス](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e)で確認できます。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## プロキシ固有の修飾子リスト {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の幅として使用する、デバイスで使用可能な幅のパーセンテージを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の高さとして使用する、デバイスで使用可能な高さのパーセンテージを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>デバイスのメモリ制限埋め込みメディアプロパティの割合を指定して、応答サイズを制限します。 これは、jpg応答にのみ適用されます。 応答サイズが指定した割合内になるまで、画像の画質は下がります。 </p></td> 
 </tr> 
</table>

## 埋め込み画像のメモリ制限 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

デバイスでWebページに埋め込める画像のサイズに制限がある場合、応答形式がjpgである限り、画像のサイズはそのサイズに制限されます。 デバイスに制限がない場合、プロキシは応答を500 MBに制限します。

## バックエンド処理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

プロキシは、Device Atlasデータファイルを1日1回ダウンロード、検証、読み込みます。 検証は、異なるデバイスの異なるプロパティを取り出し、新しいデータを受け入れる前に、期待される値と比較します。
