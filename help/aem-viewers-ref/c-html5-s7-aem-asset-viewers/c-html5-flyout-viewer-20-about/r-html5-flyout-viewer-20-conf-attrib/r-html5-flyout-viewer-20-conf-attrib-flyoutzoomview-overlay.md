---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> フライアウトがアクティブな場合のメイン表示のハイライトの外観を制御します。 <span class="codeph"> 0</span>に設定した場合、フライアウトウィンドウに現在表示されている領域は、<span class="codeph"> .s7highlight</span>または<span class="codeph"> .s7cursor</span> CSSクラス名（<span class="codeph"> highlightmode</span>修飾子の値に応じて異なります）でハイライトされます。 <span class="codeph"> 1</span>コンポーネントを「逆」モードにする場合は、現在表示されている領域が完全に透明（<span class="codeph"> highlightmode</span>が<span class="codeph"> highlightmode</span>に設定されている場合）、または<span class="codeph"> .s7cursor</span> CSSクラス名（ケース<span class="codeph"> highlightmode</span>）です。は<span class="codeph"> cursor</span>に設定されますが、周囲の領域は<span class="codeph"> .s7overlay</span> CSSクラス名で提供されるスタイルを使用して塗りつぶされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
