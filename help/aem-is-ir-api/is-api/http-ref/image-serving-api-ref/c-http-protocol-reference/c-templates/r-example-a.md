---
description: 静的な背景画像を持つ固定サイズのテンプレートを作成します。可変画像は、背景の幅と高さの80%を超えないように、左中央の背景に合わせて拡大縮小されます。縦書きテキストがキャンバスの右端を中心に配置されます。
solution: Experience Manager
title: 例A
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# 例A{#example-a}

静的な背景画像を持つ固定サイズのテンプレートを作成します。可変画像は、背景の幅と高さの80%を超えないように、左中央の背景に合わせて拡大縮小されます。縦書きテキストがキャンバスの右端を中心に配置されます。

![](assets/examplea.png)

## テンプレートレコード {#section-32f54710593e438fa0622224c89380af}

オブジェクトの挿入

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+goes+here=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

すべてのレイヤーの`origin=`値は、レイヤーの位置と整列を厳密に制御するために、テンプレートで明示的に指定されます。 各画層の原点は、その画層の目的の位置合わせに合わせて設定されます。 背景（レイヤー0）の`origin=`は中央に設定されます。バックグラウンド画像は実行時に変更されないので、任意です。レイヤ0原点の任意の値を使用できます。

`pos=`値は、目的のレイヤーの位置決めを実現するために、レイヤーの原点間の必要なオフセットを提供します。

レイヤー1画像のアンカーは左中央に配置されます。`pos=`値と共に、レイヤー1画像の縦横比に関係なく、背景とレイヤー1画像の間の左中央揃えを実現します。

同様に、テキストレイヤーのアンカーは、自動サイズのテキストボックスの右中央に配置されます。 pos=と組み合わせると、フォントサイズや文字列の長さに関係なく、回転したテキストの中央揃えを希望します。

実際の表示テキストは実行時に提供されるので、変数を使用してテキストをrtf形式のエンベロープから分離します。 レイヤ1イメージには、デフォルトの変数`$object`を使用します。 これにより、このイメージをリクエストパスで指定できます。

背景画像とレイヤ1画像とには、任意の画像を用いてもよい。 背景画像にマスクがある場合、マスクされていない領域はデフォルトの背景色( `attribute::BkgColor` )で塗りつぶされます。 `fmt=png-alpha`または`fmt=tif-alpha`の場合は透明のままになります。 背景画像の縦横比が正方形でない場合は、返信画像の中央に配置され、余分なスペースは`attribute::BkgColor`で埋められます。 レイヤー1の画像にアルファデータまたはマスクが含まれている場合、背景画像（または背景色）は透明な領域に表示され続けます。 画像にマスクがない場合は、割り当てられた長方形全体が埋められます。

## テンプレートの使用 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

次の図は、レイヤー1の画像の縦横比が異なり、テキスト文字列が異なる複合結果を示しています。

![](assets/exampleausing.png)
