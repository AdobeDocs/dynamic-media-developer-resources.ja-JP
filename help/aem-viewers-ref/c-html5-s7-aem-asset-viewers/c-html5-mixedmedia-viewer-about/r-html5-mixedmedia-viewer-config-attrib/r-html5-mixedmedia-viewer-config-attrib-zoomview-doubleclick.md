---
title: ZoomView.doubleclick
description: ZoomView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e87981f8-8174-432a-89ea-fae74d0584ad
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# ZoomView.doubleclick{#zoomview-doubleclick}

`[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> ダブルクリック/タップとズーム操作のマッピングを設定します。 を <span class="codeph"> なし </span> を指定すると、ダブルクリック/タップによるズームが無効になります。 次に設定した場合： <span class="codeph"> ズーム </span> 画像をクリックすると、1 段階ズームインします。Ctrl キーを押しながらクリックすると、1 段階だけズームアウトします。 を <span class="codeph"> リセット </span> を指定すると、画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 の場合 <span class="codeph"> zoomReset </span>、現在のズーム率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` デスクトップコンピュータの場合 `zoomReset` （タッチデバイス）。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
