---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> 重複クリック/タップとスピン操作を対応付けます。 <span class="codeph"> none </span>に設定すると、重複クリック/タップによるスピンが無効になります。 <span class="codeph"> zoom </span>を指定すると、画像をクリックした場合に1回のスピンステップでスピンします。Ctrlキーを押しながらクリックすると、1つのスピンステップをスピンアウトします。 <span class="codeph"> reset </span>に設定すると、画像をシングルクリックした場合に、初期のスピンレベルまでスピンがリセットされます。 <span class="codeph"> zoomReset </span>の場合、現在のスピン率が指定の限界値以上ならリセットが適用され、それ以外の場合はスピンが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` （デスクトップコンピューターの場合） `zoomReset` タッチデバイスの場合。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
