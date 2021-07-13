---
description: 次の段落書式設定コマンドがサポートされています。
solution: Experience Manager
title: 段落の書式設定
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# 段落の書式設定{#paragraph-formatting}

次の段落書式設定コマンドがサポートされています。

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>段落書式をデフォルトにリセットします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>テキストを左揃えにします。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>テキストを右揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>テキストを水平方向に中央揃えします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>テキストを水平方向に揃えます。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>段落の最後の行を左揃えにします。 </p> </td> 
   <td> <p>デフォルト；<span class="codeph"> textPs= </span>のみ；<span class="codeph"> \qj </span>がアクティブでない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>両端揃えされた段落の最後の行を右揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ；\qjがアク <span class="codeph"> ティブで </span> ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>均等配置された段落の最後の行を中央揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ；\qjがアク <span class="codeph"> ティブで </span>ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>均等配置された段落の最後の行を停止（拡大）します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ；\qjがアク <span class="codeph"> ティブで </span>ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>1行目のインデント </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>左インデント。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>右インデント。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> textPs= </span>のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行間の間隔。 </p> </td> 
   <td> <p>自動行間の場合は0 （デフォルト）。正の値を指定すると、デフォルトの行間隔より大きい場合にのみ値が使用されます。負の値に設定すると、間隔が強制的に調整されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>行間の複数のフラグ。 </p> </td> 
   <td> <p><span class="codeph"> \sl </span>がtwipsの場合は0（デフォルト）に、<span class="codeph"> \sl </span>がデフォルトの間隔の倍数の場合は1に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落の前に余分なスペース。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> text= </span>は、テキストボックスの最初の段落に<span class="codeph"> \sb </span>を適用します。<span class="codeph"> textPs= </span>は適用しません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>段落後の余分なスペース。 </p> </td> 
   <td> <p>Twips;<span class="codeph"> text= </span>は、テキストボックスの最後の段落に<span class="codeph"> \sa </span>を適用します。 <span class="codeph"> textPs= </span>は適用しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>
