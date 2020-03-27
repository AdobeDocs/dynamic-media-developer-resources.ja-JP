---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 3e57e235-7888-4ba2-9c8e-4f568a6caa52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> シングルクリック/タップとズーム操作の対応関係を設定します。noneを指定すると、 <span class="codeph"> シング </span> ルクリック/タップによるズームが無効になります。 zoomを指定すると、画 <span class="codeph"> 像をク </span> リックした場合に1段階ズームインします。Ctrlキーを押しながらクリックすると、1段階ズームアウトします。 resetを指定す <span class="codeph"> ると、 </span> 画像をシングルクリックした場合に、初期のズームレベルまでズームがリセットされます。 zoomResetの <span class="codeph"> 場合、 </span>現在のズーム率が指定の限界値以上の場合はリセットが適用され、それ以外の場合はズームが適用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` デスクトップコンピューターでタッチ `none` デバイスの場合。

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
