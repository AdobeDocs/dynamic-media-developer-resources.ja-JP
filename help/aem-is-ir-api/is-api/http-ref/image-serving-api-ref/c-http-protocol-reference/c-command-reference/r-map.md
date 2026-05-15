---
title: マップ
description: 画像マップデータ： このレイヤーの画像マップデータを提供します。 このレイヤーのカタログマップのデータを上書きします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c1fbb50-98ec-4d9a-b608-93d60d687069
TQID: 'https://experienceleague.adobe.com/9JJUVcw5-wl0B-rP-m6DC1c1DGIqxaV2UgboocFGGV8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 2%

---

# マップ{#map}

画像マップデータ： このレイヤーの画像マップデータを提供します。 このレイヤーのcatalog::Mapのデータを上書きします。

`map=[ *`文字列`*]mapA=[ *`文字列A`*]`

<table id="simpletable_2E32B25D5F6246A18A8AF817903877ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>このレイヤーの画像マップデータはレイヤー座標で表示されます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> stringA</span></span> </p></td> 
  <td class="stentry"> <p>ソース画像座標のこのレイヤーの画像マップデータ。 </p></td> 
 </tr> 
</table>

空の文字列は、このレイヤーが画像マップを提供しないことを示します。 解析の問題を回避するには、文字列をHTTP エンコードする必要があります。

*`string`*&#x200B;で発生するすべてのアンパサンド（&amp;）文字は、http エンコードされている必要があります。

`mapA=`と`catalog::Map`はソース画像座標でマップデータを指定しますが、`map=`はレイヤー長方形の左上隅に対するレイヤー座標を仮定します（`rotate=`と`extend=`が適用された後）。

出力画像マップは常にレイヤーの長方形にクリップされます。 `shape`属性を省略するか、`default`に設定すると、レイヤー長方形全体が画像マップ領域として使用されます。

## プロパティ {#section-a18d9ea95c71414a905a68b8839c0843}

レイヤー属性。 `layer=comp`に適用すると、指定されたマップ データは、他のすべての画像マップの背後に配置されます。 `req=map`以外は無視されます。 エフェクトレイヤーでは無視されます。 `map=`が指定されている場合、`mapA=`も無視されます。

## 初期設定 {#section-620c19b3f3b84ba49706062de3f12f05}

`catalog::Map`は、`map=`が指定されていない場合に使用されます。

## 例 {#section-cd7691c94f984222845c86dcb0051ce8}

シンプルなテキストレイヤー用に長方形の画像マップを定義します。

`…&layer=1&text=Scene7&map=<area%20alt=Scene7%20href=www.scene7.com>&…`

（ほとんどが）デフォルト属性を持つ`AREA`要素を使用して、レイヤーの長方形全体のマップ領域を挿入します。

## 関連項目 {#section-bc1d946fdf4b47bf9742a986800aa9b5}

[画像マップ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab), [req=map](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
