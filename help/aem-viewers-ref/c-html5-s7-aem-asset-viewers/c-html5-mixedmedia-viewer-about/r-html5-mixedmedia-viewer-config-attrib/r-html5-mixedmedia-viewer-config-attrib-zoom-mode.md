---
description: ズーム操作のタイプを設定します。
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

ズーム操作のタイプを設定します。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuousを使用す </span> ると、メインビューでクリック、ダブルタップまたはピンチアウトを行うたびに、画像が徐々にズームインします。最初のビューに戻るには、明示的にズームアウトするか、ズーム状態をリセットする必要があります。 </p> <p> <span class="codeph"> inlineを使用す </span> ると、インスタントズームが可能になり、デスクトップ上でメインビューにカーソルを合わせるときや、タッチデバイス上でタッチ&amp;ホールドするときに、ズームされた画像がすぐに表示されます。表示からマウスを移動したり、指を離すと、画像は自動的に初期状態に戻ります。<span class="codeph">インライン</span>モードでは、ネストされた画像セットは統合され、個々のサムネールとして表示されます。 <span class="codeph"> autoを指定す </span> ると、デスクトップではインラインモード、タッチデバイスでは連続モードがアクティブになります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
