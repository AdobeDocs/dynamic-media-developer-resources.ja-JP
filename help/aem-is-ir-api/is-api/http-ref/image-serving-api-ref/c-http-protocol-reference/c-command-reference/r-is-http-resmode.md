---
description: 再サンプリングモード 画像データの拡大・縮小に使用する再サンプリングおよび/または補間アルゴリズムを選択します。 また、テキストレイヤーの回転や、表示変換中の合成画像のサイズ変更にも適用されます。
solution: Experience Manager
title: resMode
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
translation-type: tm+mt
source-git-commit: b08d1f5b0aa512be4a6e6a4d45d8d4dec15ca1db
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---

# resMode{#resmode}

再サンプリングモード 画像データの拡大・縮小に使用する再サンプリングおよび/または補間アルゴリズムを選択します。 また、テキストレイヤーの回転や、表示変換中の合成画像のサイズ変更にも適用されます。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビリン  </span> </p> </td> 
   <td colname="col2"> <p>標準バイリニア補間を選択します。 最も高速な再サンプリング方法一部のエイリアシングアーチファクトが目立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 二頭の  </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 バイリニア補間よりもCPU使用率が高くなりますが、エイリアシングアーチファクトが少ないシャープな画像になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>修正ランチョス窓関数を補間アルゴリズムとして選択します。 バイキュービック法よりも多少シャープな結果が得られ、CPU使用率は高くなります。 <span class="codeph"> シャープ </span> は、 <span class="codeph"> sharp2に置き換えら </span>れました。これは、エイリアシングアーチファクト(Moiré)を引き起こす可能性が低いからです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビシャープ  </span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshopで「バイキュービックシャープ」と呼ばれる、画像サイズを小さくするためのPhotoshopの初期設定のリサンプラを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>`resMode=bisharp`と`fit=stretch`の両方を使用する場合に画像の縦横比を維持するには、widthパラメーターまたはheightパラメーターのいずれかを使用することをお勧めします。 両方のパラメータを定義する必要がある場合は、次の例に示すように、別のレイヤーにラップできます。
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## プロパティ {#section-a171bacf4ddf43c782e46b86a16d443e}

要求属性。 最終的な返信画像の作成に関連するすべての拡大・縮小操作（すべてのレイヤーの拡大・縮小を含む）に適用されます。

## 初期設定 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

画像カタログに保存されているレイヤー画像の最高品質のレンディションを取得します。 画像にはテキストを含めることができます。 画像は、画像編集アプリケーションでさらに処理されるので、画像のアルファチャネルを要求する。

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 関連項目 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
