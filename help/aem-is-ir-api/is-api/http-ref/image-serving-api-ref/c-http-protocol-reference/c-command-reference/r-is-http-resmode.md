---
title: resMode
description: 再サンプリングモード。 画像データのスケーリングに使用するリサンプリングや補間アルゴリズムを選択します。 表示の変換中にテキストレイヤーを回転し、合成画像のサイズを変更する場合にも適用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
TQID: 'https://experienceleague.adobe.com/uT9SBMqQ0JvU-S8BF2y0kY6C--jNhvggbRwhTpTJOGg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 1%

---

# resMode{#resmode}

再サンプリングモード。 画像データのスケーリングに使用するリサンプリングや補間アルゴリズムを選択します。 表示の変換中にテキストレイヤーを回転し、合成画像のサイズを変更する場合にも適用されます。

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビルリン </span> </p> </td> 
   <td colname="col2"> <p>標準の双線補間を選択します。 最速の再サンプリング方法。一部のエイリアスアーティファクトが目立ちます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>二立方補間を選択します。 CPUは双線形インターポレーションよりも強力ですが、目立たないエイリアシングのアーティファクトを使用してよりシャープな画像を生成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> シャープ 2 </span> </p> </td> 
   <td colname="col2"> <p>変更されたLanczos ウィンドウ関数を補間アルゴリズムとして選択します。 CPUのコストが高い二立方ベクトルよりも若干鋭い結果を生成できます。 <span class="codeph">個のシャープ </span>が<span class="codeph">個のシャープ 2 </span>に置き換えられました。これは、エイリアスアーティファクト（Moiré）を引き起こす可能性が低くなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">司教</span> </p> </td> 
   <td colname="col2"> <p>Adobe Photoshopで「バイキュービックシャーパー」と呼ばれる画像サイズを小さくするために、Photoshopのデフォルトのリサンプラーを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>`resMode=bisharp`と`fit=stretch`の両方を使用する場合に画像の縦横比を維持するには、幅パラメーターまたは高さパラメーターのいずれかを使用することをお勧めします。 両方のパラメーターを定義する必要がある場合は、次の例に示すように、それらを別のレイヤーでラップできます。
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## プロパティ {#section-a171bacf4ddf43c782e46b86a16d443e}

リクエスト属性： すべてのレイヤーの拡大/縮小を含め、最終的な返信画像の作成に関わるすべての拡大縮小の操作に適用されます。

## 初期設定 {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## 例 {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

画像カタログに保存されているレイヤー画像の最高画質のレンディションを取得します。 画像にはテキストを含めることができます。 画像はさらに画像編集アプリケーションで処理され、画像とともにアルファチャネルを要求する。

` http:// *` サーバー`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## 関連項目 {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
