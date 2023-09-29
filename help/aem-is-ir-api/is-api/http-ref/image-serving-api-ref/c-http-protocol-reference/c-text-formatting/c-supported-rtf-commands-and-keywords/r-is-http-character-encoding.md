---
title: 文字エンコーディング
description: 文字のエンコードには、次のコマンドを使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# 文字エンコーディング{#character-encoding}

文字のエンコードには、次のコマンドを使用します。

<table id="table_EB0C1B674BEA4A37964FB4BF559E0005"> 
 <thead> 
  <tr> 
   <th class="entry"> コマンド </th> 
   <th class="entry"> 説明 </th> 
   <th class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph">\`<span class="varname"> HH</span></span> </td> 
   <td> <p>1 つの 8 ビット文字。 </p> </td> 
   <td> <p><span class="varname"> HH</span> は、2 桁の 16 進値である必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\u<span class="varname"> N</span></span> </td> 
   <td> <p>単一の Unicode 文字。 </p> </td> 
   <td> <p><span class="varname"> N</span> は 2 バイトの符号付き整数なので、32767より大きい Unicode 値は負の数で表す必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\uc<span class="varname"> N</span></span> </td> 
   <td> <p>Unicode 文字サイズ。 </p> </td> 
   <td> <p>指定された Unicode 文字に対応するバイト数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch </span> </td> 
   <td> <p>低 ANSI 領域からの文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \wich </span> </td> 
   <td> <p>ANSI の大きい領域の文字。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch </span> </td> 
   <td> <p>全角文字が後に続きます。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
