---
title: FlyoutZoomView.imagereload
description: サイズ変更時に、コンポーネントがメインビューとフライアウトビューの新しい画像を取得する方法を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
TQID: 'https://experienceleague.adobe.com/vyA-GdKo06kVi3jO6wlBIyov3XvKVo1vwPj3mzqyoc4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

サイズ変更時に、コンポーネントがメインビューとフライアウトビューの新しい画像を取得する方法を設定します。

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 0 </span>に設定すると、コンポーネントはサイズ変更中に新しい画像を読み込まず、フライアウトビューの画像解像度も変更されません。 </p> <p><span class="codeph"> 1 </span>に設定すると、メインビューに読み込まれる画像の1つ以上の幅ブレークポイントを指定できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ブレークポイント、<span class="varname">幅</span>[; <span class="varname">幅</span>] </span> </p> </td> 
   <td colname="col2"> <p>メインビューに読み込まれた画像の幅ブレークポイント。 コンポーネントは常に初期負荷に最適なサイズを使用します。 サイズを変更すると、メインビュー内の画像が常に幅が最も大きいブレークポイントに等しくダウンロードされ、クライアントでダウンスケールされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
