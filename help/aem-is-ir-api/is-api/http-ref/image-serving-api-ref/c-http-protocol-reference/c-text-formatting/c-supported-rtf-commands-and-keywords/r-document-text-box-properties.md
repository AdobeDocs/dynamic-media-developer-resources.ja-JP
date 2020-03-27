---
description: テキストボックスでは、次のドキュメントプロパティがサポートされています。
seo-description: テキストボックスでは、次のドキュメントプロパティがサポートされています。
seo-title: ドキュメント（テキストボックス）のプロパティ
solution: Experience Manager
title: ドキュメント（テキストボックス）のプロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td> <span class="codeph"> \fontbl </span> </td> 
   <td> <p>フォントテーブル </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span></span> </td> 
   <td> <p>フォント <i>Nの文字セット</i>。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>RGBカラーテーブル </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykortbl </span> </td> 
   <td> <p>CMYKカラーテーブル。 </p> </td> 
   <td> <p>Scene7 Extension。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>画像サービングの色のカラーテーブル。 </p> </td> 
   <td> <p>Scene7 extension; <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span></span> </td> 
   <td> <p>赤の色コンポーネント。 </p> </td> 
   <td> <p>\colortbl内でのみ使用 <span class="codeph"> 可能 </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green <span class="varname"> N </span></span> </td> 
   <td> <p>緑色コンポーネント。 </p> </td> 
   <td> <p>\colortbl内でのみ使用 <span class="codeph"> 可能 </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue <span class="varname"> N </span></span> </td> 
   <td> <p>青色コンポーネント。 </p> </td> 
   <td> <p>\colortbl内でのみ使用 <span class="codeph"> 可能 </span>;0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan <span class="varname"> N </span></span> </td> 
   <td> <p>シアンのカラーコンポーネント。 </p> </td> 
   <td> <p>Scene7 extension;は、 <span class="codeph"> \cmykcolortbl </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span></span> </td> 
   <td> <p>マゼンタのカラーコンポーネント。 </p> </td> 
   <td> <p>Scene7 extension;は、 <span class="codeph"> \cmykcolortbl </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \yellow <span class="varname"> N </span></span> </td> 
   <td> <p>黄色のカラーコンポーネント。 </p> </td> 
   <td> <p>Scene7 extension;は、 <span class="codeph"> \cmykcolortbl </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \黒 <span class="varname"> N </span></span> </td> 
   <td> <p>黒のカラーコンポーネント。 </p> </td> 
   <td> <p>Scene7 extension;は、 <span class="codeph"> \cmykcolortbl </span>;0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span></span> </td> 
   <td> <p>左余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr <span class="varname"> N </span></span> </td> 
   <td> <p>右余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span></span> </td> 
   <td> <p>上余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span></span> </td> 
   <td> <p>下余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>テキストボックス内のテキストの上揃え。 </p> </td> 
   <td> <p>初期設定 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>テキストボックス内のテキストを下揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>テキストボックス内でテキストを中央揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span></span> </td> 
   <td> <p>テキストフローの方向 </p> </td> 
   <td> <p>言語固有のテキストフロー <span class="codeph"> textPs= </span> 0のみ（デフォルト）左右、上下（ヨーロッパ語） 1上下、右左（極東語） </p> </td> 
  </tr> 
 </tbody> 
</table>

