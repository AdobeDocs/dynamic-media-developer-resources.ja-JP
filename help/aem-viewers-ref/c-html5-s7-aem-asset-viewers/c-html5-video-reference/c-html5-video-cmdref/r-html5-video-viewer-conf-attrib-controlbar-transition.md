---
title: ControlBar.transition
description: ビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

ビデオビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード </span> </p> </td> 
   <td colname="col2"> <p> コントロール バーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 </p> <p><span class="codeph"> none</span> を使用すると、表示と非表示を即座に切り替えることができます。 フェード <span class="codeph"> 使用して </span> 徐々にフェードインおよびフェードアウト効果を与えます。 </p> <p>Internet Explorer 8 では、フェードはサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>コントロール バーが登録する最後のマウスまたはタッチ イベントからコントロール バーが非表示になるまでの時間を秒単位で指定します。 </p> <p> <span class="codeph">-1</span> に設定すると、コンポーネントは自動的に非表示になる効果をトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>フェードインおよびフェードアウト アニメーションのデュレーションを秒単位で設定します。 </p> </td> 
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
