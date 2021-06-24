---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップとズーム操作との対応関係を設定します。 <span class="codeph"> none </span>に設定すると、ダブルクリック/タップによるズームが無効になります。 <span class="codeph"> zoom </span>に設定すると、画像をクリックした場合に1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム率が指定の限界値以上であればリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

（オプション）

## 初期設定 {#section-814d6bc6a0834005a0a72c7040e45693}

`reset` （デスクトップコンピューターの場合） `zoomReset` （タッチデバイスの場合）

## 例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
