---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
feature: Dynamic Mediaクラシック，ビューア，SDK/API，混在メディアセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 6%

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`番号`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> devicePixelRatio</span>が<span class="codeph"> 1</span>より大きいデバイス（iPhone4など高密度ディスプレイのデバイス）の最適化の有効化、制限または無効化を行います。 有効にすると、デバイスのピクセル率が<span class="codeph"> 1</span>のみであるかのようにコンポーネントでIS画像リクエストのサイズが制限され、帯域幅が減少します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 番号</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> limit </span>設定を使用すると、指定した制限値までの高ピクセル密度が有効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
