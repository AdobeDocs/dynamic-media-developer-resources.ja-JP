---
title: 件の
description: 解像度ベースの画像の拡大・縮小。 要求された解像度に画像を拡大・縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# 件の{#res}

解像度ベースの画像の拡大・縮小。 要求された解像度に画像を拡大・縮小します。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>ターゲットの解像度（通常、1 インチあたりのピクセル数（実際））。 </p> </td> 
 </tr> 
</table>

スケール係数は、*`val`* を `catalog::Resolution` で割ることで計算されます。 このコマンドは、返信画像の印刷解像度には影響を与えません。

この機能を使用するには、元のソース画像の解像度が分かっていて、`catalog::Resolution` で設定されている必要があります。 アプリケーションによって、解像度の単位は異なる場合があります。 壁紙やファブリックなど、繰り返し可能な 2D テクスチャまたはマテリアルスウォッチの場合、解像度はピクセル/インチまたはピクセル/mm で表すことができます。 航空写真や地図は、ピクセル/マイルまたはピクセル/km で提供する方が良い場合があります。 この場合において、`catalog::Resolution` に用いる単位は、`res=` に用いる単位と同一でなければならない。

また、複数の画像を同じ解像度で合成す `res=` ことで、見えているモノとモノが正しく対応し、適切な解像度で画像を取得することも可能です。

>[!NOTE]
>
>通常、合成画像は、クライアントに返される前に、ターゲットの表示サイズ（`wid=`、`hei=` または `attribute::DefaultPix` で指定）に変更されます。 このサイズ変更を防ぎ、`res=` で指定された正確な解像度の画像を取得するには、`scl=1` を明示的に指定してビュースケーリングを無効にする必要がある場合があります。 これは、サーバーに対して、合成画像を拡大縮小するのではなく、ターゲットの表示サイズに切り抜くように指示します。

## プロパティ {#section-fdbd16e59cff4952a3717146bc91412e}

Source image/mask 属性。 ソース イメージまたはマスクに関連付けられていないレイヤによって無視されます。 画層 0 に適用される `layer=comp` は指定されています。 同じレイヤーに `scale=` または `size=` が指定されている場合は無視されます。

## 初期設定 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

指定しない場合は、`scale=` または `size=` によって倍率が決まります。指定しない場合は、拡大縮小せずにイメージが使用されます。

## 例 {#section-eb06f333e08e4247971fb1b18922597b}

画像レンダリングまたは画像オーサリングで使用するテクスチャ画像を 12 ピクセル/インチのオブジェクト解像度で取得します。 損失のない PNG 形式と、可能な限り最高の品質を得るための高品質の再サンプリングを指定しています。

` http:// *` サーバー `*/myTexture?res=12&fmt=png&resMode=sharp`

## 関連項目 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、[attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
