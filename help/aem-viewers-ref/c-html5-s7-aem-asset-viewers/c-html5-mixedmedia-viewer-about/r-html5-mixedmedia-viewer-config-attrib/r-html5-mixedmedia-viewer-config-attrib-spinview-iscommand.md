---
title: SpinView.iscommand
description: SpinView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: d616c8cf-6717-48f9-9926-1b37afe0e444
TQID: 'https://experienceleague.adobe.com/VJ07whEz3jCqP-QzIFR21GH-a2yjEZVoN6-Pjwsnwmw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 6%

---

# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> スピン画像に適用される画像サービングコマンド文字列。 URLで指定した場合、<span class="codeph"> &amp;</span>および<span class="codeph"> =</span>のすべての出現箇所は、それぞれ<span class="codeph"> %26</span>および<span class="codeph"> %3D</span>としてHTTP エンコードする必要があります。 </p> <p> <p>注意：画像サイズ変更の操作コマンドはサポートされていません。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

なし

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

ビューア URLで指定した場合：

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

設定データで指定した場合：

`iscommand=op_sharpen=1&op_colorize=0xff0000`
