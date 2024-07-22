---
title: 循環
description: 画像を回転 画像、テキスト、または単色のレイヤーを指定した角度だけ回転させます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---

# 循環{#rotate}

画像を回転 画像、テキスト、または単色のレイヤーを指定した角度だけ回転させます。

`rotate= *` 角度 `*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角 </span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p></td> 
 </tr> 
</table>

正の角度は時計回りに回転します。 レイヤーのアンカーポイント（`anchor=` または `catalog::Anchor`）は、回転の中心として機能します。 レイヤーの長方形は、切り抜きを避けるために、必要に応じて回転されたデータの周囲に拡大および調整されます。 回転は、レイヤーの背景領域を `color=` で埋めた後に適用されます。 モディファイヤ `bgColor=` を使用すると、回転後のバウンディング矩形に背景色を追加できます。

## プロパティ {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

[ 画層 ] コマンド： 現在の画層、または `layer=comp` の場合は画層 0 に適用されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0` （回転なし）。

## 例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

画像カタログの画像の左上隅に「販売中」ラベルを配置します。 ラベル画像は 300 x 300 ビューに対して既に正しいサイズに設定されており、左に 30 度回転する必要があります。 ラベルを強調するには、テキスト ボックスを白の半不透明の色で塗りつぶします。

`http:// *` サーバー `*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

ビューのサイズを設定するには、`wid=` と `hei=` を使用するのではなく、`size=` をレイヤ 0 に適用します。 この方法を使用すると、`labelImage` の最終的なサイズを変更せずに `myImageId` のサイズを変更できます。 また、`scl=1` を指定します。指定しない場合は、合成イメージのサイズが `attribute::DefaultPix` に変更されます（0,0 に設定されている場合を除く）。 修飾子 `color=` は、回転前にテキストボックスに半不透明の背景色を追加します。

両方のレイヤーの原点は、目的の配置を達成するために左上隅に設定されます。 レイヤ 1 の原点は `labelImage` 回転した後に適用されます。

回転したテキストの例については、[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の [ 例 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) を参照してください。

## 関連項目 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
