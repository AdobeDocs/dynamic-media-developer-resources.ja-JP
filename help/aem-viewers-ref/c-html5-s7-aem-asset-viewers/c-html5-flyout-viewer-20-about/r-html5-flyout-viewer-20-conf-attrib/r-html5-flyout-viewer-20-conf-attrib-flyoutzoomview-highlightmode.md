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
   <td colname="col2"> <p> 使用するナビゲーションフレームの種類を指定します。 に設定する場合 <span class="codeph"> カーソル </span>の場合、コンポーネントは固定サイズの参照カーソルを使用します。 デスクトップシステムとタッチデバイスで異なるカーソルアートを使用できます。 この機能は次の条件で制御されます。 <span class="codeph"> .s7cursor </span> CSS クラスと <span class="codeph"> input=mouse|touch </span> 属性セレクターを使用します。 デスクトップシステムでは、アンカーポイントはカーソル領域の中央に設定され、タッチデバイスでは、アンカーはカーソルの下中央に設定されます。 に設定する場合 <span class="codeph"> highlight </span>を使用する場合、コンポーネントは可変サイズのナビゲーションフレームを使用します。フレームのサイズと形状は、ズーム率とフライアウトビューのサイズに応じて異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> ユーザーがアクティブにした後に、ハイライトまたはカーソルがフェードインする時間（秒）を設定します。 フェードインはタッチデバイスでのみ適用され、デスクトップシステムではコンポーネントで無視されます。 </p> <p>フェードインは、ハイライトフレーム、固定カーソル、オーバーレイ（場合に応じて）の UI 要素に適用されます。 <span class="codeph"> オーバーレイ </span> パラメーターがに設定されている <span class="codeph"> 1 </span>) をクリックします。 フライアウトビューのアニメーションは、ハイライト/カーソルのフェードインアニメーションが完了した後にのみ開始されます。 フェードアウトアニメーションはありません。 ユーザがフライアウトを非アクティブにすると、対応する UI 要素（カーソル、ハイライト、オーバーレイ）がすぐに非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> ナビゲーションフレームの位置を制御します。 </p> <p>に設定した場合、 <span class="codeph"> onimage </span>を指定しない場合、ナビゲーションフレームは、メインビュー内の実際の画像領域の内側にのみ配置できます。 </p> <p>に設定した場合、 <span class="codeph"> 無料 </span> ユーザは、画像コンテンツの外側でも、論理的なメインビュー領域の任意の場所にナビゲーションフレームを移動できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
