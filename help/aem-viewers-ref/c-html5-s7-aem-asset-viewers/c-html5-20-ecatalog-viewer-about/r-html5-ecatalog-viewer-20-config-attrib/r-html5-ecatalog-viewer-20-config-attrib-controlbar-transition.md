---
title: ControlBar.transition
description: コントロールバーとその内容の表示/非表示を切り替える際に使用する効果の種類を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとその内容の表示/非表示を切り替える際に使用する効果の種類を指定します。 用途 <span class="codeph"> なし </span> 即座に表示と非表示を切り替えるのに <span class="codeph"> フェード </span> は、徐々にフェードインおよびフェードアウトする効果を提供します（Internet Explorer 8 ではサポートされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーが登録する最後のマウス/タッチイベントと、時間コントロールバーの非表示との間の時間を秒単位で指定します。 </p> <p> に設定した場合、 <span class="codeph"> -1 </span>を指定した場合、コンポーネントは自動非表示の効果をトリガーせず、常に画面に表示されたままになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p> フェードインおよびフェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。このコマンドは、タッチデバイスでは無視され、コントロールバーの自動非表示が無効になります。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
