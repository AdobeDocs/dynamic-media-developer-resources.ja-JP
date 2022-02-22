---
title: resMode
description: 再サンプリングモード。 レンダリング画像を wid=、hei=または scl=で指定されたサイズに拡大縮小するために使用する再サンプリングや補間アルゴリズムを選択します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 8%

---

# resMode{#resmode}

再サンプリングモード。 レンダリングイメージをで指定したサイズに拡大縮小する際に使用する再サンプリングおよび補間アルゴリズムを選択します。 `wid=`, `hei=`または `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> ビリン </span> </p> </td> 
   <td colname="col2"> <p>標準の双線形補間を選択します。 最も高速な再サンプル法です。ただし、いくつかのエイリアシングアーチファクトが多少目に付きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 2 線形補間よりも CPU 使用率が高くなりますが、目に見えるエイリアスアーティファクトが減少した、よりシャープな画像が得られます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>補間アルゴリズムとして、変更された Lanczos Window 関数を選択します。 CPU コストが高い場合、バイキュービック法よりも少しシャープな結果が得られる場合があります。 </p> <p> <span class="codeph"> 鋭い </span> は、 <span class="codeph"> sharp2 </span>：エイリアシングアーティファクト（Moiré とも呼ばれる）が発生する可能性が低くなります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 二尖鋭の </span> </p> </td> 
   <td colname="col2"> <p>を選択します。 <span class="keyword"> Adobe Photoshop </span> 画像サイズを縮小するためのデフォルトの再サンプリング ( <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ea7029f37e094d9cb85646b85fbac0ce}

リクエスト内の任意の場所で発生する場合があります。 最終的な画像の拡大/縮小が適用されていない場合は無視されます。

## 初期設定 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 関連項目 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
