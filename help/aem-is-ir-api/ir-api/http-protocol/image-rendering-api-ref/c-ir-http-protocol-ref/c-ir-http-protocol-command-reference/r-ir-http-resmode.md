---
description: 再サンプリングモード wid=、hei=またはscl=で指定されたサイズにレンダリングイメージを拡大・縮小する際に使用する再サンプリング/補間アルゴリズムを選択します。
seo-description: 再サンプリングモード wid=、hei=またはscl=で指定されたサイズにレンダリングイメージを拡大・縮小する際に使用する再サンプリング/補間アルゴリズムを選択します。
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 7%

---


# resMode{#resmode}

再サンプリングモード wid=、hei=またはscl=で指定されたサイズにレンダリングイメージを拡大・縮小する際に使用する再サンプリング/補間アルゴリズムを選択します。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> ビリン  </span> </p> </td> 
   <td colname="col2"> <p>標準バイリニア補間を選択します。 最も高速な再サンプル法です。ただし、いくつかのエイリアシングアーチファクトが多少目に付きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> 二頭の  </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 バイリニア補間よりもCPU使用率が高くなりますが、エイリアシングアーチファクトが少ないシャープな画像が得られます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>修正ランチョス窓関数を補間アルゴリズムとして選択します。 バイキュービック法よりも多少シャープな結果になる場合があり、CPU使用率は高くなります。 </p> <p> <span class="codeph"> シャープ </span> は、 <span class="codeph"> sharp2に置き換えら </span>れました。これは、エイリアシングアーチファクト（Moiréとも呼ばれる）を引き起こす可能性が低いものです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ビシャープ  </span> </p> </td> 
   <td colname="col2"> <p><span class="keyword">Adobe Photoshop</span>で「バイキュービックシャーパー」と呼ばれる画像サイズを縮小するための<span class="keyword">Adobe Photoshop</span>のデフォルトリサンプラーを選択します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ea7029f37e094d9cb85646b85fbac0ce}

リクエスト内の任意の場所で発生する可能性があります。 最終的な画像の拡大/縮小が適用されない場合は無視されます。

## 初期設定 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 関連項目 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
