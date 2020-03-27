---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 30f133bd-09c7-4d70-bcc4-d961bb028e55
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration`*[, *``*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 すぐに表 <span class="codeph"> 示/非表 </span> 示を切り替える場合は、noneを使用します。fadeを使用す <span class="codeph"></span> ると、徐々にフェードイン/フェードアウトする効果が得られます（Internet Explorer 8ではサポートされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーが最後に登録し、コントロールバーが非表示になるマウス/タッチイベントの間隔を秒単位で指定します。 </p> <p> -1に設定すると、コン <span class="codeph"> ポーネ </span> ントは自動非表示の効果をトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 期 </span> 間 </span> </p> </td> 
   <td colname="col2"> <p> フェードインおよびフェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）タッチデバイスでは、コントロールバーの自動非表示が無効な場合、このコマンドは無視されます。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
