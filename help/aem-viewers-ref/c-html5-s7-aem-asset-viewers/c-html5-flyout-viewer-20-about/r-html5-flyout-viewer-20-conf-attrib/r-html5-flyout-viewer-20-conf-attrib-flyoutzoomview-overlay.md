---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
TQID: 'https://experienceleague.adobe.com/MxdOr4hM38H7Hy6uCIvrOJQ0xjxbiyaJlIwaIFKGZOU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> フライアウトがアクティブな場合のメインビューのハイライト表示の外観を制御します。 <span class="codeph"> 0</span>に設定すると、フライアウトウィンドウに現在表示されている領域は、<span class="codeph"> .s7highlight</span>または<span class="codeph"> .s7cursor</span> CSS クラス名で提供されているスタイルを使用して強調表示されます（<span class="codeph"> highlightmode</span>修飾子の値によって異なります）。 <span class="codeph"> 1</span>に設定すると、コンポーネントは「反転」モードに入り、現在表示されている領域は完全に透明になります（例：<span class="codeph"> highlightmode</span>が<span class="codeph"> highlight</span>に設定されている場合）。または<span class="codeph"> .s7cursor</span> CSS クラス名でスタイル設定されます（例：<span class="codeph"> highlightmode</span>が<span class="codeph"> cursor</span>に設定されている場合）。ただし、周囲の領域は<span class="codeph"> .s7overlay</span> CSS クラスで指定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
