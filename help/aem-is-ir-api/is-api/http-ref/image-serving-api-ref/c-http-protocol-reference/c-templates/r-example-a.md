---
title: 例 A
description: 静的な背景画像、つまり左中央の背景に揃えられ、背景の幅と高さの 80% を超えないように拡大縮小される変数画像を使用して、固定サイズのテンプレートを作成します。 最後に、キャンバスの右端を中心に垂直テキストを配置した 1 つのテキストレイヤーです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 例 A{#example-a}

静的な背景画像、つまり左中央の背景に揃えられ、背景の幅と高さの 80% を超えないように拡大縮小される変数画像を使用して、固定サイズのテンプレートを作成します。 最後に、キャンバスの右端を中心に垂直テキストを配置した 1 つのテキストレイヤーです。

![ 画像の例 ](assets/examplea.png)

## テンプレートレコード {#section-32f54710593e438fa0622224c89380af}

オブジェクトの挿入

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+goes+here&amp;text=rtf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.0,</span> </p> </td> 
 </tr> 
</table>

すべてのレイヤーの `origin=` 値は、レイヤーの配置と整列を厳密に制御するために、テンプレートで明示的に指定されます。 各レイヤの原点は、そのレイヤの目的の位置合わせに一致するように設定されます。 背景の `origin=` （レイヤー 0）は中央に設定されます。この値は、実行時に背景画像が変化しないので、任意です。レイヤー 0 の原点の値を使用できます。

`pos=` の値は、レイヤの原点ポイント間に必要なオフセットを提供し、目的のレイヤ位置を実現します。

レイヤー 1 画像のアンカーは左中央に配置され、`pos=` の値が設定されます。 この設定により、レイヤー 1 画像の縦横比に関係なく、背景とレイヤー 1 画像の左中央揃えが実現します。

同様に、テキストレイヤーのアンカーは、自動サイズ調整されたテキストボックスの右中央に、`pos=` の値で配置されます。 この設定により、フォントサイズや文字列の長さに関係なく、回転したテキストに対して目的の右中央揃えが実現します。

実際の表示テキストは実行時に提供されるため、変数を使用してテキストを rtf 書式設定エンベロープから分離します。 レイヤ 1 のイメージには、既定の変数 `$object` が使用されます。 この変数を使用すると、リクエストパスでこの画像を指定できます。

背景画像およびレイヤー 1 画像には、任意の画像を使用できます。 背景画像にマスクがある場合、マスクされていない領域はデフォルトの背景色（`attribute::BkgColor`）で塗りつぶされるか、`fmt=png-alpha` または `fmt=tif-alpha` の場合は透明のままになります。 背景画像の縦横比が四角形でない場合は、返信画像の中央に配置され、余分なスペースが `attribute::BkgColor` で埋められます。 レイヤー 1 の画像にアルファデータまたはマスクが含まれている場合、背景画像（または背景色）は透明領域に表示されたままになります。 画像にマスクがない場合は、割り当てられた長方形全体が塗りつぶされます。

## テンプレートの使用 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *` サーバー `*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

次の画像は、レイヤー 1 画像と異なるテキスト文字列の異なる縦横比を合成した結果を示しています。

![ 例：複合結果の画像 ](assets/exampleausing.png)
