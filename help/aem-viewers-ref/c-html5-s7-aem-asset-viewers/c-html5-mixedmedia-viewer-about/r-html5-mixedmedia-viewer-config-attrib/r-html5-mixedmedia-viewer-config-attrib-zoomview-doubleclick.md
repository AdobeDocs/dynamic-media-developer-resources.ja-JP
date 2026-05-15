---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
TQID: 'https://experienceleague.adobe.com/JvxrF0i21MMccjMLvAB16fbZn95yqAq8As1Knu3lh2E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップによるズームアクションのマッピングを設定します。 <span class="codeph"> none </span>に設定すると、ダブルクリックまたはタップによるズームが無効になります。 <span class="codeph">に設定した場合、画像をクリックすると</span>は1回のズームステップでズームアウトします。CTRL+クリックすると、1回のズームステップでズームアウトします。 <span class="codeph"> リセット </span>に設定すると、画像を1回クリックすると、ズームが初期ズームレベルにリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム係数が指定された制限を超えている場合はリセットが適用され、そうでない場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

デスクトップ コンピューターの`reset`、タッチ デバイスの`zoomReset`。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
