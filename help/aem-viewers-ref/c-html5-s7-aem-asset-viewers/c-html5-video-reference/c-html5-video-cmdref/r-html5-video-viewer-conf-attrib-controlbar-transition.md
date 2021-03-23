---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
uuid: abd98898-d7d8-468f-b696-052e61e171b5
feature: Dynamic Mediaクラシック，ビューア，SDK/API，ビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

ビデオビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 </p> <p>すぐに表示/非表示にするには、<span class="codeph"> none</span>を使用します。 徐々にフェードイン/フェードアウトするには、<span class="codeph"> fade</span>を使用します。 </p> <p>fadeはInternet Explorer 8ではサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーによって記録される最後のマウス/タッチイベントから、コントロールバーが非表示になるまでの時間を秒単位で指定します。 </p> <p> <span class="codeph"> -1</span>に設定した場合、コンポーネントは自動非表示の効果をトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>フェードイン/フェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
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

