---
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

インタラクティブビデオビューアの設定属性。

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> コンポーネントのプリロード動作を指定します。 </p> <p><span class="codeph"> -1</span>に設定すると、コンポーネントの初期化時またはアセットの変更時に、すべてのスウォッチが同時に読み込まれます。 </p> <p><span class="codeph"> 0</span>に設定すると、表示されているスウォッチのみが読み込まれます。 </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>に設定して、表示されている領域の周りにある非表示の行/列を、いくつプリロードするかを定義します。 </p> </td> 
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

