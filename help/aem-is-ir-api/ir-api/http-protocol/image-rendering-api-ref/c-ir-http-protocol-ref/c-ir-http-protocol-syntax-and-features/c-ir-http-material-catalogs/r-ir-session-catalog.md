---
description: セッションカタログは、要求のセッション属性を提供するマテリアルカタログです。また、すべてのsrc=、vignette=およびicc=コマンドの初期設定のcatId値も提供されます。
seo-description: セッションカタログは、要求のセッション属性を提供するマテリアルカタログです。また、すべてのsrc=、vignette=およびicc=コマンドの初期設定のcatId値も提供されます。
seo-title: セッションカタログ
solution: Experience Manager
title: セッションカタログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# セッションカタログ{#session-catalog}

セッションカタログは、要求のセッション属性を提供するマテリアルカタログです。また、すべてのsrc=、vignette=およびicc=コマンドの初期設定のcatId値も提供されます。

セッションカタログは、HTTP要求パスの最初のパス要素として指定します（サーバー名の直後）。 最初のパス要素がカタログのattribute::RootIdに一致しない場合、初期設定のカタログがセッションカタログとして使用されます。

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
   <td> <p> マテリアルデータファイルのルートパス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::VignettePath</span> </p> </td> 
   <td> <p> ビネットファイルのルートパス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::IccProfileRgb</span> </p> </td> 
   <td> <p> ビネットにICCプロファイルが埋め込まれない場合の初期設定の作業カラースペース </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span>コマンドの相対HTTPファイルパスのルートURL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重なり合うオブジェクトの最初の表示/非表示の状態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> プロキシサーバーとブラウザーキャッシュの応答画像の有効時間の値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> 許可される返信画像の幅と高さの最大値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span>と<span class="codeph"> hei=</span>のデフォルト値 </p> </td> 
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

