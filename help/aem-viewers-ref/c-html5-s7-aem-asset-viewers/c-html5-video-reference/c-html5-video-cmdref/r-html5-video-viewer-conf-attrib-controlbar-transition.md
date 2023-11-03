---
title: ControlBar.transition
description: ビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

ビデオビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとその内容の表示/非表示を切り替える際に使用する効果の種類を指定します。 </p> <p>用途 <span class="codeph"> なし</span> すぐに表示/非表示にできます。 用途 <span class="codeph"> フェード</span> 徐々にフェードイン/フェードアウトする効果を提供する。 </p> <p>Internet Explorer 8 では、fade はサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーが登録する最後のマウス/タッチイベントと、コントロールバーが非表示になる時間との間の時間を秒単位で指定します。 </p> <p> に設定した場合、 <span class="codeph"> -1</span>を指定した場合、コンポーネントは自動非表示の効果をトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>フェードインおよびフェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
