---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

[!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリックまたはタップしてズームアクションへのマッピングを設定します。 なし </span> を <span class="codeph"> に設定すると、ダブルクリックやズームのタップが無効になります。 <span class="codeph"> ズームに設定した場合 </span> 画像をクリックすると、1 回のズームステップでズームします。Ctrl キーを押しながらクリックすると、1 回のズームステップでズームします。 リセット </span> に設定 <span class="codeph"> ると、画像を 1 回クリックするだけで、ズームが初期ズームレベルにリセットされます。 zoomReset </span> では、現在 <span class="codeph"> ズーム率が指定した制限以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

オプション。

## 初期設定 {#section-814d6bc6a0834005a0a72c7040e45693}

デスクトップコンピューターでは [!DNL `reset`]、タッチデバイスでは [!DNL `zoomReset`] を使用します。

## 例 {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
