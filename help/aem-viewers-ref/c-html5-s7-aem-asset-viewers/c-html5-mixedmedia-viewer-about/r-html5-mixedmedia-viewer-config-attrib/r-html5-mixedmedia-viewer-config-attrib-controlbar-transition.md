---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
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

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
