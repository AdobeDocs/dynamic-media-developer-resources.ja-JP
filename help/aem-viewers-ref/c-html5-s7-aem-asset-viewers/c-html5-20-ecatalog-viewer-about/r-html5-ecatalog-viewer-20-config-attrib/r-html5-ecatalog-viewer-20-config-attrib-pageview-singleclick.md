---
description: 'null'
seo-description: 'null'
seo-title: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
topic: Dynamic media
uuid: 608700d2-5be4-4b96-b026-b12a3ade68ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作の対応関係を設定します。noneを指定すると、 <span class="codeph"> シング </span> ルクリック/タップによるズームが無効になります。 zoomを指定すると、画 <span class="codeph"> 像をク </span> リックした場合に1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 resetを指定す <span class="codeph"> ると、 </span> 画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 zoomResetの <span class="codeph"> 場合、 </span>現在のズーム率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-edcfcd6c0bd24ac093442c56450b3c97}

（オプション）

## 初期設定 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` デスクトップコンピューターでタッチ `none` デバイスの場合。

## 例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
