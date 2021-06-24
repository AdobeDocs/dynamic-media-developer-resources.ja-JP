---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 6%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`番号`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>が<span class="codeph"> 1</span>より大きいデバイス（iPhone4など高密度ディスプレイを使用するデバイス）の最適化の有効化、制限または無効化を行います。 有効にすると、デバイスのピクセル比が<span class="codeph"> 1</span>の場合と同じように、コンポーネントでISイメージリクエストのサイズが制限され、帯域幅が削減されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 番号</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> limit</span>設定を使用すると、指定された制限までの高ピクセル密度が有効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
