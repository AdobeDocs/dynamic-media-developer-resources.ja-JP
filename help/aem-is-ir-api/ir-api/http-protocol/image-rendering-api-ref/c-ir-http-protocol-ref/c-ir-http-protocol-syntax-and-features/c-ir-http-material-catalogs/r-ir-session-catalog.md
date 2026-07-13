---
title: セッションカタログ
description: セッションカタログは、リクエストのセッション属性を提供するマテリアルカタログであり、すべてのsrc=、vignette=、およびicc= コマンドのデフォルトのcatId値です。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
TQID: 'https://experienceleague.adobe.com/--3F69i8XdliFxf5IhMPbUThRzMNyIDjtW4-Y-SBCFE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 235
ht-degree: 0%

---

# セッションカタログ{#session-catalog}

セッションカタログは、リクエストのセッション属性を提供するマテリアルカタログであり、すべての`src=`、`vignette=`、および`icc=` コマンドのデフォルトのcatId値です。

セッションカタログは、HTTP リクエストパスの最初のパス要素（サーバー名の直後）として指定されます。 最初のパス要素が任意のカタログの属性：:RootIdと一致しない場合、デフォルトカタログがセッションカタログとして使用されます。

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
   <td> <p> <span class="codeph">属性：:RootPath</span> </p> </td> 
   <td> <p> マテリアル データ ファイルのルート パス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:VignettePath</span> </p> </td> 
   <td> <p> 周辺光量補正ファイルのルートパス </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:IccProfileRgb</span> </p> </td> 
   <td> <p> ビネットがICC プロファイルを埋め込まない場合のデフォルトの作業用カラースペース </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span> コマンドの相対HTTP ファイルパスのルート URL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重なり合うオブジェクトの初期表示/非表示の状態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：有効期限</span> </p> </td> 
   <td> <p> プロキシサーバーおよびブラウザーキャッシュの返信画像の有効期間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:MaxPix</span> </p> </td> 
   <td> <p> 返信画像の幅と高さの最大値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span>および<span class="codeph"> hei=</span>の既定値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:Format</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span>の既定値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:JpegQuality</span> </p> </td> 
   <td> <p> <span class="codeph"> qlt=</span>の既定値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:TiffEncoding</span> </p> </td> 
   <td> <p> TIFF出力用の圧縮タイプ </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：：シャープ </span> </p> </td> 
   <td> <p> <span class="codeph"> sharpen=</span>の既定値 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:OnFailSel</span> </p> </td> 
   <td> <p> <span class="codeph"> sel=</span> コマンドが失敗したときに動作を指定します </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">属性：:OnFailObj</span> </p> </td> 
   <td> <p> <span class="codeph"> obj=</span> コマンドが失敗したときに動作を指定します </p> </td> 
  </tr> 
 </tbody> 
</table>

