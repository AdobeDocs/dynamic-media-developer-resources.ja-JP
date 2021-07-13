---
description: 解像度ベースの画像の拡大/縮小 画像を必要な解像度に拡大/縮小します。
solution: Experience Manager
title: res
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 1%

---

# res{#res}

解像度ベースの画像の拡大/縮小 画像を必要な解像度に拡大/縮小します。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>ターゲットの解決通常は、1インチあたりのピクセル数（実数）です。 </p> </td> 
 </tr> 
</table>

スケール係数は、*`val`*&#x200B;を`catalog::Resolution`で割って計算されます。 このコマンドは、返信画像の印刷解像度に影響を与えません。

この機能を使用するには、元のソース画像の解像度を`catalog::Resolution`に設定する必要があります。 アプリケーションによっては、解像度の単位が異なる場合があります。 繰り返し可能な2Dテクスチャや、壁紙やファブリックなどのマテリアルスウォッチの場合、解像度はピクセル/インチまたはピクセル/mmで表すことができます。 空中写真やマップは、ピクセル/マイルまたはピクセル/kmで提供される方が良い場合があります。 いずれの場合も、`catalog::Resolution`に使用する単位は、`res=`に使用する単位と同じである必要があります。

正確な解像度の画像を得るだけでなく、`res=`を用いて、複数の画像を同じ解像度で組み合わせることも可能で、これらの画像に表示される項目が互いに正確に比例して表示されます。

>[!NOTE]
>
>通常、合成画像は、クライアントに返される前に、ターゲットのビューサイズ（`wid=`、`hei=`、`attribute::DefaultPix`で指定）に合わせてサイズ変更されます。 このサイズ変更を防ぎ、`res=`で指定された解像度で画像を取得するには、`scl=1`を明示的に指定してビューの拡大/縮小を無効にする必要が生じる場合があります。 これは、サーバに対して、合成画像を拡大縮小するのではなく、ターゲットのビューサイズに合わせて切り抜くように指示します。

## プロパティ {#section-fdbd16e59cff4952a3717146bc91412e}

ソースイメージ/マスクのアトリビュート ソース画像またはマスクに関連付けられていないレイヤーでは無視されます。 `layer=comp`に対してレイヤ0に適用されます。 `scale=`または`size=`が同じレイヤーに対して指定されている場合は無視されます。

## 初期設定 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

指定しなかった場合は、 `scale=`または`size=`によって拡大率が決定されます。どちらも指定されていない場合は、拡大縮小せずに画像が使用されます。

## 例 {#section-eb06f333e08e4247971fb1b18922597b}

12ピクセル/インチのオブジェクト解像度でテクスチャイメージを取得し、Image RenderingまたはImage Authoringで使用します。 最高の画質を得るために、損失のないPNG形式とより高品質な再サンプリングを指定します。

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## 関連項目 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) 、 [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
