---
title: SpinView.enableHD
description: SpinView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *` 数値 `*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> devicePixelRatio</span> が <span class="codeph"> 1</span> より大きいデバ <span class="codeph"> ス、つまりiPhone4 などの高密度ディスプレイを使用するデバイスの最適化を有効、制限、または無効にします。 アクティブの場合、コンポーネントは、デバイスのピクセル比が <span class="codeph"> 1 だけであるかのように IS 画像リクエストのサイズを制限するので </span> 帯域幅が減ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> limit</span> 設定を使用する場合、コンポーネントは指定された制限までの高画素密度のみを有効にします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
