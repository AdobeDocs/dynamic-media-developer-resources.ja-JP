---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
TQID: 'https://experienceleague.adobe.com/5kOYHbgdV2j5D34iHX0zu384E0sMjo6agU3d58LOsGI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップによるズームアクションのマッピングを設定します。 <span class="codeph"> none </span>に設定すると、ダブルクリックまたはタップによるズームが無効になります。 <span class="codeph">に設定した場合、画像をクリックすると</span>は1回のズームステップでズームアウトします。CTRL+クリックすると、1回のズームステップでズームアウトします。 <span class="codeph"> リセット </span>に設定すると、画像を1回クリックすると、ズームが初期ズームレベルにリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム係数が指定された制限を超えている場合はリセットが適用され、そうでない場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

オプション。

## 初期設定 {#section-814d6bc6a0834005a0a72c7040e45693}

デスクトップコンピューターの`reset`、タッチデバイスの`zoomReset`。

## 例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
