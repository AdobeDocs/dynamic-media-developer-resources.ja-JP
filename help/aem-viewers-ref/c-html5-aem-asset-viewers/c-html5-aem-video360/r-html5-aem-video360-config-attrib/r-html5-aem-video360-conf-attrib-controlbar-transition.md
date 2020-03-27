---
description: ビデオ360ビューアの設定属性。
seo-description: ビデオ360ビューアの設定属性。
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e8c1da96-3533-4d31-9ad3-569a87948ac6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

ビデオ360ビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration`*[, *``*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 </p> <p>「なし」を <span class="codeph"> 使用す</span> ると、すぐに表示/非表示が切り替わります。 徐々にフェ <span class="codeph"> ードイン</span> /フェードアウトする効果を適用するには、fadeを使用します。 </p> <p>フェードは、Internet Explorer 8ではサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p>コントロールバーが最後に登録し、コントロールバーが非表示になるマウス/タッチイベントの間隔を秒単位で指定します。 </p> <p> -1に設定すると <span class="codeph"></span> 、コンポーネントの自動非表示の効果はトリガーされず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 期 <span class="varname"> 間</span></span> </p> </td> 
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

