---
description: ズーム操作のタイプを設定します。
seo-description: ズーム操作のタイプを設定します。
seo-title: zoomMode
solution: Experience Manager
title: zoomMode
topic: Dynamic media
uuid: fdbe7ab6-47db-46cf-8a0d-085c66d4b0f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# zoomMode{#zoommode}

ズーム操作のタイプを設定します。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuousを使 </span> 用すると、クラシックズームが有効になり、メインビューでクリック、ダブルタップまたはピンチアウトすると、画像が徐々にズームインします。 最初のビューに戻るには、明示的にズームアウトするか、ズーム状態をリセットする必要があります。 </p> <p> <span class="codeph"> inlineを使 </span> 用すると、インスタントズームが有効になり、デスクトップでメインビューにカーソルを合わせたとき、またはタッチデバイスでタッチ&amp;ホールドしたときに、ズームされた画像が即座に表示されます。ビューからマウスを移動するか、指を離すと、画像が自動的に初期状態に戻ります。 インラインモードでは、ネ <span class="codeph"> ストさ </span> れた画像セットは統合され、個々のサムネールとして表示されます。 <span class="codeph"> autoを指定する </span> と、デスクトップではインラインモードがアクティブになり、タッチデバイスでは連続モードがアクティブになります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
