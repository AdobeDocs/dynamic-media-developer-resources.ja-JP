---
description: テキストボックスでは、次のドキュメントプロパティがサポートされています。
solution: Experience Manager
title: ドキュメント（テキストボックス）のプロパティ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---

# ドキュメント（テキストボックス）のプロパティ{#document-text-box-properties}

テキストボックスでは、次のドキュメントプロパティがサポートされています。

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>コマンド</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>フォントテーブル </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>フォント<i>N</i>の文字セット。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>RGBカラーテーブル </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykortbl  </span> </td> 
   <td> <p>CMYKカラーテーブル。 </p> </td> 
   <td> <p>Dynamic Media拡張機能。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>画像サービングのカラーテーブル </p> </td> 
   <td> <p>Dynamic Media拡張機能<span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>赤のカラーコンポーネント。 </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>のみで使用できます。0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>緑のカラーコンポーネント。 </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>のみで使用できます。0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>青のカラーコンポーネント。 </p> </td> 
   <td> <p><span class="codeph"> \colortbl </span>のみで使用できます。0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>シアン色のコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能は、 <span class="codeph"> \cmykcolortbl </span>のみで使用できます。0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>マゼンタのカラーコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能は、 <span class="codeph"> \cmykcolortbl </span>のみで使用できます。0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>黄色のカラーコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能は、 <span class="codeph"> \cmykcolortbl </span>のみで使用できます。0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>黒のカラーコンポーネント。 </p> </td> 
   <td> <p>Dynamic Media拡張機能は、 <span class="codeph"> \cmykcolortbl </span>のみで使用できます。0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左余白。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右マージン。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>上余白。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>下余白。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>テキストボックスのテキストを上揃えにします。 </p> </td> 
   <td> <p>初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>テキストボックス内のテキストを下揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>テキストボックスを中央揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>テキストのフローの方向 </p> </td> 
   <td> <p>言語固有のテキストフロー<span class="codeph"> textPs= </span>のみ0（デフォルト）左右、上下（ヨーロッパ） 1上下、右左（極東） </p> </td> 
  </tr> 
 </tbody> 
</table>
