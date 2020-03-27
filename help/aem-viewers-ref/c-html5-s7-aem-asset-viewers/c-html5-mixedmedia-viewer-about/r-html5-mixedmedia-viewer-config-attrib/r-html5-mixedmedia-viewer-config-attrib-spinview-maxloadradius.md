---
description: SpinViewがアイドルの場合に各方向でプリロードするフレームの最大数を表します。
seo-description: SpinViewがアイドルの場合に各方向でプリロードするフレームの最大数を表します。
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.maxloadradius{#spinview-maxloadradius}

SpinViewがアイドルの場合に各方向でプリロードするフレームの最大数を表します。

` [SpinView.|<containerId>_spinView.]maxloadradius= *`valuehighRes`*[, *``*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> 値を —1に設定すると、セ <span class="codeph"> ット内の</span> すべてのフレームがプリロードされます。 プリロードされたフレームは、常にSpinViewが最初に読み込まれた元の解像度で表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> プリロードされたフレームの品質を制御します。 </p> <p>1に設定すると <span class="codeph"></span> 、高品質でフレームが読み込まれ、コンポーネントのサイズに合わせられます。 </p> <p>0に設定すると、低 <span class="codeph"> 解像度の</span> プレビュータイルのみが読み込まれます。 </p> <p>高解像度でプリロードすると、特に自動スピンが有効な場合に、エンドユーザーの操作性が向上します。 同時に、開始時間が遅くなり、ネットワーク消費が高くなるので、注意して使用する必要があります。 高解像度のプリロードを使用する場合、プリロードされたフレームは常に、コンポーネントが最初に読み込まれた元の解像度になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
