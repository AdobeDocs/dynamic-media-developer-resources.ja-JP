---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Mediaクラシック，ビューア，SDK/API，フライアウト
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 <span class="codeph"> -1</span>に設定すると、コンポーネントの初期化時またはアセットの変更時に、すべてのスウォッチが同時に読み込まれます。 <span class="codeph"> 0</span>に設定すると、表示されているスウォッチのみが読み込まれます。 </p> <p><span class="codeph"> <span class="varname"> preloadnbr読み込みを行う</span></span> には、表示されている領域の周りにある非表示の行/列をいくつプリロードするかを指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

（オプション）

## 初期設定 {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## 例 {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
