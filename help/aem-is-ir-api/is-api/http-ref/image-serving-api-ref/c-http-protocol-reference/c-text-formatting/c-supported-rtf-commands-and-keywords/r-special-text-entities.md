---
description: テキストの書式設定には、次の特殊なエンティティを使用します。
solution: Experience Manager
title: 特殊テキストエンティティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3798dd83-897a-441c-a7c4-ef7325b20f16
TQID: 'https://experienceleague.adobe.com/WkEyXKu8K2l9NFlwZWsXE-NC8xJRNPEUdKijo58bagE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 2%

---

# 特殊テキストエンティティ{#special-text-entities}

テキストの書式設定には、次の特殊なエンティティを使用します。

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
   <td> <p>段落区切り。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \line </span> </td> 
   <td> <p>改行： </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \\ </span> </td> 
   <td> <p>バックスラッシュ。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> &amp;brace; </span> </td> 
   <td> <p>中括弧を開きます。 </p> </td> 
   <td> <p>中括弧はHTTP エンコードする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> &amp;rbrace; </span> </td> 
   <td> <p>中括弧を閉じます。 </p> </td> 
   <td> <p>中括弧はHTTP エンコードする必要があります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \~ </span> </td> 
   <td> <p>区切り不要のスペース </p> </td> 
   <td> <p><span class="codeph"> textPs=</span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \_</span> </td> 
   <td> <p>改行なしハイフン。 </p> </td> 
   <td> <p><span class="codeph"> textPs=</span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \- </span> </td> 
   <td> <p>オプションのハイフン： </p> </td> 
   <td> <p><span class="codeph"> textPs=</span>のみ。 </p> </td> 
  </tr> 
 </tbody> 
</table>
