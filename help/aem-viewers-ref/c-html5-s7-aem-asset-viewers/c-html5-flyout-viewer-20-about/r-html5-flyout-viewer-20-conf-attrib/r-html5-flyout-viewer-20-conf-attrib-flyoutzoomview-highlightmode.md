---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor </span> </p> </td> 
   <td colname="col2"> <p> 使用するナビゲーション フレームの種類を指定します。 カーソル </span> に設定 <span class="codeph"> ると、コンポーネントは固定サイズの参照カーソルを使用します。 デスクトップシステムとタッチデバイスでは、異なるカーソルアートを使用できます。 この機能は、CSS クラス <span class="codeph">input=mouse|touch </span> 属性セレクターを </span> 用し <span class="codeph">.s7cursor で制御されます。 デスクトップシステムでは、アンカーポイントはカーソル領域の中央に設定され、タッチデバイスでは、アンカーはカーソルの下中央に設定されます。 ハイライト </span> に設定 <span class="codeph"> ると、コンポーネントは可変サイズのナビゲーションフレームを使用します。フレームのサイズと形状は、ズーム率とフライアウトビューのサイズによって異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> ハイライトまたはカーソルがアクティブになってからフェードインするまでの時間（秒単位）を設定します。 フェードインは、タッチデバイスでのみ適用されます。デスクトップシステムでは、コンポーネントによって無視されます。 </p> <p>フェードインは、ハイライトフレーム、固定カーソル、オーバーレイ（オーバーレイ </span> パラメーターが <span class="codeph"> 1</span> に設定されてい <span class="codeph"> 場合）の UI 要素に適用されます。 フライアウト ビューのアニメーションは、ハイライト/カーソル フェード インのアニメーションが完了した後にのみ開始されます。 フェードアウト アニメーションはありません。 ユーザーがフライアウトをアクティベート解除すると、対応する UI 要素（カーソル、ハイライト、オーバーレイ）は直ちに非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|無料 </span> </p> </td> 
   <td colname="col2"> <p> ナビゲーションフレームの位置を制御します。 </p> <p><span class="codeph"> onimage </span> に設定した場合、ナビゲーションフレームはメインビュー内の実際の画像領域内にのみ配置できます。 </p> <p>自由に設定す <span class="codeph"> と </span> ユーザーは、画像コンテンツの外側を含め、論理メインビュー領域内の任意の場所にナビゲーションフレームを移動できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
