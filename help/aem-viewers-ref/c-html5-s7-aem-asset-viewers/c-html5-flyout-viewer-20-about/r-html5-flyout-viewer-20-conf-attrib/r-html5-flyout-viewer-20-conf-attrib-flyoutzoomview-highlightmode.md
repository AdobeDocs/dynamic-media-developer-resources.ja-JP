---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor </span> </p> </td> 
   <td colname="col2"> <p> 使用するナビゲーションフレームの種類を指定します。 cursorに設定すると、 <span class="codeph"> コンポ </span>ーネントは固定サイズの参照カーソルを使用します。 デスクトップシステムとタッチデバイスでは、異なるカーソルアートを使用できます。これは、.s7cursor <span class="codeph"> CSSクラスと </span> input=mouse|touch属性セレクターを使用して制御 <span class="codeph"></span> します。 デスクトップシステムでは、アンカーポイントはカーソル領域の中央に設定され、タッチデバイスでは、アンカーはカーソルの下中央に配置されます。 highlightに設定すると、コ <span class="codeph"> ンポ </span>ーネントは可変サイズのナビゲーションフレームを使用します。フレームのサイズと形状は、ズーム率とフライアウトビューのサイズによって異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ショー </span> 時間 </span> </p> </td> 
   <td colname="col2"> <p> ユーザーがアクティブにした後に、ハイライトまたはカーソルがフェードインするまでの時間（秒）を設定します。 フェードインはタッチデバイスにのみ適用されます。デスクトップシステムでは、コンポーネントでは無視されます。 </p> <p>フェードインは、次のUI要素に適用されます。ハイライトフレーム、固定カーソル、オーバーレイ(オーバーレ <span class="codeph"> イパラ </span> メータが1に設定され <span class="codeph"> ている場 </span>合)。 フライアウトビューのアニメーションは、ハイライト/カーソルのフェードインアニメーションが完了した後にのみ開始されます。 フェードアウトアニメーションはありません。 ユーザがフライアウトを非アクティブにすると、対応するUI要素（カーソル、ハイライト、オーバーレイ）が即座に非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> ナビゲーションフレームの位置を制御します。 </p> <p>onimageに設定した場 <span class="codeph"> 合、ナ </span> ビゲーションフレームは、メインビュー内の実際の画像領域内にのみ配置できます。 </p> <p>freeを設定すると、ユ <span class="codeph"> ーザは </span> 画像コンテンツの外部にあっても、論理メインビュー領域の任意の場所にナビゲーションフレームを移動できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
