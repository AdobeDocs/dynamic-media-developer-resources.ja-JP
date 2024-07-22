---
description: Image Server プロキシを使用すると、日本の携帯電話用の画像のサイズを変更できます。
solution: Experience Manager
title: Image server プロキシ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Image server プロキシ{#image-server-proxy}

Image Server プロキシを使用すると、日本の携帯電話用の画像のサイズを変更できます。

## URL の形式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS プロキシの URL 形式は、通常の IS リクエストに非常によく似ています。 プロキシに渡された IS 修飾子は、Image Server に渡されます。 IS 修飾子に関する情報は、[HTTP プロトコルリファレンス ](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e) を参照してください。

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## プロキシ固有の修飾子リスト {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の幅として使用するデバイスの使用可能な幅のパーセンテージを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の高さとして使用するデバイスの使用可能な高さの割合を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>応答サイズを制限するデバイスの Memory Limit Embedded Media プロパティの割合を指定します。 これは、jpg 応答にのみ適用されます。 応答サイズが指定のパーセンテージに収まるまで、画像の画質が低下します。 </p></td> 
 </tr> 
</table>

## 埋め込み画像のメモリ制限 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Web ページに埋め込むことができる画像のサイズがデバイスで制限されている場合、応答形式が jpg である限り、画像のサイズはそのサイズに制限されます。 デバイスに制限がない場合、プロキシは応答を 500 MB に制限します。

## バックエンド処理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

プロキシは、Device Atlas データ ファイルを 1 日に 1 回ダウンロード、検証、およびロードします。 検証では、異なるデバイスに対して異なるプロパティを取り出し、それらを期待値と比較してから、新しいデータを受け入れます。
