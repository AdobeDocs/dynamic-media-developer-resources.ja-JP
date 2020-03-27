---
description: 固定サイズのテンプレートを作成し、背景の静的な画像と、背景の左中央に配置され、背景の幅と高さの80%を超えないように拡大・縮小された可変画像と、縦書きのテキストがカンバスの右端の中央に配置された1つのテキストレイヤーを作成します。
seo-description: 固定サイズのテンプレートを作成し、背景の静的な画像と、背景の左中央に配置され、背景の幅と高さの80%を超えないように拡大・縮小された可変画像と、縦書きのテキストがカンバスの右端の中央に配置された1つのテキストレイヤーを作成します。
seo-title: 例A
solution: Experience Manager
title: 例A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 例A{#example-a}

固定サイズのテンプレートを作成し、背景の静的な画像と、背景の左中央に配置され、背景の幅と高さの80%を超えないように拡大・縮小された可変画像と、縦書きのテキストがカンバスの右端の中央に配置された1つのテキストレイヤーを作成します。

![](assets/examplea.png)

## テンプレートレコード {#section-32f54710593e438fa0622224c89380af}

オブジェクトの挿入

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=layer+2+text goes+here&amp;he=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

すべての `origin=` レイヤーの値は、レイヤーの位置と位置揃えを厳密に制御するために、テンプレートで明示的に指定されます。 各レイヤーの原点は、そのレイヤーの目的の位置に合わせて設定されます。 背景 `origin=` （レイヤー0）の値が中央に設定され、これは、実行時に背景画像が変更されないので、任意の値です。レイヤー0の原点の値は任意に使用できます。

この値 `pos=` は、レイヤーの位置を決めるために、レイヤーの原点間の必要なオフセットを提供します。

レイヤー1画像のアンカーは左中央に配置されます。この値と組み合わ `pos=` せて、レイヤー1の画像の縦横比に関係なく、背景画像とレイヤー1の画像の間の左中央揃えが実行されます。

同様に、テキストレイヤーのアンカーは、自動サイズのテキストボックスの右中央に配置されます。 pos=と組み合わせると、フォントサイズや文字列の長さに関係なく、回転したテキストの右中央揃えを行うことができます。

実際の表示テキストは実行時に提供されるので、変数を使用してrtf形式のエンベロープからテキストを分離します。 レイヤ1イメージのデフォ `$object` ルトの変数を使用します。 これにより、このイメージを要求パスで指定できます。

背景画像とレイヤー1画像には、任意の画像を使用できます。 背景画像にマスクが含まれている場合、マスクされていない領域は初期設定の背景色( `attribute::BkgColor`)で塗りつぶされ、またはの場合は透明のまま `fmt=png-alpha` になりま `fmt=tif-alpha`す。 背景画像の縦横比が正方形でない場合、返信画像の中央に配置され、余分なスペースが埋められます `attribute::BkgColor`。 レイヤー1の画像にアルファデータまたはマスクが含まれている場合、背景画像（または背景色）は透明な領域に表示されたままになります。 画像にマスクがない場合は、割り当てられた長方形全体が埋められます。

## テンプレートの使用 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

次の図に、レイヤー1の画像の縦横比とテキスト文字列の違いを合成した結果を示します。

![](assets/exampleausing.png)

