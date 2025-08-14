---
description: 次の段落書式設定コマンドがサポートされています。
solution: Experience Manager
title: 段落書式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 段落書式{#paragraph-formatting}

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
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>段落書式を既定値にリセットします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>テキストを左揃えにします。 </p> </td> 
   <td> <p>デフォルト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>テキストを右揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>テキストを水平方向の中央に配置します。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>テキストを水平方向に揃えます。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>段落の最後の行を左揃えにします。 </p> </td> 
   <td> <p>デフォルト。<span class="codeph"> textPs= </span> のみ。\qj <span class="codeph"> がアクティブ </span> ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>両端揃えの段落の最後の行を右揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。\qj <span class="codeph"> がアクティブでない場合 </span> 無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>両端揃え段落の最後の行を中央揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。\qj <span class="codeph"> がアクティブ </span> ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>両端揃えの段落の最後の行を固定（ストレッチ）します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs= </span> のみ。\qj <span class="codeph"> がアクティブ </span> ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>1 行目のインデント。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>左インデント。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>右インデント </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs= </span> のみ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>行と行の間のスペース </p> </td> 
   <td> <p>自動行間を設定する場合は 0 （デフォルト）、デフォルトの行間より大きい場合は値のみを使用する場合は正の値、行間を強制的に設定する場合は負の値を使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>行間隔の複数フラグ。 </p> </td> 
   <td> <p>\sl <span class="codeph"> が twip の場合 </span>0 （デフォルト）、\sl <span class="codeph"> がデフォルトの間隔の倍数の場合 </span>1 に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>段落の前の余分なスペース。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> text= </span>\sb <span class="codeph"></span> テキストボックスの最初の段落に適用されます <span class="codeph">、textPs= </span> は適用されません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>段落の後の余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> text= </span> は\sa <span class="codeph"></span> テキストボックスの最後の段落に適用されます <span class="codeph">、textPs= </span> は適用されません。 </p> </td> 
  </tr> 
 </tbody> 
</table>
