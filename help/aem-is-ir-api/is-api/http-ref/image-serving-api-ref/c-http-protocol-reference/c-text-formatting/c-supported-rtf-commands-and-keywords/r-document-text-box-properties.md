---
description: 次のドキュメントプロパティは、テキストボックスでサポートされています。
solution: Experience Manager
title: 文書（テキストボックス）のプロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
TQID: 'https://experienceleague.adobe.com/U8T6F0KmGyopf6rXM0-zssY-hpfKPVUHWt-vO8aA7xM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 文書（テキストボックス）のプロパティ{#document-text-box-properties}

次のドキュメントプロパティは、テキストボックスでサポートされています。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> コマンド </b> </th> 
   <th class="entry"> <b>説明</b> </th> 
   <th class="entry"> <b> メモ </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>フォントテーブル： </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>フォント <i>N</i>の文字セット。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGBのカラーテーブル： </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK カラーテーブル。 </p> </td> 
   <td> <p>Dynamic Media拡張機能： </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>画像サービングカラーのカラーテーブル。 </p> </td> 
   <td> <p>Dynamic Media拡張機能；<span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>赤色のコンポーネント： </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>にのみ表示されます；0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span> </span> </td> 
   <td> <p>緑色のコンポーネント： </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>にのみ表示されます；0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span> </span> </td> 
   <td> <p>青色コンポーネント： </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>にのみ表示されます；0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span> </span> </td> 
   <td> <p>シアンカラーコンポーネント： </p> </td> 
   <td> <p>Dynamic Media拡張機能。表示できるのは<span class="codeph"> \cmykcolortbl </span>; 0...100のみです </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>マゼンタのカラーコンポーネント： </p> </td> 
   <td> <p>Dynamic Media拡張機能。表示できるのは<span class="codeph"> \cmykcolortbl </span>; 0...100のみです </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow <span class="varname"> N </span> </span> </td> 
   <td> <p>黄色のカラーコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。表示できるのは<span class="codeph"> \cmykcolortbl </span>; 0...100のみです </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black <span class="varname"> N </span> </span> </td> 
   <td> <p>黒のカラーコンポーネント： </p> </td> 
   <td> <p>Dynamic Media拡張機能。表示できるのは<span class="codeph"> \cmykcolortbl </span>; 0...100のみです </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>左マージン。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>右マージン。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>上マージン： </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>下余白： </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>テキストボックス内のテキストの上揃え。 </p> </td> 
   <td> <p>初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>テキストボックス内のテキストの下揃え。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>テキストボックス内のテキストを中央に配置します。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>テキストフローの向き。 </p> </td> 
   <td> <p>言語固有のテキストフロー；<span class="codeph"> textPs= </span> only 0 （default） left-right, top-bottom （European） 1 top-bottom, right-left （Far Eastern） </p> </td> 
  </tr> 
 </tbody> 
</table>
