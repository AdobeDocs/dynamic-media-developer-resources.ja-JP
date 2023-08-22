---
title: res
description: 解像度ベースの画像の拡大/縮小。 要求された解像度に画像を拡大・縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 1%

---

# res{#res}

解像度ベースの画像の拡大/縮小。 要求された解像度に画像を拡大・縮小します。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>ターゲットの解像度。通常、ピクセル/インチ（実数）で表します。 </p> </td> 
 </tr> 
</table>

スケール係数は、 *`val`* 作成者 `catalog::Resolution`. このコマンドは、返信画像の印刷解像度に影響を与えません。

この機能を使用するには、元のソース画像の解像度を認識し、 `catalog::Resolution`. アプリケーションによって、解像度の単位が異なる場合があります。 繰り返し可能な 2D テクスチャや、壁紙や布などのマテリアルスウォッチの場合、解像度はピクセル/インチまたはピクセル/mm で表すことができます。 空中写真やマップは、ピクセル/マイルまたはピクセル/km で提供される方が良い場合があります。 いずれの場合も、 `catalog::Resolution` は、 `res=`.

正確な解像度で画像を取得する以外に、 `res=` は、同じ解像度で複数の画像を組み合わせる場合にも使用できるので、これらの画像に表示される項目は互いに正確な比率で並べられます。

>[!NOTE]
>
>通常、合成画像はターゲットのビューサイズ ( `wid=`, `hei=`または `attribute::DefaultPix`) を返す前にクライアントに返します。 このサイズ変更を防ぎ、で指定した解像度の画像を取得するには `res=`を明示的に指定して、ビューの拡大/縮小を無効にする必要が生じる場合があります。 `scl=1`. これにより、サーバは、合成画像を拡大・縮小するのではなく、ターゲットのビューサイズに切り抜くように指示します。

## プロパティ {#section-fdbd16e59cff4952a3717146bc91412e}

ソース画像/マスクの属性。 ソース画像またはマスクに関連付けられていないレイヤーでは無視されます。 レイヤ 0 に適用される対象は次のとおりです。 `layer=comp`. 次のいずれかの場合は無視 `scale=` または `size=` は同じ画層に対して指定されます。

## 初期設定 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

指定しない場合、 `scale=` または `size=` は、拡大/縮小率を指定します。指定しない場合は、拡大/縮小せずに画像を使用します。

## 例 {#section-eb06f333e08e4247971fb1b18922597b}

12 ピクセル/インチのオブジェクト解像度でテクスチャイメージを取得し、Image Rendering または Image Authoring で使用します。 我々は、可能な限り最高の品質を得るために、損失のない PNG 形式とより高品質な再サンプリングを指定する。

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## 関連項目 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) , [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
