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
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# zoomMode{#zoommode}

ズーム操作のタイプを設定します。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuousを </span> 使用すると、従来のズーム機能が有効になり、メイン表示でクリック、重複タップまたはピンチアウトすると、画像が徐々にズームインします。最初の表示に戻るには、明示的にズームアウトするか、ズーム状態をリセットする必要があります。 </p> <p> <span class="codeph"> inline </span> を指定すると、インスタントズームが有効になり、デスクトップでメイン表示にマウスを合わせたときやタッチデバイスでタッチ&amp;ホールドしたときに、ズームされた画像が即座に表示されます。マウスを表示から移動するか、指を離すと、画像が自動的に初期状態に戻ります。<span class="codeph">インライン</span>モードでは、ネストされた画像セットは統合され、個々のサムネールとして表示されます。 <span class="codeph"> autoは、デスクトップではインラインモードを、タッチデバイスでは連続モードを </span> アクティブにします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
