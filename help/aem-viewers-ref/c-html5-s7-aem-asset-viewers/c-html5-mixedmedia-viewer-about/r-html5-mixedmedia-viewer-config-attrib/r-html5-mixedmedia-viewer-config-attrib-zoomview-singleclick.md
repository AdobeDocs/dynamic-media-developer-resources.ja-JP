---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリックまたはタップによるズームアクションのマッピングを設定します。 なし <span class="codeph"> 設定すると </span> シングルクリック/タップズームが無効になります。 <span class="codeph"> ズームに設定した場合 </span> 画像をクリックすると、1 回のズームステップでズームします。Ctrl キーを押しながらクリックすると、1 回のズームステップでズームします。 リセット </span> に設定 <span class="codeph"> ると、画像を 1 回クリックするだけで、ズームが初期ズームレベルにリセットされます。 zoomReset </span> では、現在 <span class="codeph"> ズーム率が指定した制限以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

デスクトップコンピューターでは `zoomReset`、タッチデバイスでは `none` を使用します。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
