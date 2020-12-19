---
description: 埋め込まれた名前付きパスのバウンディングボックスに切り抜くことができます。 次に、画像のサイズを切り抜きます。
seo-description: 埋め込まれた名前付きパスのバウンディングボックスに切り抜くことができます。 次に、画像のサイズを切り抜きます。
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
topic: Scene7 Image Serving - Image Rendering API
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---


# cropPathE{#croppathe}

埋め込まれた名前付きパスのバウンディングボックスに切り抜くことができます。 次に、画像のサイズを切り抜きます。

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ） </p> <p> <span class="codeph"><span class="varname"> pathNameは、レイヤーソース画像に埋め込まれたパスの名前です。</span></span> パスは、画像コンテンツとの相対的な位置揃えを維持するために、必要に応じて自動的に変換されます。 複数の<span class="codeph"><span class="varname"> pathName</span></span>を指定した場合、サーバは各パスのバウンディングボックスを1つずつ切り抜きます。 ソース画像内に<span class="codeph"><span class="varname"> pathName</span></span>が見つからない場合は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。

`cropPathE=` は、指定した名前のパスがレイヤーソース画像内に見つからない場合、またはレイヤーソースが画像でない場合は無視されます。

## 初期設定 {#section-d1986aa31af14767aeb1b4a57add67f4}

なし（レイヤーの切り抜きを行わない）。

## 関連項目 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[切り抜き](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、 [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
