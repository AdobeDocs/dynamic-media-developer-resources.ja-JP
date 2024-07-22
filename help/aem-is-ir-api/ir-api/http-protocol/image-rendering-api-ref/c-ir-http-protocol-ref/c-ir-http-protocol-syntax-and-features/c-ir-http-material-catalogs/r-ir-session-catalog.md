---
title: セッションカタログ
description: セッションカタログは、リクエストのセッション属性と、すべての src=、vignette=、icc= コマンドのデフォルトの catId 値を提供する資料カタログです。
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

セッションカタログは、リクエストのセッション属性と、すべての `src=`、`vignette=`、`icc=` コマンドのデフォルトの catId 値を提供する材料カタログです。

セッションカタログは、HTTP リクエストパスの最初のパス要素として（サーバー名の直後に）指定されます。 最初のパス要素がどのカタログの attribute::RootId にも一致しない場合は、デフォルトのカタログがセッションカタログとして使用されます。

セッションカタログには、次のセッションのデフォルト値が表示されます。

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:RootPath</span> </p> </td> 
   <td> <p> マテリアル データ ファイルのルート パス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:VignettePath</span> </p> </td> 
   <td> <p> ビネットファイルのルートパス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:IccProfileRgb</span> </p> </td> 
   <td> <p> ビネットに ICC プロファイルが埋め込まれていない場合のデフォルトの作業カラースペース </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:RootUrl</span> </p> </td> 
   <td> <p> src=</span> コマンドの相対 HTTP ファイルパス <span class="codeph"> ルート URL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:ShowOverlapObjs</span> </p> </td> 
   <td> <p> オーバーラップ オブジェクトの初期表示/非表示状態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Expiration</span> </p> </td> 
   <td> <p> プロキシサーバーおよびブラウザーキャッシュの返信画像の有効期限の値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::MaxPix</span> </p> </td> 
   <td> <p> 許可される返信画像の最大の幅と高さ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span> および <span class="codeph"> hei=</span> のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute::Format</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span> のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:JpegQuality</span> </p> </td> 
   <td> <p> qlt=</span><span class="codeph"> デフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:TiffEncoding</span> </p> </td> 
   <td> <p> TIFF画像出力用の圧縮タイプ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:Sharpen</span> </p> </td> 
   <td> <p> <span class="codeph"> sharpen=</span> のデフォルト値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:OnFailSel</span> </p> </td> 
   <td> <p> <span class="codeph"> sel=</span> コマンドが失敗したときの動作を指定します </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 属性：:OnFailObj</span> </p> </td> 
   <td> <p> <span class="codeph"> obj=</span> コマンドが失敗したときの動作を指定します </p> </td> 
  </tr> 
 </tbody> 
</table>
