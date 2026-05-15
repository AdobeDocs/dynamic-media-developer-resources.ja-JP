---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
TQID: 'https://experienceleague.adobe.com/x43ipzx6iKOODZ10S8o8yJA9pg0Gl8mldfS5fEiVQJ4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ハイライト|カーソル </span> </p> </td> 
   <td colname="col2"> <p> 使用するナビゲーションフレームのタイプを指定します。 <span class="codeph"> カーソル </span>に設定すると、コンポーネントは固定サイズの参照カーソルを使用します。 デスクトップシステムとタッチデバイスに対して、異なるカーソルアートを使用することができます。 この機能は、<span class="codeph"> .s7cursor </span> CSS クラスと<span class="codeph"> input=mouse|touch </span>属性セレクターで制御されます。 デスクトップシステムでは、アンカーポイントはカーソル領域の中央に設定され、タッチデバイスではアンカーはカーソルの下部中央に設定されます。 <span class="codeph"> ハイライト </span>に設定すると、コンポーネントは可変サイズのナビゲーションフレームを使用します。フレームのサイズと形状は、ズーム率とフライアウトビューのサイズによって異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ショータイム </span> </span> </p> </td> 
   <td colname="col2"> <p> ユーザーがアクティブ化した後、ハイライトまたはカーソルがフェードインするまでの時間（秒単位）を設定します。 フェードインはタッチデバイスにのみ適用され、デスクトップシステムではコンポーネントによって無視されます。 </p> <p>フェードインは、次のUI要素に適用されます。ハイライト枠、固定カーソル、オーバーレイ（<span class="codeph"> オーバーレイ </span> パラメーターが<span class="codeph"> 1 </span>に設定されている場合）。 フライアウトビューアニメーションは、アニメーションのハイライト/カーソルのフェードが完了した後にのみ開始されます。 フェードアウトアニメーションはありません。 ユーザーがフライアウトを無効にすると、対応するUI要素（カーソル、ハイライト、オーバーレイ）が瞬時に非表示になります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|無料</span> </p> </td> 
   <td colname="col2"> <p> ナビゲーションフレームの位置を制御します。 </p> <p>画像</span>で<span class="codeph">に設定した場合、ナビゲーションフレームは、メインビュー内の実際の画像領域内にのみ配置できます。 </p> <p><span class="codeph">が空いている</span>に設定されている場合、ユーザーは、画像コンテンツの外部であっても、論理メインビュー領域内の任意の場所でナビゲーションフレームを移動できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
