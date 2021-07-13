---
description: カルーセルビューアの設定属性。
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

カルーセルビューアの設定属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示を切り替える効果の種類を指定します。 </p> <p><span class="codeph"> none</span>に設定すると、すぐに表示/非表示になります。 </p> <p><span class="codeph"> fade</span>に設定すると、徐々にフェードイン/フェードアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーによって登録された最後のマウス/タッチイベントから、コントロールバーが非表示になるまでの時間を秒単位で指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントの自動非表示効果がトリガーされないので、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p> フェードイン/フェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）コントロールバーの自動非表示が無効になっているタッチデバイスでは、このコマンドは無視されます。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
