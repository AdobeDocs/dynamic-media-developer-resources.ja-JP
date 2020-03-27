---
description: 'null'
seo-description: 'null'
seo-title: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic media
uuid: 302e20bf-d398-45de-98a5-58b9edde48f3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。 指定した形式が —alphaで終わる場合 <span class="codeph"></span>、画像は透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として処理されます。 コンポーネントの背景色はデフォルトで白です。 したがって、透明にするには、 <span class="codeph"> CSSプロパティbackground-color</span> をtransparentに設定 <span class="codeph"> します</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-12a6fb2fcbc1476b95bd53ce880dc185}

（オプション）

## 初期設定 {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## 例 {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
