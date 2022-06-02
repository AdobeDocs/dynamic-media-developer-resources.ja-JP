---
title: resMode
description: 再サンプリングモード。 画像データの拡大/縮小に使用する再サンプリングや補間アルゴリズムを選択します。 また、ビュー変換時のテキストレイヤーの回転や合成画像のサイズ変更にも適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 3%

---

# resMode{#resmode}

再サンプリングモード。 画像データの拡大/縮小に使用する再サンプリングや補間アルゴリズムを選択します。 また、ビュー変換時のテキストレイヤーの回転や合成画像のサイズ変更にも適用されます。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビリン </span> </p> </td> 
   <td colname="col2"> <p>標準のバイリニア補間を選択します。 最速の再サンプリング方法目に見えるエイリアスアーティファクトが一部発生します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 バイリニア補間よりも CPU 使用率が高くなりますが、目に見えるエイリアスアーティファクトが減少した、よりシャープな画像が得られます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>補間アルゴリズムとして、変更された Lanczos Window 関数を選択します。 バイキュービック法よりも少しシャープな結果が得られ、CPU コストがかかります。 <span class="codeph"> 鋭い </span> は、 <span class="codeph"> sharp2 </span>：エイリアシングアーティファクト (Moiré) が発生する可能性が低くなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 二尖鋭の </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshopで「バイキュービックシャーパー」と呼ばれる、画像サイズを縮小するためのPhotoshopのデフォルトの再サンプリング方法を選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>画像の縦横比を維持するには、 `resMode=bisharp` および `fit=stretch`を使用する場合は、「幅」パラメーターまたは「高さ」パラメーターを使用することをお勧めします。 両方のパラメータを定義する必要がある場合は、次の例に示すように、別のレイヤでラップできます。
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## プロパティ {#section-a171bacf4ddf43c782e46b86a16d443e}

要求属性。 最終的な返信画像の作成に関連するすべての拡大/縮小操作に適用されます。これには、すべてのレイヤーの拡大/縮小も含まれます。

## 初期設定 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

画像カタログに保存されているレイヤー画像の最高品質のレンディションを取得します。 画像にはテキストを含めることができます。 画像は、画像編集アプリケーションでさらに処理され、画像を使用してアルファチャンネルを要求する。

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 関連項目 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
