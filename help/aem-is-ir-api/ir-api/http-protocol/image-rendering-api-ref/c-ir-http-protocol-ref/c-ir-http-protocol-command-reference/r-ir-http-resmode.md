---
title: resMode
description: 再サンプリングモード。 wid=、hei=、scl=で指定されたサイズにレンダーしたイメージをスケーリングするために使用する再サンプリングおよび補間アルゴリズムを選択します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 7%

---

# resMode{#resmode}

再サンプリングモード。 レンダリング イメージを `wid=`、`hei=`、`scl=` で指定されたサイズにスケーリングするために使用する再サンプリングや補間アルゴリズムを選択します。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>標準の双線形補間を選択します。 最も高速な再サンプル法です。ただし、いくつかのエイリアシングアーチファクトが多少目に付きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 バイリニア補間よりも CPU に負荷がかかりますが、エイリアシングのアーティファクトが目立たない鮮明な画像が得られます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>修正されたランチョス ウィンドウ関数を補間アルゴリズムとして選択します。 CPU コストが高く、バイキュービック演算よりもわずかにシャープな結果が得られる場合があります。 </p> <p> シ <span class="codeph"> プな </span><span class="codeph"> は sharp2 </span> に置き換えられました。これにより、エイリアシングのアーティファクト（モアレとも呼ばれる）が発生する可能性が低くなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>画像サイズを縮小するための <span class="keyword"> Adobe Photoshop </span> デフォルトのリサンプラーを選択します。これは、Adobe Photoshop </span> では「バイキュービックシャーパー」と呼ば <span class="keyword"> ます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ea7029f37e094d9cb85646b85fbac0ce}

は、リクエスト内のどこでも発生する可能性があります。 最終的な画像の拡大/縮小が適用されない場合は無視されます。

## 初期設定 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 関連項目 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82)、[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
