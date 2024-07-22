---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> フライアウトがアクティブなときのメイン ビューのハイライトの外観をコントロールします。 <span class="codeph"> 0</span> に設定した場合、フライアウトウィンドウに現在表示されている領域は、<span class="codeph"> .s7highlight</span> または <span class="codeph"> .s7cursor</span> CSS クラス名（highlightmode</span> 修飾子の値によって異なる）によって提供されるスタイルを使用し <span class="codeph"> ハイライト表示されます。 <span class="codeph">1 に設定すると </span> コンポーネントは「逆」モードに入ります。ここでは、現在表示されている領域が完全に透明な場合（<span class="codeph"> highlightmode</span> が <span class="codeph"> highhighlight</span> に設定されている場合）または <span class="codeph"> .s7cursor</span> CSS クラス名（<span class="codeph"> highlightmode</span> が <span class="codeph"> cursor</span> に設定されている場合）でスタイル設定されていますが、周囲の領域は.s7overlay</span> CSS クラス名 <span class="codeph"> 指定されているスタイルで塗りつぶされています。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

オプション。

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
