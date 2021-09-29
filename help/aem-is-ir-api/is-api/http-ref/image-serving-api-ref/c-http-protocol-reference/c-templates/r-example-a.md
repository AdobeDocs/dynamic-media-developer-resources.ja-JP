---
title: 例 A
description: 静的な背景画像を持つ固定サイズのテンプレートを作成します。可変画像は、左中央に背景と整列し、背景の幅と高さの 80%を超えないように拡大縮小されます。 最後に、縦書きのテキストがキャンバスの右端の中央に配置された 1 つのテキストレイヤーを作成します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 例 A{#example-a}

静的な背景画像を持つ固定サイズのテンプレートを作成します。可変画像は、左中央に背景と整列し、背景の幅と高さの 80%を超えないように拡大縮小されます。 最後に、縦書きのテキストがキャンバスの右端の中央に配置された 1 つのテキストレイヤーを作成します。

![画像の例](assets/examplea.png)

## テンプレートレコード {#section-32f54710593e438fa0622224c89380af}

オブジェクトの挿入

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text goes+here=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

すべての画層の `origin=` 値は、画層の位置と整列を厳密に制御するために、テンプレートで明示的に指定されます。 各画層の原点は、その画層の希望の位置合わせに合わせて設定されます。 背景（レイヤー 0）の `origin=` は中心に設定されます。この値は、実行時に背景画像が変更されないので、任意です。レイヤ 0 の原点の値はどれでも使用できます。

`pos=` の値は、必要なレイヤの位置決めを行うために、レイヤの原点間の必要なオフセットを提供します。

レイヤー 1 画像のアンカーは、`pos=` 値を使用して左中央に配置されます。 この設定は、レイヤー 1 画像の縦横比に関係なく、背景画像とレイヤー 1 画像の間の左中央揃えを実現します。

同様に、テキストレイヤーのアンカーは、自動サイズのテキストボックスの右中央に `pos=` 値で配置されます。 この設定は、フォントサイズや文字列の長さに関係なく、回転したテキストの中央揃えを目的とします。

実際の表示テキストは実行時に提供されるので、変数を使用してテキストを rtf 形式のエンベロープから分離します。 デフォルトの変数 `$object` がレイヤ 1 イメージに使用されます。 この変数を使用すると、リクエストパスでこの画像を指定できます。

背景画像とレイヤ 1 画像には、任意の画像を用いてもよい。 背景画像にマスクがある場合、マスクされていない領域はデフォルトの背景色 ( `attribute::BkgColor` ) で塗りつぶされます。 `fmt=png-alpha` または `fmt=tif-alpha` の場合は、透明のままになります。 背景画像の縦横比が正方形でない場合は、返信画像の中央に配置され、余分なスペースは `attribute::BkgColor` で埋められます。 レイヤー 1 の画像にアルファデータまたはマスクが含まれている場合、背景画像（または背景色）は透明領域に表示されたままになります。 画像にマスクがない場合は、割り当てられた長方形全体が埋められます。

## テンプレートの使用 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

次の図は、レイヤ 1 の画像の縦横比が異なり、テキスト文字列が異なる複合結果を示しています。

![例：合成結果画像](assets/exampleausing.png)
