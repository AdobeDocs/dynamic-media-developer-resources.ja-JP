---
description: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor  </span> </p> </td> 
   <td colname="col2"> <p> 使用するナビゲーションフレームの種類を指定します。 <span class="codeph">カーソル</span>に設定した場合、コンポーネントは固定サイズの参照カーソルを使用します。 デスクトップシステムとタッチデバイスには、異なるカーソルアートを持つことができます。これは、<span class="codeph"> .s7cursor </span> CSSクラスと<span class="codeph"> input=mouse|touch </span>属性セレクターを使用して制御します。 デスクトップシステムでは、アンカーポイントはカーソル領域の中央に設定され、タッチデバイスでは、アンカーはカーソルの下中央に配置されます。 <span class="codeph"> highlight </span>に設定すると、コンポーネントは可変サイズのナビゲーションフレームを使用します。フレームのサイズと形状は、ズーム率とフライアウト表示のサイズに応じて異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime  </span> </span> </p> </td> 
   <td colname="col2"> <p> ユーザーがアクティブにした後に、ハイライトまたはカーソルのフェードインにかかる時間（秒）を設定します。 フェードインはタッチデバイスにのみ適用されます。デスクトップシステムでは、コンポーネントでは無視されます。 </p> <p>フェードインが次のUI要素に適用されます。ハイライトフレーム、固定カーソル、オーバーレイ（<span class="codeph"> overlay </span>パラメーターが<span class="codeph"> 1 </span>に設定されている場合） フライアウト表示のアニメーションは、ハイライト/カーソルのフェードインアニメーションが完了した後にのみ開始します。 フェードアウトアニメーションはありません。 ユーザがフライアウトを無効にすると、対応するUI要素（カーソル、ハイライト、オーバーレイ）は即座に非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free  </span> </p> </td> 
   <td colname="col2"> <p> ナビゲーションフレームの位置を制御します。 </p> <p>image </span>の<span class="codeph">に設定した場合、ナビゲーションフレームはメイン表示内の実際の画像領域内にのみ配置できます。 </span></p> <p><span class="codeph"> free </span>に設定すると、ユーザは、論理的なメイン表示領域内の任意の場所（画像コンテンツの外部も含む）にナビゲーションフレームを移動できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
