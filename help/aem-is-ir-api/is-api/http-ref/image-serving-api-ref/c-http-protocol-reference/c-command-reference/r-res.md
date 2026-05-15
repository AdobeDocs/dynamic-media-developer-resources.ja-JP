---
title: res
description: 解像度ベースの画像スケーリング： 要求された解像度に合わせて画像を拡大・縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e8ed7b00-7bb3-463e-9aaa-47f77bd4b45e
TQID: 'https://experienceleague.adobe.com/cvzfgWpPXIxwN0HaehiHOL8vAcfb369UJnC0tVuKFFI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# res{#res}

解像度ベースの画像スケーリング： 要求された解像度に合わせて画像を拡大・縮小します。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>ターゲット解像度。通常は、1 インチあたりのピクセル数（実数）です。 </p> </td> 
 </tr> 
</table>

スケール係数は、*`val`*&#x200B;を`catalog::Resolution`で割って計算します。 このコマンドは、返信画像の印刷解像度には影響しません。

この機能を使用するには、元のソース画像の解像度を把握し、`catalog::Resolution`で設定する必要があります。 アプリケーションによっては、解像度ユニットが異なる場合があります。 繰り返し可能な2D テクスチャや、壁紙や布地などの素材スウォッチの場合、解像度はピクセル/インチまたはピクセル/mmで表すことができます。 航空写真と地図は、ピクセル/マイルまたはピクセル/kmで提供する方が良い場合があります。 いずれの場合も、`catalog::Resolution`に使用される単位は、`res=`に使用される単位と同じである必要があります。

正確な解像度で画像を取得するだけでなく、`res=`を使用して、複数の画像を同じ解像度で結合して、これらの画像に表示される項目が正確に比例するようにすることもできます。

>[!NOTE]
>
>通常、合成画像は、クライアントに返される前に、ターゲット表示サイズ（`wid=`、`hei=`または`attribute::DefaultPix`で指定）にサイズ変更されます。 このサイズ変更を防ぎ、`res=`で指定された正確な解像度の画像を取得するには、`scl=1`を明示的に指定して表示の拡大・縮小を無効にする必要がある場合があります。 これにより、コンポジット画像を拡大・縮小するのではなく、ターゲットのビューサイズに合わせて切り抜くようにサーバーに指示します。

## プロパティ {#section-fdbd16e59cff4952a3717146bc91412e}

Source image/mask属性。 ソース画像またはマスクに関連付けられていないレイヤーによって無視されます。 適用されるレイヤー0は、`layer=comp`に指定されています。 `scale=`または`size=`が同じレイヤーに指定されている場合は無視されます。

## 初期設定 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

指定しない場合は、`scale=`または`size=`がスケール係数を決定します。指定しない場合は、画像がスケールなしで使用されます。

## 例 {#section-eb06f333e08e4247971fb1b18922597b}

画像レンダリングまたは画像オーサリングで使用するために、12 ピクセル/インチのオブジェクト解像度でテクスチャ画像を取得します。 損失のないPNG形式と、可能な限り最高の品質を実現するためのより優れた品質の再サンプリングを指定します。

` http:// *` サーバー`*/myTexture?res=12&fmt=png&resMode=sharp`

## 関連項目 {#section-1f8a8f11772e493ca803c4511f397a11}

[ カタログ：:Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)、[属性：:DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
