---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohideduration`*[, *``*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
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

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
