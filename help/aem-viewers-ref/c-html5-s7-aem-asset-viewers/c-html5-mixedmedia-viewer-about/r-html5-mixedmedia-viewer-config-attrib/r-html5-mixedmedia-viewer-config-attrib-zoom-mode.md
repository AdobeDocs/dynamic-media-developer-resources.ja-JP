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
ht-degree: 2%

---

# zoomMode{#zoommode}

ズーム操作のタイプを設定します。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> 連続画 </span> を使用する <span class="codeph">、メインビューでクリック、ダブルタップ、またはピンチアウトすると、画像が徐々にズームインされる、クラシックズームが有効になります。 初期ビューに戻るには、ズームアウトするか、ズーム状態をリセットします。 クラス </p> <p> インライン </span> を使用する <span class="codeph">、即時ズームが有効になります。この場合、デスクトップ上でメイン ビューにカーソルを合わせたり、タッチ デバイスをタッチ アンド ホールドすると、ズームされた画像がただちに表示されます。 ビューからマウスを移動するか、指を放すと、イメージは自動的に初期状態に戻ります。 インラ <span class="codeph"> ン </span> モードでは、ネストされた画像セットは統合され、個々のサムネールとして表示されます。 このクラス <span class="codeph"> auto </span> は、デスクトップではインラインモードを、タッチデバイスでは継続モードをアクティブにします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

オプション。

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
