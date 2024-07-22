---
title: ControlBar.transition
description: カルーセルビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

カルーセルビューアの設定属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード </span> </p> </td> 
   <td colname="col2"> <p> コントロール バーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 </p> <p><span class="codeph"> なし」に設定すると </span> 表示/非表示を即座に切り替えることができます。 </p> <p>徐々にフェードイン/フェードアウトする効果を得るには </span> フェードを <span class="codeph"> に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーによって登録された最後のマウスまたはタッチイベントからタイムコントロールバーが非表示になるまでの時間（秒）を指定します。 </p> <p><span class="codeph">-1 に設定すると </span> コンポーネントは自動的に隠す効果をトリガーしないので、常に画面に表示されたままになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> フェードイン/フェードアウトアニメーションのデュレーションを秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。 このコマンドは、コントロールバーの自動非表示が無効になっているタッチデバイスでは無視されます。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
