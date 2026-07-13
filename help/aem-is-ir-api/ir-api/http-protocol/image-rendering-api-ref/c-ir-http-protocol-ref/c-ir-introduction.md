---
title: はじめに
description: このドキュメントでは、Dynamic Media Image RenderingのHTTP プロトコルについて説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
TQID: 'https://experienceleague.adobe.com/I21iWFmYP0Vwunf3evtnLAr3tslHOsTOB0sGWG6l-bc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 387
ht-degree: 0%

---

# はじめに{#introduction}

このドキュメントでは、Dynamic Media Image RenderingのHTTP プロトコルについて説明します。

プロトコルの一般公開されている側面のみが記載されています。 サーバーは、Dynamic Media クライアントソフトウェアで使用するために予約された追加コマンドをサポートする場合があります。

**対象オーディエンス**

このドキュメントは、Web サイトまたはカスタムアプリケーションにDynamic Media画像レンダリングを使用したい経験豊富なプログラマーおよびWeb サイト開発者を対象としています。

読者は、Dynamic Mediaの画像オーサリングと画像レンダリング、一般的なHTTP プロトコルの標準と規則、基本的な画像用語に精通していることを前提としています。

**ドキュメント規則**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>リテラル </p> </td> 
  <td class="stentry"> <p>構文セクションでは、イタリック以外のテキストはリテラルです。空白や記号[ ] { } | *には適用されません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'リテラル' </p> </td> 
  <td class="stentry"> <p>記述的なセクションでは、単引用符の非イタリックのテキストはリテラルです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> パラメーター</span> </p> </td> 
  <td class="stentry"> <p>斜体は、実際の値で置き換える変数またはパラメーターを示します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">属性：：項目</span> </p> </td> 
  <td class="stentry"> <p>「attribute::」が付いた名前は、画像カタログ属性を表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> カタログ：：項目</span> </p> </td> 
  <td class="stentry"> <p>「catalog::」が付いた名前は、マテリアルカタログデータフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc:：項目</span> </p> </td> 
  <td class="stentry"> <p>「icc:::」というプレフィックスが付いた名前は、ICC カラープロファイルマップのフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> マクロ：：項目</span> </p> </td> 
  <td class="stentry"> <p>「macro::」というプレフィックスが付いた名前は、マクロ定義テーブルのフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ルールセット：：項目</span> </p> </td> 
  <td class="stentry"> <p>「ruleset:::」というプレフィックスが付いた名前は、URL前処理ルールセット内の要素を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">の既定値：：項目</span> </p> </td> 
  <td class="stentry"> <p>「default::」というプレフィックスが付いた名前は、デフォルトの画像カタログの属性を指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> ビネット：：項目</span> </td> 
  <td class="stentry"> <p>「周辺光量補正：:」というプレフィックスが付いた名前は、周辺光量補正マップ内のフィールドを指します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> optional </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文エレメントは、角括弧で囲まれます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[<span class="varname"> オプション </span> ] </p> </td> 
  <td class="stentry"> <p>オプションの構文エレメントは、何度も繰り返すことはできません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>縦棒グラフは、左側の単一の構文項目または右側の項目のいずれかを使用できることを示します。 1つの項目を選択してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>中括弧は、構文エレメントをグループ化するために使用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> グループ </span> } </p> </td> 
  <td class="stentry"> <p>グループ内の構文要素は、1回以上繰り返すことができます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>空白 </p> </td> 
  <td class="stentry"> <p>HTTP リクエストでは、空白（スペースまたはタブ）は使用できません。 このドキュメントでは、構文要素の間に空白が表示されることがあります。 </p> </td> 
 </tr> 
</table>

**一般的な用語**

** *`MSS`* ** Material Specification Segment: リクエスト内の2つの選択コマンド間のマテリアル属性のセット。

** *`vignette`* ** Dynamic Mediaの画像オーサリングで、画像レンダリングで使用するために準備された画像。

