---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 919dd48e-b621-4dbb-9cae-f2d0f91f45a9
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

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`zoomReset` デスクトップコンピューターでタッチ `none` デバイスの場合。

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
