---
title: ControlBar.transition
description: コントロール バーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード </span> </p> </td> 
   <td colname="col2"> <p> コントロール バーとそのコンテンツの表示/非表示を切り替えるために使用する効果の種類を指定します。 「なし」 <span class="codeph"> を使用 </span> ると、表示と非表示を瞬時に切り替えることができます。<span class="codeph"> のフェードイン </span> フェードアウト効果により、フェードインとフェードアウトが徐々に変化します（Internet Explorer 8 ではサポートされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> コントロール バーが登録する最後のマウスまたはタッチ イベントからタイム コントロール バーが非表示になるまでの時間（秒）を指定します。 </p> <p> <span class="codeph">-1 </span> に設定すると、コンポーネントは自動的に非表示になる効果をトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p> フェードインおよびフェードアウト アニメーションのデュレーションを秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。 このコマンドは、コントロールバーの自動非表示が無効になっているタッチデバイスでは無視されます。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
