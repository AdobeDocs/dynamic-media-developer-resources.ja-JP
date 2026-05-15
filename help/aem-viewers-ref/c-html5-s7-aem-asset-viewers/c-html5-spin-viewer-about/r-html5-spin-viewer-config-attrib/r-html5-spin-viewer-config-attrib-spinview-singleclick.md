---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
TQID: 'https://experienceleague.adobe.com/DkpKrDJuqlcE93u-W3D7F1DwEwxhRet4lP8MHjC-9ZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップによるズームアクションのマッピングを設定します。 <span class="codeph">なし</span>に設定すると、シングルクリック/タップのズームが無効になります。 <span class="codeph"> スピン </span>に設定されている場合、画像をクリックすると1回のズームステップでズームアウトします。CTRL + クリックすると、1回のズームステップでズームアウトします。 <span class="codeph"> リセット </span>に設定すると、画像を1回クリックすると、ズームが初期スピンレベルにリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム係数が指定された制限を超えている場合はリセットが適用され、そうでない場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

オプション。

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

デスクトップ コンピューターの`zoomReset`、タッチ デバイスの`none`。

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
