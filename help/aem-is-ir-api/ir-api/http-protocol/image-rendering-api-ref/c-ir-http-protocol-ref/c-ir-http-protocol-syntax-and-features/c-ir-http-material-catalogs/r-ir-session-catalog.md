---
description: セッションカタログは、要求のセッション属性と、すべてのsrc=、vignette=およびicc=コマンドのデフォルトのcatId値を提供するマテリアルカタログです。
solution: Experience Manager
title: セッションカタログ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# セッションカタログ{#session-catalog}

セッションカタログは、要求のセッション属性と、すべてのsrc=、vignette=およびicc=コマンドのデフォルトのcatId値を提供するマテリアルカタログです。

セッションカタログは、HTTPリクエストパスの最初のパス要素として指定します（サーバー名のすぐ後）。 最初のパス要素がカタログのattribute::RootIdと一致しない場合、デフォルトのカタログがセッションカタログとして使用されます。

セッションカタログには、次のセッションデフォルト値が用意されています。

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootPath</span> </p> </td> 
   <td> <p> 材料データファイルのルートパス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> ビネットファイルのルートパス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> ビネットがICCプロファイルを埋め込まない場合のデフォルトの作業カラースペース </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span>コマンドの相対HTTPファイルパスのルートURL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重なりオブジェクトの最初の表示/非表示の状態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> プロキシサーバーおよびブラウザーキャッシュの応答画像の有効期間の値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> 返信画像の最大の幅と高さ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span>および<span class="codeph"> hei=</span>のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span>のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> <span class="codeph"> qlt=</span>のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> TIFF画像出力の圧縮タイプ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Sharpen</span> </p> </td> 
   <td> <p> <span class="codeph"> sharpen=</span>のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> <span class="codeph"> sel=</span>コマンドが失敗した場合の動作を指定します </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> <span class="codeph"> obj=</span>コマンドが失敗した場合の動作を指定します </p> </td> 
  </tr> 
 </tbody> 
</table>
