---
title: resMode
description: 再サンプリングモード。 レンダリングされた画像をwid=、hei=、またはscl=で指定されたサイズに拡大・縮小するために使用するリサンプリングや補間アルゴリズムを選択します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
TQID: 'https://experienceleague.adobe.com/VLg7JU1aiA7tRGG6vmoHciv-hDIZftbYtU4hAE5N0DY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 6%

---

# resMode{#resmode}

再サンプリングモード。 レンダリングされた画像を`wid=`、`hei=`または`scl=`で指定されたサイズに拡大/縮小するために使用するリサンプリングや補間アルゴリズムを選択します。

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> ビルリン </span> </p> </td> 
   <td colname="col2"> <p>標準バイリニア補間を選択します。 最も高速な再サンプル法です。ただし、いくつかのエイリアシングアーチファクトが多少目に付きます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>バイキュービック補間を選択します。 バイリニア補間よりもCPUを多く使用しますが、目立たないエイリアスアーティファクトを使用してよりシャープな画像を生成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> シャープ 2 </span> </p> </td> 
   <td colname="col2"> <p>変更されたLanczos ウィンドウ関数を補間アルゴリズムとして選択します。 CPUのコストが高いバイキュービックよりもわずかにシャープな結果を生成する可能性があります。 </p> <p> <span class="codeph">個のシャープ </span>が<span class="codeph">個のシャープ 2 </span>に置き換えられました。これは、エイリアシング アーティファクトを引き起こす可能性が低く、Moiréとも呼ばれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">司教</span> </p> </td> 
   <td colname="col2"> <p><span class="keyword"> Adobe Photoshop </span>のデフォルトリサンプラーを選択して、<span class="keyword"> Adobe Photoshop </span>で「バイキュービックシャーパー」と呼ばれる画像サイズを縮小します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ea7029f37e094d9cb85646b85fbac0ce}

リクエスト内のどこでも発生する可能性があります。 最終的な画像の拡大・縮小が適用されない場合は無視されます。

## 初期設定 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 関連項目 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[属性：:ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82)、[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)、[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)、[scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
