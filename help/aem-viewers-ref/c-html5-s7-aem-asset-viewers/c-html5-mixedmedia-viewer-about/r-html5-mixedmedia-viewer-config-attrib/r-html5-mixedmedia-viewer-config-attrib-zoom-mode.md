---
title: zoomMode
description: ズーム操作の種類を設定します。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 2%

---

# zoomMode{#zoommode}

ズーム操作の種類を設定します。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">連続|インライン|自動</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">連続</span>を使用すると、メイン表示でクリック、ダブルタップ、またはピンチアウトしたときに、画像が徐々にズームインする従来のズームが可能になります。 初期ビューに戻るには、ズームアウトするか、ズーム状態をリセットします。 クラス </p> <p> <span class="codeph"> インライン </span>では、デスクトップのメインビューにカーソルを合わせたり、タッチデバイスでタッチ&amp;ホールドしたりすると、ズームされた画像が即座に表示されるインスタントズームが有効になります。 マウスをビューから移動するか、指を放すと、画像は自動的に初期状態に戻ります。 <span class="codeph"> インライン </span> モードでは、ネストされた画像セットは統合され、個々のサムネールとして表示されます。 クラス <span class="codeph">の自動</span>は、デスクトップではインラインモードを、タッチデバイスでは連続モードを有効にします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
