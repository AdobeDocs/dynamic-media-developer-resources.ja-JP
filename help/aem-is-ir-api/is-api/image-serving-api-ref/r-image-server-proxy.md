---
description: イメージサーバプロキシを使用して、日本の携帯電話の画像のサイズを変更できます。
solution: Experience Manager
title: Image Server プロキシ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Image Server プロキシ{#image-server-proxy}

イメージサーバプロキシを使用して、日本の携帯電話の画像のサイズを変更できます。

## URL の形式 {#section-2e8c40b0547c4f99874cdf502b338940}

IS プロキシの URL 形式は、通常の IS リクエストとよく似ています。 プロキシに渡される IS 修飾子は、Image Server を通じて渡されます。 IS 修飾子の情報は、 [HTTP プロトコルリファレンス](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## プロキシ固有の修飾子リスト {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の幅として使用する、デバイスで使用可能な幅のパーセンテージを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>画像の高さとして使用する、デバイスで使用可能な高さのパーセンテージを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>デバイスのメモリ制限埋め込みメディアプロパティのパーセンテージを指定して、応答サイズを制限します。 これは、jpg 応答にのみ適用されます。 応答サイズが指定の割合内になるまで、画像の画質が下がります。 </p></td> 
 </tr> 
</table>

## 埋め込み画像のメモリ制限 {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Web ページに埋め込む画像のサイズに制限がある場合、応答形式が jpg である限り、画像サイズはそのサイズに制限されます。 デバイスに制限がない場合、プロキシは応答を 500 MB に制限します。

## バックエンド処理 {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

プロキシは、Device Atlas データファイルを 1 日 1 回ダウンロード、検証、読み込みます。 検証では、異なるデバイスの異なるプロパティを取り出し、新しいデータを受け入れる前に期待される値と比較します。
