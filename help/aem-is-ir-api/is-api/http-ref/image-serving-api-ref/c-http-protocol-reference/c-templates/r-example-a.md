---
description: 静的な背景画像と、左中央の背景と整列し、背景の幅と高さの80%を超えないように拡大縮小された可変画像、およびカンバスの右端を中央に配置した垂直テキストの1つのテキストレイヤーを作成します。
seo-description: 静的な背景画像と、左中央の背景と整列し、背景の幅と高さの80%を超えないように拡大縮小された可変画像、およびカンバスの右端を中央に配置した垂直テキストの1つのテキストレイヤーを作成します。
seo-title: 例A
solution: Experience Manager
title: 例A
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---


# 例A{#example-a}

静的な背景画像と、左中央の背景と整列し、背景の幅と高さの80%を超えないように拡大縮小された可変画像、およびカンバスの右端を中央に配置した垂直テキストの1つのテキストレイヤーを作成します。

![](assets/examplea.png)

## テンプレートレコード{#section-32f54710593e438fa0622224c89380af}

オブジェクトの挿入

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+goes+here=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

すべてのレイヤーの`origin=`値は、テンプレートで明示的に指定され、レイヤーの位置と整列を厳密に制御します。 各レイヤー接触チャネルは、そのレイヤーの目的の位置に一致するように設定されます。 背景（レイヤー0）の`origin=`は中央に設定されます。これは、背景画像が実行時に変更されないので、任意の値です。レイヤー0接触チャネルの値は任意に使用できます。

`pos=`値は、望ましいレイヤーの位置を決めるために、レイヤーの接触チャネル点間の必要なオフセットを提供します。

レイヤー1画像のアンカーは左中央に配置されます。`pos=`値と組み合わせて、レイヤー1の画像の縦横比に関係なく、背景画像とレイヤー1の画像の左中央揃えが実行されます。

同様に、テキストレイヤーのアンカーは、自動サイズのテキストボックスの右中央に配置されます。 pos=と組み合わせると、フォントサイズや文字列の長さに関係なく、回転したテキストの目的の右中央揃えが実現します。

実際の表示テキストは実行時に提供されるので、変数を使用してrtf形式エンベロープからテキストを分離します。 レイヤー1のイメージにはデフォルトの変数`$object`を使用します。 これにより、このイメージを要求パスで指定できます。

背景画像とレイヤ1画像には、任意の画像を用いることができる。 背景画像にマスクが含まれている場合、マスクされていない領域は、初期設定の背景色(`attribute::BkgColor`)で塗りつぶされます。または、`fmt=png-alpha`または`fmt=tif-alpha`のときに透明のままになります。 背景画像の縦横比が正方形でない場合、画像は返信画像の中央に配置され、余分なスペースは`attribute::BkgColor`で埋められます。 レイヤー1の画像にアルファデータまたはマスクが含まれている場合、背景画像（または背景色）は透明領域に表示されたままになります。 画像にマスクがない場合は、割り当てられた長方形全体が埋められます。

## テンプレート{#section-3e04eedc268c482db5a8cfc662c0f327}の使用

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

次の図に、レイヤー1の画像の縦横比とテキスト文字列の違いを合成した結果を示します。

![](assets/exampleausing.png)

