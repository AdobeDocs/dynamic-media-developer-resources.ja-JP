---
description: テキストの書式設定には、次の特殊エンティティを使用します。
seo-description: テキストの書式設定には、次の特殊エンティティを使用します。
seo-title: 特殊テキストエンティティ
solution: Experience Manager
title: 特殊テキストエンティティ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: efcc3962-7097-4395-8b9f-f37c6e7f5b75
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---


# 特殊テキストエンティティ{#special-text-entities}

テキストの書式設定には、次の特殊エンティティを使用します。

<table id="table_CFEB845C1B9A475CA52ECDFA9BB59A9D"> 
 <thead> 
  <tr> 
   <th class="entry"> コマンド </th> 
   <th class="entry"> 説明 </th> 
   <th class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \par</span> </td> 
   <td> <p>段落区切り </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ライン </span> </td> 
   <td> <p>改行。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \\  </span> </td> 
   <td> <p>バックスラッシュ。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> &amp;lbrace;  </span> </td> 
   <td> <p>中括弧開き </p> </td> 
   <td> <p>括弧はHTTPエンコードする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> &amp;rbrace;  </span> </td> 
   <td> <p>中括弧。 </p> </td> 
   <td> <p>括弧はHTTPエンコードする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \～  </span> </td> 
   <td> <p>区切りなしスペース。 </p> </td> 
   <td> <p><span class="codeph"> textPs=</span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \_</span> </td> 
   <td> <p>改行しないハイフン。 </p> </td> 
   <td> <p><span class="codeph"> textPs=</span> only. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \-  </span> </td> 
   <td> <p>オプションのハイフン。 </p> </td> 
   <td> <p><span class="codeph"> textPs=</span> only. </p> </td> 
  </tr> 
 </tbody> 
</table>

