---
title: zoomMode
description: ズーム操作のタイプを設定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# zoomMode{#zoommode}

ズーム操作のタイプを設定します。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 連続 </span> は、メインビューでのクリック、ダブルタップまたはピンチアウトに応じて画像が徐々にズームインするクラシックズームを有効にします。 最初のビューに戻るには、ズームアウトするか、ズーム状態をリセットします。 クラス </p> <p> <span class="codeph"> inline </span> インスタントズームを有効にします。デスクトップでメインビューにマウスポインターを置くと、またはタッチデバイスでタッチ&amp;ホールドすると、ズームされた画像がすぐに表示されます。 マウスをビューから移動したり、指を放した後、画像は自動的に初期状態に戻ります。 In <span class="codeph"> inline </span> モードの場合、ネストされた画像セットは統合され、個々のサムネールとして表示されます。 クラス <span class="codeph"> auto </span> は、デスクトップでインラインモードをアクティブにし、タッチデバイスでは連続モードをアクティブにします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
