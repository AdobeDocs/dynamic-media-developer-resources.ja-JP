---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick
feature: Dynamic Media Classic，ビューア，SDK/API，スピンセット
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作との対応関係を設定します。<span class="codeph"> none </span>に設定すると、シングルクリック/タップによるズームが無効になります。 <span class="codeph">スピン</span>に設定すると、画像をクリックすると、1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のスピンレベルまでズームがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のズーム率が指定の限界値以上であればリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-924163cb2f6542499f49894becef7fb5}

（オプション）

## 初期設定 {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` （デスクトップコンピューターの場合） `none` （タッチデバイスの場合）

## 例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
