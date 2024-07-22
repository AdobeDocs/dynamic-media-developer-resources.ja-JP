---
description: 次のドキュメントプロパティは、テキストボックスでサポートされています。
solution: Experience Manager
title: ドキュメント（テキストボックス）のプロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# ドキュメント（テキストボックス）のプロパティ{#document-text-box-properties}

次のドキュメントプロパティは、テキストボックスでサポートされています。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> コマンド </b> </th> 
   <th class="entry"> <b> 説明 </b> </th> 
   <th class="entry"> <b> 備考 </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fontbl </span> </td> 
   <td> <p>フォントテーブル。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>フォント <i>N</i> の文字セット。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGBカラーテーブル。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>CMYK カラーテーブル。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>画像サービングカラーのカラーテーブル。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。<span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>赤の色コンポーネント。 </p> </td> 
   <td> <p>\colortbl </span>; 0...255<span class="codeph"> のみ使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span> </span> </td> 
   <td> <p>緑色コンポーネント。 </p> </td> 
   <td> <p>\colortbl </span>; 0...255<span class="codeph"> のみ使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span> </span> </td> 
   <td> <p>青の色コンポーネント。 </p> </td> 
   <td> <p>\colortbl </span>; 0...255<span class="codeph"> のみ使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span> </span> </td> 
   <td> <p>シアンの色コンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。\cmykcolortbl </span>; 0...100<span class="codeph"> のみ表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>マゼンタ色のコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。\cmykcolortbl </span>; 0...100<span class="codeph"> のみ表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow <span class="varname"> N </span> </span> </td> 
   <td> <p>黄色のカラーコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。\cmykcolortbl </span>; 0...100<span class="codeph"> のみ表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \黒 <span class="varname"> N </span> </span> </td> 
   <td> <p>黒のカラーコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。\cmykcolortbl </span>; 0...100<span class="codeph"> のみ表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>左余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span> </span> </td> 
   <td> <p>右余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>上余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>下余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>テキストボックス内のテキストを上揃えにします。 </p> </td> 
   <td> <p>初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>テキストボックス内のテキストを下揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>テキスト ボックスのテキストを中央に配置します。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>テキストのフローの向き。 </p> </td> 
   <td> <p>言語固有のテキストフロー。<span class="codeph"> textPs= </span> only 0 （デフォルト）左 – 右、上 – 下（ヨーロッパ） 1 上 – 下、右 – 左（極東） </p> </td> 
  </tr> 
 </tbody> 
</table>
