---
description: 次の段落書式コマンドがサポートされています。
solution: Experience Manager
title: 段落書式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
TQID: 'https://experienceleague.adobe.com/bksi7t36irm8XQqI0LtJl3kNaSCZANRzbCKf80o-eNM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# 段落書式{#paragraph-formatting}

次の段落書式コマンドがサポートされています。

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>コマンド </p> </th> 
   <th class="entry"> <p>説明 </p> </th> 
   <th class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>段落書式をデフォルトにリセットします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>テキストの左揃え。 </p> </td> 
   <td> <p>デフォルト： </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>テキストを右揃えにする： </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>テキストを水平方向に中央に配置します。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>テキストを水平方向に揃える </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>段落の最後の行を左揃えにします。 </p> </td> 
   <td> <p>既定；<span class="codeph"> textPs= </span>のみ；<span class="codeph"> \qj </span>がアクティブでない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>両端揃え段落の最終行を右揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ、<span class="codeph"> \qj </span>がアクティブでない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>両端揃え段落の最後の行を中央揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ、<span class="codeph"> \qj </span>がアクティブでない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>均等配置された段落の最後の行を均等配置（伸縮）します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span>のみ、<span class="codeph"> \qj </span>がアクティブでない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>1行目のインデント。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>左インデント。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>右インデント： </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>行間のスペース。 </p> </td> 
   <td> <p>自動行間隔の場合は0 （デフォルト）、デフォルトの行間隔より大きい場合にのみ値を使用する場合は正の値、行間隔を強制する場合は負の値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>行間の複数のフラグ。 </p> </td> 
   <td> <p><span class="codeph"> \sl </span>がtwipsの場合は0 （デフォルト）に、<span class="codeph"> \sl </span>がデフォルトの間隔の倍数の場合は1に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>段落の前に余分なスペースを追加します。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>はテキストボックスの最初の段落に<span class="codeph"> \sb </span>を適用しますが、<span class="codeph"> textPs= </span>は適用しません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>段落後の余白。 </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>は、テキストボックスの最後の段落に<span class="codeph"> \sa </span>を適用しますが、<span class="codeph"> textPs= </span>は適用しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>
