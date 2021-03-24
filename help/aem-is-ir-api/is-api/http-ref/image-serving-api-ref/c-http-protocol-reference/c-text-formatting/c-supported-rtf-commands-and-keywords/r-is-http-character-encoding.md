---
description: 文字のエンコードには次のコマンドを使用します。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---


# 文字エンコーディング{#character-encoding}

文字のエンコードには次のコマンドを使用します。

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
   <td> <p>8ビット単一文字。 </p> </td> 
   <td> <p><span class="varname"> 2</span> 桁の16進値を指定する必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph">\<span class="varname"> uN</span></span> </td> 
   <td> <p>単一のUnicode文字。 </p> </td> 
   <td> <p><span class="varname"> </span> NISは符号付き2バイトの整数です。したがって、32767より大きいUnicode値は負の数で表す必要があります。 </p> </td> 
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
   <td> <span class="codeph"> \which  </span> </td> 
   <td> <p>高ANSI領域の文字が続きます。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \dbch  </span> </td> 
   <td> <p>重複バイト文字の後に続きます。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

