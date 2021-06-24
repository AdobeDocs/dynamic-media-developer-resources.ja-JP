---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic，ビューア，SDK/API，フライアウト
role: Developer,Business Practitioner
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> フライアウトがアクティブな場合の、メインビューのハイライトの外観を制御します。 <span class="codeph"> 0</span>に設定すると、フライアウトウィンドウに現在表示されている領域が、 <span class="codeph"> .s7highlight</span>または<span class="codeph"> .s7cursor</span> CSSクラス名（ <span class="codeph"> highlightmode</span>修飾子の値に応じて異なる）で指定されたスタイルを使用してハイライトされます。 <span class="codeph"> 1</span>コンポーネントを「逆」モードにする場合は、現在表示されている領域が完全に透明になる（<span class="codeph"> highlightmode</span>が<span class="codeph"> highlightmode</span>に設定される）か、<span class="codeph"> .s7cursor</span> CSSクラス名(ケース<span class="codeph"> highlightmode</span>が<span class="codeph"> cursor</span>に設定され、周囲の領域は<span class="codeph"> .s7overlay</span> CSSクラス名で提供されるスタイルを使用して塗りつぶされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
