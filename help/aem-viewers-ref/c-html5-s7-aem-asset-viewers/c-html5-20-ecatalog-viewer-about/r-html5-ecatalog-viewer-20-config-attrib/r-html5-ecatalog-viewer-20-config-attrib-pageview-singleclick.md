---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Mediaクラシック，ビューア，SDK/API,eCatalog
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作を対応付けます。<span class="codeph"> none </span>に設定すると、シングルクリック/タップによるズームが無効になります。 <span class="codeph"> zoom </span>を指定すると、画像をクリックした場合に1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム率が指定の限界値以上ならリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-edcfcd6c0bd24ac093442c56450b3c97}

（オプション）

## 初期設定 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` （デスクトップコンピューターの場合） `none` タッチデバイスの場合。

## 例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
