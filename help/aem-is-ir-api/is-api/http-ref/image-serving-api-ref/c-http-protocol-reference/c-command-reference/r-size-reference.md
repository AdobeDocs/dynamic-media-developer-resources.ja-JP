---
title: サイズ
description: レイヤーサイズ： レイヤーにrotate=、perspective=、およびextend=が適用される前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
TQID: 'https://experienceleague.adobe.com/DQG9OdxhfenQe-vv7opfQUYljxn7N7XaRIsl1LkSry4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 424
ht-degree: 1%

---

# サイズ{#size}

レイヤーサイズ： レイヤーにrotate=、perspective=、およびextend=が適用される前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">幅</span>、<span class="varname">高さ</span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズのピクセル単位の制約（int、int、0以上）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズの制約は、レイヤー0のサイズ（実数、実数、0.0...1.0）に対して正規化されます。 </p> </td> 
 </tr> 
</table>

画像レイヤーに指定した場合、size=は、レイヤー画像の幅、高さ、またはその両方を制約します。 画像は`size=`以下に拡大・縮小されます。 正規化されたサイズを指定した場合、そのサイズはレイヤー0のサイズを基準とします。 *`width`*&#x200B;と&#x200B;*`height`*&#x200B;の両方が指定されている場合、どちらのディメンションも指定されたサイズを超えないように、ソース画像は（2&rbrace;が適用された後に）拡大・縮小されます。 `crop=`ソース長方形の縦横比は、すべての場合において維持されます。 *`width`*&#x200B;または&#x200B;*`height`*&#x200B;は0に設定できます。この場合、値は画像の縦横比に基づいてサーバーによって計算されます。

テキストレイヤーに指定した場合、`size=`はテキストボックスのサイズを指定します。 *`width`*&#x200B;が必要です。*`height`*&#x200B;は0に設定できます。この場合、レイアウトされたテキストの高さがレイヤーの高さとして使用されます。 デフォルトでは、テキストレイアウトエンジンは改行を挿入して、テキストが常に使用可能なスペースに水平に収まるようにします。 *`height`*&#x200B;が指定されている場合、使用可能なスペースに収まらない行はクリップ（`text=`）または省略（`textPs=`）されます。 `text=`は追加の適合モードをサポートしています。詳細については、`textAttr=`を参照してください。

単色レイヤーに指定した場合、`size=`は正確なレイヤーサイズを定義します。両方の値を指定する必要があります（マスクが指定されていない場合）。 `mask=`も指定されている場合、画像レイヤーで画像を拡大・縮小する場合と同じように、マスク画像は`size=`に合うようにサイズが調整されます。

## プロパティ {#section-5f254b66fcba49bcb63f9c9ea40b230c}

レイヤー属性。 `layer=comp`の場合、レイヤー0に適用されます。 `sizeN=`は`layer=0`または`layer=comp`に対して許可されていません。 `sizeN=`は、透かし画像を定義するカタログレコードでのみ`layer=0`および`layer=comp`に使用できます。 この場合、`sizeN`は、透かしを適用する合成画像に対する透かし画像の拡大・縮小を定義します。 `size=`が指定されている場合、`res=`と`scale=`はこのレイヤーでは無視されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`、レイヤーサイズに制限はありません。 画像レイヤーの場合、レイヤーサイズは、`crop=`、`scale=`、または`res=`操作が適用された後のレイヤー画像サイズに基づいて決定されます。 テキストレイヤーの場合、`size=`が指定されていない場合、レイヤーはレンダリングされたテキストに合わせて自動的にサイズ調整されます。

べた塗りのレイヤーには、完全に指定された`size=`、`mask=`、`clipPath=`のいずれかが必要です。

## 例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の[例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)を参照してください。

## 関連項目 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)、[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)、[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、[&#x200B; テキストレイヤー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
