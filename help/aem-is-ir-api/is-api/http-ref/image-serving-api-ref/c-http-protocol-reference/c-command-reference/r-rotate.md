---
title: 循環
description: 画像を回転します。 画像、テキスト、またはべた塗りのカラーレイヤーを指定した角度だけ回転します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# 循環{#rotate}

画像を回転します。 画像、テキスト、またはべた塗りのカラーレイヤーを指定した角度だけ回転します。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>回転角度 ( 度単位（実数）。 </p></td> 
 </tr> 
</table>

正の角度は時計回りに回転します。 レイヤーのアンカーポイント ( `anchor=` または `catalog::Anchor`) は、回転の中心として機能します。 切り抜きを避けるために、必要に応じて、回転したデータの周りにレイヤー長方形を拡大して取り付けます。 レイヤーの背景領域を次のように塗りつぶした後に、回転が適用されます。 `color=`. `bgColor=` は、回転後の境界の長方形に背景色を追加する場合に使用します。

## プロパティ {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

[ 画層 ] コマンド 現在の画層に適用されます。 `layer=comp`. 効果画層で無視されます。

## 初期設定 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`（回転なし）。

## 例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

画像カタログ内の画像の左上隅近くに「販売中」ラベルを配置します。 ラベル画像は 300 x 300 ビュー用に既に正しいサイズに設定されており、左に 30 度回転する必要があります。 テキストボックスを白の半不透明色で塗りつぶし、ラベルを強調します。

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

申し込みを行います `size=` を 0 に設定し、 `wid=` および `hei=`. これにより、 `myImageId` 最終サイズを変えずにサイズを変更する `labelImage`. また、 `scl=1`を使用しない場合、合成画像は `attribute::DefaultPix` （0,0 に設定されていない限り）。 `color=` 回転前にテキストボックスに半不透明の背景色を追加します。

両方の画層の原点は、必要な位置揃えを行うために、左上のコーナーに設定されます。 レイヤ 1 の原点は、次の場所に適用されます。 `labelImage`回転後

詳しくは、 [例 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) 例：回転したテキスト。

## 関連項目 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
