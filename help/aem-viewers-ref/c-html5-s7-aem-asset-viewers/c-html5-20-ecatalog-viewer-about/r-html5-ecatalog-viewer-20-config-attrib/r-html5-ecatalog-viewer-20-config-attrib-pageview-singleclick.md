---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# PageView.singleclick{#pageview-singleclick}

`[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作との対応関係を設定します。<span class="codeph"> none </span>に設定すると、シングルクリック/タップによるズームが無効になります。 <span class="codeph"> zoom </span>に設定すると、画像をクリックした場合に1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム率が指定の限界値以上であればリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-edcfcd6c0bd24ac093442c56450b3c97}

（オプション）

## 初期設定 {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` （デスクトップコンピューターの場合） `none` （タッチデバイスの場合）

## 例 {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
