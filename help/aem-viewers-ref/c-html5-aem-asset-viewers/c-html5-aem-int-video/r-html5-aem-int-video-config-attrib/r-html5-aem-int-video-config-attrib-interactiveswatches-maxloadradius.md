---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: InteractiveSwatches.maxloadradius
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
topic: Dynamic media
uuid: 12391b8b-532f-4e68-ad60-4dbcc86d9e58
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

インタラクティブビデオビューアの設定属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 </p> <p>-1を指定すると <span class="codeph"></span> 、コンポーネントの初期化時またはアセットの変更時に、すべてのスウォッチが同時に読み込まれます。 </p> <p>0に設定すると、表示され <span class="codeph"> ている</span> スウォッチのみが読み込まれます。 </p> <p>preloadnbrに設定 <span class="codeph"><span class="varname"> すると</span></span> 、表示領域の周りに表示されない行/列がプリロードされる数を定義できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

