---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Mediaクラシック，ビューア，SDK/API，混在メディアセット
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

---


# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>コンポーネントのプリロード動作を指定します。 <span class="codeph"> -1</span>に設定すると、コンポーネントの初期化時またはアセットの変更時に、すべてのスウォッチが同時に読み込まれます。 </p> <p><span class="codeph"> 0</span>に設定すると、表示されているスウォッチのみが読み込まれます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> で、表示されている領域の周りにある非表示の行/列を、いくつプリロードするかを定義します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
