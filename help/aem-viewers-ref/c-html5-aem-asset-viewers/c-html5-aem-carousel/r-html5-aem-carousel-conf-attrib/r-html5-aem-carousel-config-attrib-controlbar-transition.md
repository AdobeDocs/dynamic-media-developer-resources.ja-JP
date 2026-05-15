---
title: ControlBar.transition
description: カルーセルビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
TQID: 'https://experienceleague.adobe.com/oVi-FxRdW7mQ-HlLoExaCG6cAB56WDuupA2RnEM7pqY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

カルーセルビューアの設定属性。

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示に使用するエフェクトタイプを指定します。 </p> <p>インスタント表示/非表示を切り替えるには、<span class="codeph"> none</span>に設定します。 </p> <p>段階的なフェードイン/フェードアウト効果を提供するために、<span class="codeph"> フェード </span>に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> コントロールバーによって登録された最後のマウス/タッチイベントとタイムコントロールバーが非表示になるまでの時間を秒単位で指定します。 </p> <p><span class="codeph"> -1</span>に設定した場合、コンポーネントは自動非表示エフェクトをトリガーしないため、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">期間</span></span> </p> </td> 
   <td colname="col2"> <p> フェードイン/フェードアウト アニメーションのデュレーションを秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。 コントロールバーの自動非表示が無効になっているタッチデバイスでは、このコマンドは無視されます。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
