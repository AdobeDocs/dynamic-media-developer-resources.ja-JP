---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# ControlBar.transition{#controlbar-transition}

インタラクティブビデオビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration`*[, *``*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示に使用する効果の種類を指定します。 </p> <p>すぐに表示/非 <span class="codeph"> 表示にする</span> には、noneに設定します。 </p> <p>徐々にフェードイ <span class="codeph"> ン</span> /フェードアウトする効果を適用するには、fadeに設定します。 Internet Explorer 8ではサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーが最後に登録したマウス/タッチイベントから、コントロールバーが非表示になるまでの時間を秒単位で指定します。 -1に設定すると <span class="codeph"></span> 、コンポーネントの自動非表示の効果はトリガされないので、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> フェードイン/フェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

