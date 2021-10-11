---
title: ControlBar.transition
description: ビデオ 360 ビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

ビデオ 360 ビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとその内容の表示/非表示を切り替える際に使用する効果の種類を指定します。 </p> <p><span class="codeph"> none</span> を使用すると、表示と非表示がすぐにできます。 徐々にフェードイン/フェードアウトするには、 <span class="codeph"> fade</span> を使用します。 </p> <p>fade は Internet Explorer 8 ではサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーが最後に登録したマウス/タッチイベントと、コントロールバーの非表示の間の時間を秒単位で指定します。 </p> <p> <span class="codeph"> -1</span> に設定した場合、コンポーネントは自動非表示の効果をトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>フェードインおよびフェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
