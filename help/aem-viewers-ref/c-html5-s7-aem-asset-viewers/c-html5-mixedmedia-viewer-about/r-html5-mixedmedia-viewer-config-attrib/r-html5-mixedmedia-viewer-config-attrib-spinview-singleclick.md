---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 18c5c21d-af31-4b1c-ab8b-c04d08650123
TQID: 'https://experienceleague.adobe.com/I1Yo1KRG4FBftei2gQmpkeakND1CCP1VdVokHEILU2A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_0824E332DF1340A2ABC40A3EB428F2D0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップによるズームアクションのマッピングを設定します。 <span class="codeph">なし</span>に設定すると、シングルクリック/タップのズームが無効になります。 <span class="codeph">に設定した場合、画像をクリックすると</span>は1回のズームステップでズームアウトします。CTRL+クリックすると、1回のズームステップでズームアウトします。 <span class="codeph"> リセット </span>に設定すると、画像を1回クリックすると、ズームが初期スピンレベルにリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム係数が指定された制限を超えている場合はリセットが適用され、そうでない場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

デスクトップ コンピューターの`zoomReset`、タッチ デバイスの`none`。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
