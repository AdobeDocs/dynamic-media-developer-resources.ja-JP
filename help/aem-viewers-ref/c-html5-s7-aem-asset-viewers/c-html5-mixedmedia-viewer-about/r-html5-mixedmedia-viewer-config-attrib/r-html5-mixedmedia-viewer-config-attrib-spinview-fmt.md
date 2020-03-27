---
description: 'null'
seo-description: 'null'
seo-title: SpinView.fmt
solution: Experience Manager
title: SpinView.fmt
topic: Dynamic media
uuid: ad4bb340-3144-46e8-a184-a5cae572596c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.fmt{#spinview-fmt}

`[SpinView.|<containerId>_spinView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_68C0C3D5C60640DC9A8EE04EA685AB99"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> コンポーネントがImage Serverからの画像の読み込みに使用する画像形式を指定します。 指定した形式が —alphaで終わる場合 <span class="codeph"></span>、画像は透明なコンテンツとしてレンダリングされます。 その他のすべての画像形式の場合、画像は不透明として処理されます。 </p> <p>コンポーネントの背景色はデフォルトで白です。 したがって、透明にするには、 <span class="codeph"> CSSプロパティbackground-color</span> をtransparentに設定 <span class="codeph"> します</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
