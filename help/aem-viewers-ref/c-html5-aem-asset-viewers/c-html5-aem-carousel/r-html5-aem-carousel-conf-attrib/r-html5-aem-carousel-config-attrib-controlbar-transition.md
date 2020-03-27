---
description: カルーセルビューアの設定属性。
seo-description: カルーセルビューアの設定属性。
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

カルーセルビューアの設定属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohideduration`*[, *``*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 </p> <p>すぐに表示/非 <span class="codeph"> 表示にする</span> には、noneに設定します。 </p> <p>徐々にフェードイ <span class="codeph"> ン</span> /フェードアウトする効果を適用するには、fadeに設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーが最後に登録したマウス/タッチイベントから、コントロールバーが非表示になるまでの時間を秒単位で指定します。 </p> <p>-1に設定すると <span class="codeph"></span> 、コンポーネントの自動非表示の効果はトリガされないので、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> フェードイン/フェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）このコマンドは、コントロールバーの自動非表示が無効になっているタッチデバイスでは無視されます。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

