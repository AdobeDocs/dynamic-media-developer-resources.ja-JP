---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: e2a9388d-c753-4988-9aa0-73c4d0428d67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 8%

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> ズーム画像に適用される画像サービングコマンド文字列です。 URLで指定する場合、すべての<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>を<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTPエンコードする必要があります。 </p> <p> <p>注意： 画像サイズ変更操作コマンドはサポートされていません。 </p> </p> </td> 
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
