---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示を切り替える効果の種類を指定します。 </p> <p><span class="codeph"> none</span>を使用すると、表示と非表示を即座に切り替えることができます。 徐々にフェードイン/フェードアウトするには、 <span class="codeph"> fade</span>を使用します。 </p> <p>fadeはInternet Explorer 8ではサポートされていません。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>コントロールバーが最後に登録するマウス/タッチイベントから、コントロールバーが非表示になるまでの時間を秒単位で指定します。 </p> <p> <span class="codeph"> -1</span>に設定した場合、コンポーネントの自動非表示効果はトリガーされず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>フェードイン/フェードアウトアニメーションの時間を秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
