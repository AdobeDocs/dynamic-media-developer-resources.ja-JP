---
description: 再サンプリングモード 画像データの拡大・縮小に使用する再サンプリングおよび/または補間アルゴリズムを選択します。 また、テキストレイヤーの回転や、表示変換中の合成画像のサイズ変更にも適用されます。
seo-description: 再サンプリングモード 画像データの拡大・縮小に使用する再サンプリングおよび/または補間アルゴリズムを選択します。 また、テキストレイヤーの回転や、表示変換中の合成画像のサイズ変更にも適用されます。
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 12%

---


# resMode{#resmode}

再サンプリングモード 画像データの拡大・縮小に使用する再サンプリングおよび/または補間アルゴリズムを選択します。 また、テキストレイヤーの回転や、表示変換中の合成画像のサイズ変更にも適用されます。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビリン  </span> </p> </td> 
   <td colname="col2"> <p>標準バイリニア補間を選択します。 最も高速な再サンプル法です。ただし、いくつかのエイリアシングアーチファクトが多少目に付きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 二頭の  </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 バイリニア補間よりもCPU使用率が高くなりますが、エイリアシングアーチファクトが少ないシャープな画像が得られます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>修正ランチョス窓関数を補間アルゴリズムとして選択します。 バイキュービック法よりも多少シャープな結果になりますが、CPU 使用率はさらに高くなります。<span class="codeph"> シャープ </span> は、 <span class="codeph"> sharp2に置き換えら </span>れました。これは、エイリアシングアーチファクト(Moiré)を引き起こす可能性が低いからです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビシャープ  </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshopで「バイキュービックシャープ」と呼ばれる、画像サイズを小さくするためのPhotoshopの初期設定のリサンプラを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-a171bacf4ddf43c782e46b86a16d443e}

要求属性。 最終的な返信画像の作成に関連するすべての拡大・縮小操作（すべてのレイヤーの拡大・縮小を含む）に適用されます。

## 初期設定 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

画像カタログに保存されているレイヤー画像の最高品質のレンディションを取得します。 画像にはテキストが含まれる場合があります。 画像編集アプリケーションでさらに処理を行い、画像のアルファチャネルを要求します。

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 関連項目 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
