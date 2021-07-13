---
description: 埋め込まれた名前付きパスのバウンディングボックスに切り抜くことができます。 次に、この切り抜きによって画像のサイズが変わります。
solution: Experience Manager
title: cropPathE
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# cropPathE{#croppathe}

埋め込まれた名前付きパスのバウンディングボックスに切り抜くことができます。 次に、この切り抜きによって画像のサイズが変わります。

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ）。 </p> <p> <span class="codeph"><span class="varname"> </span></span> pathNameは、レイヤーソース画像に埋め込まれたパスの名前です。パスは、画像コンテンツとの相対的な整列を維持するために、必要に応じて自動的に変換されます。 複数の<span class="codeph"><span class="varname"> pathName</span></span>を指定した場合、サーバは各パスのバウンディングボックスに一度に1つずつ切り抜きます。 ソースイメージ内で<span class="codeph"><span class="varname"> pathName</span></span>が見つからない場合は無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

レイヤー属性。 `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。

`cropPathE=` は、指定した名前のパスがレイヤーソース画像内に見つからない場合、またはレイヤーソースがイメージでない場合は無視されます。

## 初期設定 {#section-d1986aa31af14767aeb1b4a57add67f4}

なし（追加でレイヤーを切り抜かない場合）。

## 関連項目 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[crop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、 [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
