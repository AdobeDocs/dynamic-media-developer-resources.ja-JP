---
description: 次のコマンドを使用して、文字をエンコードします。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: a03f08f7-e9cc-458f-9ff0-7721f1dbc4cc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# 文字エンコーディング{#character-encoding}

次のコマンドを使用して、文字をエンコードします。

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
   <td> <span class="codeph">\'<span class="varname"> HH</span></span> </td> 
   <td> <p>単一の8ビット文字。 </p> </td> 
   <td> <p><span class="varname"> </span> は、2桁の16進値である必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>単一のUnicode文字。 </p> </td> 
   <td> <p><span class="varname"> </span> Nisには符号付き2バイト整数を指定します。したがって、32767より大きいUnicode値は負の数で表す必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> ucN</span></span> </td> 
   <td> <p>Unicode文字サイズ。 </p> </td> 
   <td> <p>指定したUnicode文字に対応するバイト数。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \loch  </span> </td> 
   <td> <p>低ANSI領域の文字が続きます。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \hich  </span> </td> 
   <td> <p>高ANSI領域の文字が続きます。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>2バイト文字が続きます。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>
