---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: faa6344a-a0b5-4b27-818b-81e9e0b721b4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> ズーム画像に適用される画像サービングコマンド文字列。 URLで指定する場合、 <span class="codeph"> &amp;</span>と<span class="codeph"> =</span>はすべて、 <span class="codeph"> %26</span>と<span class="codeph"> %3D</span>にそれぞれHTTPエンコードする必要があります。 </p> <p> <p>注意： 画像のサイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

ビューアのURLで指定する場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

configデータで指定する場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
