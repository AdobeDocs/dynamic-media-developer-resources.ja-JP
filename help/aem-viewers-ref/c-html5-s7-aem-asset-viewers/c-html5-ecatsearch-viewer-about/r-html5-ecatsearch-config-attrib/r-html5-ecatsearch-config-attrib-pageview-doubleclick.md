---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

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

[!DNL `reset`] （デスクトップコンピューターの場合） [!DNL `zoomReset`] （タッチデバイスの場合）

## 例 {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
