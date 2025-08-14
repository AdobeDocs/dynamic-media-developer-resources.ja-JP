---
title: ControlBar.transition
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

インタラクティブビデオビューアの設定属性。

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード </span> </p> </td> 
   <td colname="col2"> <p> コントロール バーとその内容の表示/非表示を切り替えるために使用する効果の種類を指定します。 </p> <p><span class="codeph"> なし」に設定すると </span> 表示/非表示を即座に切り替えることができます。 </p> <p>徐々にフェードイン/フェードアウトする効果を得るには <span class="codeph"> フェードを </span> に設定します。 Internet Explorer 8 ではサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーによって登録された最後のマウスまたはタッチイベントからタイムコントロールバーが非表示になるまでの時間（秒）を指定します。 <span class="codeph">-1 に設定すると </span> コンポーネントは自動的に隠す効果をトリガーしないので、常に画面に表示されたままになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> フェードイン/フェードアウトアニメーションのデュレーションを秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
