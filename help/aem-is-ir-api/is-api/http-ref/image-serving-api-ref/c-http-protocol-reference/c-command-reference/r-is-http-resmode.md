---
title: resMode
description: 再サンプリングモード。 画像データの拡大縮小に使用する再サンプリングまたは補間アルゴリズムを選択します。 ビュー変換中のテキストレイヤーの回転および合成画像のサイズ変更にも適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# resMode{#resmode}

再サンプリングモード。 画像データの拡大縮小に使用する再サンプリングまたは補間アルゴリズムを選択します。 ビュー変換中のテキストレイヤーの回転および合成画像のサイズ変更にも適用されます。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>標準の双線形補間を選択します。 最も速い再サンプリング方法。いくつかのエイリアシング アーティファクトが目立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>双三次補間を選択します。 バイリニア補間よりもCPUを多用しますが、エイリアシングのアーティファクトが目立たない鮮明なイメージが生成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>修正されたランチョス ウィンドウ関数を補間アルゴリズムとして選択します。 CPUのコストが高く、2 立方バイトよりもわずかにシャープな結果を得ることができます。 シ <span class="codeph"> プな </span> は sharp2 <span class="codeph"> に置き換えられました。これにより、エイリアシング </span> アーティファクト（モアレ）が発生する可能性が低くなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>画像サイズを縮小するためのPhotoshopのデフォルトのリサンプラーを選択します。これは、Adobe Photoshopでは「バイキュービックシャーパー」と呼ばれます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>`resMode=bisharp` と `fit=stretch` の両方を使用する場合に画像の縦横比を維持するには、width パラメーターまたは height パラメーターを使用することをお勧めします。 両方のパラメーターを定義する必要がある場合は、次の例に示すように、それらを別のレイヤーに含めることができます。
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## プロパティ {#section-a171bacf4ddf43c782e46b86a16d443e}

リクエスト属性。 最終的な返信画像の作成に関連するすべての拡大縮小操作（すべてのレイヤーの拡大縮小を含む）に適用されます。

## 初期設定 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

画像カタログに保存された、レイヤー化された画像の最高品質のレンディションを取得します。 画像にはテキストを含めることができます。 画像は、画像編集アプリケーションでさらに処理され、これにより、画像とともにアルファチャネルが要求される。

` http:// *` サーバー `*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 関連項目 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[属性：:ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
