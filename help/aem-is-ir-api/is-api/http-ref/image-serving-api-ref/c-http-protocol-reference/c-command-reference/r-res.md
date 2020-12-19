---
description: 解像度ベースの画像の拡大/縮小 画像を目的の解像度に拡大・縮小します。
seo-description: 解像度ベースの画像の拡大/縮小 画像を目的の解像度に拡大・縮小します。
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# res{#res}

解像度ベースの画像の拡大/縮小 画像を目的の解像度に拡大・縮小します。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>ターゲットの解決；通常は、ピクセル/インチ（実数）で表します。 </p> </td> 
 </tr> 
</table>

スケール係数は、*`val`*&#x200B;を`catalog::Resolution`で割って計算されます。 このコマンドは、返信画像の印刷解像度には影響しません。

この機能を使用するには、元のソース画像の解像度を`catalog::Resolution`で確認し、設定する必要があります。 アプリケーションによっては、解像度の単位が異なる場合があります。 繰り返し可能な2Dテクスチャまたはマテリアルスウォッチ（壁紙やファブリックなど）の場合、解像度はピクセル/インチまたはピクセル/mmで表すことができます。 航空写真や地図は、ピクセル/マイルまたはピクセル/kmで配信する方が良い場合があります。 いずれの場合も、`catalog::Resolution`に使用する単位は、`res=`に使用する単位と同じでなければなりません。

正確な解像度で画像を取得するだけでなく、`res=`を使用して複数の画像を同じ解像度で組み合わせることも可能で、画像に表示される項目が互いに正確な比率を保つことができます。

>[!NOTE]
>
>通常、合成画像はターゲット表示のサイズ（`wid=`、`hei=`、または`attribute::DefaultPix`で指定）に合わせてサイズ変更されてからクライアントに返されます。 このサイズ変更を防ぎ、`res=`で指定された解像度で画像を取得するには、`scl=1`を明示的に指定して表示の拡大/縮小を無効にする必要がある場合があります。 これにより、サーバは、合成画像を拡大・縮小するのではなく、ターゲット表示のサイズに合わせて切り抜くように指定します。

## プロパティ {#section-fdbd16e59cff4952a3717146bc91412e}

ソース画像/マスク属性 ソース画像またはマスクに関連付けられていないレイヤーでは無視されます。 `layer=comp`に対して画層0に適用されます。 同じレイヤーに対して`scale=`または`size=`が指定されている場合は無視されます。

## 初期設定 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

指定しなかった場合は、`scale=`または`size=`によって尺度が決まります。指定しなかった場合は、画像は尺度変更せずに使用されます。

## 例 {#section-eb06f333e08e4247971fb1b18922597b}

12 pixel/インチのオブジェクト解像度でテクスチャイメージを取得し、イメージレンダリングまたはイメージオーサリングで使用します。 損失のないPNG形式を指定し、最高の画質を得るためにより高い画質のリサンプリングを行います。

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## 関連項目 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
