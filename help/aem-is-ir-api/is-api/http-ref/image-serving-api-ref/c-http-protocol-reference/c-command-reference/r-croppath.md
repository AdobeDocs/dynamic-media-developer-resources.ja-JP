---
title: cropPathE
description: 埋め込まれたパスのバウンディングボックスに切り抜くことができます。 この切り抜きは、次に画像のサイズを変更します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
TQID: 'https://experienceleague.adobe.com/zjmnN-7ACO78rMKs7H2S6b989IEHi2I9nPrS5FPaEFA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 1%

---

# cropPathE{#croppathe}

埋め込まれたパスのバウンディングボックスに切り抜くことができます。 この切り抜きは、次に画像のサイズを変更します。

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>レイヤーソース画像に埋め込まれたパスの名前（ASCIIのみ）。 </p> <p> <span class="codeph"><span class="varname"> pathName</span></span>は、レイヤーソース画像に埋め込まれたパスの名前です。 パスは、画像コンテンツとの相対的な整合性を維持するために、必要に応じて自動的に変換されます。 複数の<span class="codeph"><span class="varname"> pathName</span></span>が指定されている場合、サーバーは各パスのバウンディングボックスに1つずつ切り抜きます。 ソース画像に見つからない<span class="codeph"><span class="varname"> pathName</span></span>はすべて無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

レイヤー属性。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーでは無視されます。

指定された名前のパスがレイヤーソース画像に見つからない場合、またはレイヤーソースが画像でない場合、`cropPathE=`は無視されます。

## 初期設定 {#section-d1986aa31af14767aeb1b4a57add67f4}

なし（レイヤーの追加の切り抜きはありません）。

## 関連項目 {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[切り抜き](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab)、[clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
