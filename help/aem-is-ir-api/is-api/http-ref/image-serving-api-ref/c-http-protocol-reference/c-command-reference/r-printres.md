---
title: printRes
description: 印刷解像度。 応答画像に埋め込まれた印刷解像度の値を上書きします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
TQID: 'https://experienceleague.adobe.com/QJMoF8XW-O1W-E12Cpix3uiwiqKOFo6A4bI6I0hv0II'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# printRes{#printres}

印刷解像度。 応答画像に埋め込まれた印刷解像度の値を上書きします。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>印刷解像度（dpi）: </p></td> 
 </tr> 
</table>

印刷解像度は、通常、カタログ エントリの場合は`catalog::PrintResolution`によって定義されます。そうでない場合は、ソース画像に埋め込まれた印刷解像度の値によって定義されます。 テンプレートまたはレイヤー化された合成画像がある場合、応答ファイルに埋め込まれたデフォルトの印刷解像度は、レイヤー番号が最も小さいレイヤー画像の印刷解像度です。

印刷解像度を設定しても、返信画像のピクセルサイズは変更されません。

## プロパティ {#section-03c7910ebe234804a319e5d0d8ef3a74}

リクエスト属性： 現在のレイヤー設定に関係なく適用されます。

## 初期設定 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
ソースイメージに埋め込まれたプリント解像度でも可能です。

## 関連項目 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
