---
description: セッションカタログは、要求のセッション属性と、すべてのsrc=、vignette=およびicc=コマンドの初期設定のcatId値を提供するマテリアルカタログです。
seo-description: セッションカタログは、要求のセッション属性と、すべてのsrc=、vignette=およびicc=コマンドの初期設定のcatId値を提供するマテリアルカタログです。
seo-title: セッションカタログ
solution: Experience Manager
title: セッションカタログ
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# セッションカタログ{#session-catalog}

セッションカタログは、要求のセッション属性と、すべてのsrc=、vignette=およびicc=コマンドの初期設定のcatId値を提供するマテリアルカタログです。

セッションカタログは、HTTP要求パスの最初のパス要素（サーバー名の直後）として指定されます。 最初のパス要素がカタログのattribute::RootIdと一致しない場合、デフォルトのカタログがセッションカタログとして使用されます。

セッションカタログには、次のセッションのデフォルト値が含まれます。

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
   <td> <p> <span class="codeph"> 属性：:IccProfileRgb</span> </p> </td> 
   <td> <p> ビネットにICCプロファイルが埋め込まれない場合の初期設定の作業用カラースペース </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::RootUrl</span> </p> </td> 
   <td> <p> src=commandsの相対HTTPファイルパスのル <span class="codeph"> ートURL</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重なりオブジェクトの初期状態の表示/非表示 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Expiration</span> </p> </td> 
   <td> <p> プロキシサーバーとブラウザーのキャッシュの応答画像の有効期間の値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> 許可される返信画像の幅と高さの最大値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> wid=およ <span class="codeph"> びhei=の</span> デフォ <span class="codeph"> ルト値</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> fmt=のデフォ <span class="codeph"> ルト値</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::JpegQuality</span> </p> </td> 
   <td> <p> qlt=のデフォ <span class="codeph"> ルト値</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::TiffEncoding</span> </p> </td> 
   <td> <p> TIFF画像出力の圧縮タイプ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Sharpen</span> </p> </td> 
   <td> <p> シャープのデフォ <span class="codeph"> ルト値=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:OnFailSel</span> </p> </td> 
   <td> <p> sel=コマンドが失敗した <span class="codeph"> 場合の動作</span> を指定します </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::OnFailObj</span> </p> </td> 
   <td> <p> obj=コマンドが失敗した <span class="codeph"> 場合の動作</span> を指定します </p> </td> 
  </tr> 
 </tbody> 
</table>

