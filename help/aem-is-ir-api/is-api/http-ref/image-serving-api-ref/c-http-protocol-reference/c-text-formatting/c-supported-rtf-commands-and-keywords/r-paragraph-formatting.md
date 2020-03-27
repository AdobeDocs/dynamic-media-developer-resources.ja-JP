---
description: 次の段落の書式設定コマンドがサポートされています。
seo-description: 次の段落の書式設定コマンドがサポートされています。
seo-title: 段落の書式設定
solution: Experience Manager
title: 段落の書式設定
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 段落の書式設定{#paragraph-formatting}

次の段落の書式設定コマンドがサポートされています。

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
   <td> <p>段落の書式をデフォルトにリセットします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>テキストを左揃えにします。 </p> </td> 
   <td> <p>初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>テキストを右揃えにします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>テキストを水平方向に中央揃えします。 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>テキストを水平方向に均等配置します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>段落の最後の行を左揃えにします。 </p> </td> 
   <td> <p>デフォルト； <span class="codeph"> textPs= </span> のみ；\qjがアクテ <span class="codeph"> ィブで </span>ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>両端揃えされた段落の最後の行を右揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み；\qjがアクテ <span class="codeph"> ィブでな </span> い場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>両端揃えされた段落の最後の行を中央揃えにします。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み；\qjがアクテ <span class="codeph"> ィブで </span>ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>均等配置された段落の最後の行を停止（拡大）します。 </p> </td> 
   <td> <p> <span class="codeph"> textPs=の </span> み；\qjがアクテ <span class="codeph"> ィブで </span>ない場合は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span></span> </td> 
   <td> <p>1行目のインデント。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span></span> </td> 
   <td> <p>左インデント。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span></span> </td> 
   <td> <p>右インデント。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> textPs=の </span> み。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span></span> </td> 
   <td> <p>行間のスペース。 </p> </td> 
   <td> <p>0（デフォルト）は自動行間。正の値を指定すると、デフォルトの行間隔よりも大きい場合にのみ値が使用されます。負の値を指定すると、間隔が強制的に調整されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span></span> </td> 
   <td> <p>行間の複数のフラグ。 </p> </td> 
   <td> <p>\slがtwip単位の場合は0（デフォルト）に設定し、 <span class="codeph"> \slがデフォルトの間隔の倍数に </span> なる場 <span class="codeph"></span> 合は1に設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span></span> </td> 
   <td> <p>段落前の余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> text=は、テキ </span>ストボックス <span class="codeph"> の最初の段落に </span> \sbを適用し <span class="codeph"> ます。textPs=は適用さ </span> れません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span></span> </td> 
   <td> <p>段落後の余白。 </p> </td> 
   <td> <p>Twip; <span class="codeph"> text=は、テ </span> キストボ <span class="codeph"> ックス </span> の最後の段落に¥saを適用し <span class="codeph"> ます。textPs=は適 </span> 用しません。 </p> </td> 
  </tr> 
 </tbody> 
</table>

