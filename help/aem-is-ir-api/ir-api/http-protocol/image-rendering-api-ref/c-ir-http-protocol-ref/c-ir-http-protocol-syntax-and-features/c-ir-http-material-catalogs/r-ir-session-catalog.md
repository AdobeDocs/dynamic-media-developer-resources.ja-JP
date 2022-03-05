---
title: セッションカタログ
description: セッションカタログは、要求のセッション属性と、すべての src=、vignette=、および icc=コマンドのデフォルトの catId 値を提供するマテリアルカタログです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# セッションカタログ{#session-catalog}

セッションカタログは、要求のセッション属性を提供するマテリアルカタログで、すべてのデフォルトの catId 値を提供します `src=`, `vignette=`、および `icc=` コマンド

セッションカタログは、HTTP リクエストパスの最初のパス要素として指定します（サーバー名のすぐ後）。 最初のパス要素がカタログの attribute::RootId と一致しない場合、デフォルトのカタログがセッションカタログとして使用されます。

セッションカタログには、次のセッションのデフォルト値が用意されています。

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
   <td> <p> ビネットが ICC プロファイルを埋め込まない場合のデフォルトの作業用カラースペース </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> の相対 HTTP ファイルパスのルート URL <span class="codeph"> src=</span> コマンド </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重複オブジェクトの最初の表示/非表示の状態 </p> </td> 
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
   <td> <p> のデフォルト値 <span class="codeph"> wid=</span> および <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> のデフォルト値 <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> のデフォルト値 <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> TIFF画像出力の圧縮タイプ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Sharpen</span> </p> </td> 
   <td> <p> のデフォルト値 <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailSel</span> </p> </td> 
   <td> <p> 動作を指定します。 <span class="codeph"> sel=</span> コマンドが失敗しました </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> 動作を指定します。 <span class="codeph"> obj=</span> コマンドが失敗しました </p> </td> 
  </tr> 
 </tbody> 
</table>
