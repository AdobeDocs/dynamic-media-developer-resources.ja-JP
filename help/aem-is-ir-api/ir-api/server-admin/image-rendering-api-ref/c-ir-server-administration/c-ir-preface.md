---
description: このドキュメントでは、サーバー管理の問題と、Dynamic Media画像レンダリングの設定について説明します。
solution: Experience Manager
title: サーバー管理の概要
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 65fc3510-3d47-4650-bf89-322b517dc004
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# サーバー管理の概要{#server-administration-preface}

このドキュメントでは、サーバー管理の問題と、Dynamic Media画像レンダリングの設定について説明します。

**対象オーディエンス**

このドキュメントは、Dynamic Media画像レンダリングのインストール、設定および管理を必要とするシステム管理者および web マスターを対象としています。

**ドキュメント規則**

このドキュメントで説明されている項目は、多くの場合、次の項目タイプのプレフィックスが付いています。

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>attribute::Item </p></td> 
  <td class="stentry"> <p>先頭に「attribute::」が付く名前は、画像カタログ属性を参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>カタログ：：項目 </p></td> 
  <td class="stentry"> <p>先頭に「catalog::」が付いた名前は、材料カタログデータフィールドを指します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>icc::Item </p></td> 
  <td class="stentry"> <p>先頭に「icc::」が付いた名前は、ICC カラープロファイルマップのフィールドを参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>マクロ：：項目 </p></td> 
  <td class="stentry"> <p>「macro::」というプレフィックスが付いた名前は、マクロ定義テーブルのフィールドを指します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ルールセット：:Item </p></td> 
  <td class="stentry"> <p>プレフィックス「ruleset::」が付いた名前は、URL 内の要素を前処理ルールセットとして参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>default::Item </p></td> 
  <td class="stentry"> <p>先頭に「default::」が付く名前は、デフォルトの画像カタログの属性を参照します。 </p></td> 
 </tr> 
</table>
