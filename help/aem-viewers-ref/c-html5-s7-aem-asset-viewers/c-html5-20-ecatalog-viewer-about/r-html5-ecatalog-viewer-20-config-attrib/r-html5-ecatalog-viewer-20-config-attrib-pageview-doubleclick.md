---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# PageView.doubleclick{#pageview-doubleclick}

`[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

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

デスクトップコンピューターでは `reset`、タッチデバイスでは `zoomReset` を使用します。

## 例 {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
