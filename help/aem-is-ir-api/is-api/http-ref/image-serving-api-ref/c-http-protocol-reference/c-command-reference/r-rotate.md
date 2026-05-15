---
title: 循環
description: 画像を回転。 指定した角度で画像、テキスト、または単色レイヤーを回転します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
TQID: 'https://experienceleague.adobe.com/WDC8SRJEBqspJidlNPxLvwmX-HMQG1zC6wwHNJIXLK4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 266
ht-degree: 2%

---

# 循環{#rotate}

画像を回転。 指定した角度で画像、テキスト、または単色レイヤーを回転します。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">角度</span> </p> </td> 
  <td class="stentry"> <p>回転角度（実数）。 </p></td> 
 </tr> 
</table>

正の角度は時計回りに回転します。 レイヤーのアンカーポイント（`anchor=`または`catalog::Anchor`）が回転の中心になります。 レイヤーの長方形を拡大し、必要に応じて回転データの周囲に取り付けて、切り抜きを避けます。 レイヤーの背景領域を`color=`で塗りつぶした後、回転が適用されます。 修飾子`bgColor=`を使用して、回転後にバウンディング長方形に背景色を追加できます。

## プロパティ {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はレイヤー0に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0` （回転なし）。

## 例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

画像カタログの画像の左上隅付近に「販売中」ラベルを配置します。 ラベル画像は既に300 x 300 ビューのサイズが正しく設定されており、左に30°回転する必要があります。 ラベルを強調するには、テキストボックスに白い半不透明の色を塗りつぶします。

`http:// *` サーバー`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

`size=`をレイヤー0に適用して、`wid=`と`hei=`を使用せずにビューサイズを設定します。 このメソッドを使用すると、最終サイズ `labelImage`を変更せずに`myImageId`のサイズを変更できます。 また、`scl=1`を指定します。指定しない場合、コンポジット画像は`attribute::DefaultPix`に拡大・縮小されます（0,0に設定されていない限り）。 修飾子`color=`は、回転する前に、半不透明の背景色をテキストボックスに追加します。

両方のレイヤーの原点は左上隅に設定され、目的の整列を実現します。 レイヤー1の原点は、回転した後に`labelImage`に適用されます。

回転したテキストの例については、[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の[例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)を参照してください。

## 関連項目 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)、[bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab)、[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
