---
description: このドキュメントでは、サーバー管理の問題を説明し、Scene7イメージレンダリングの設定について説明します。
seo-description: このドキュメントでは、サーバー管理の問題を説明し、Scene7イメージレンダリングの設定について説明します。
seo-title: サーバー管理のはじめに
solution: Experience Manager
title: サーバー管理のはじめに
topic: Scene7 Image Serving - Image Rendering API
uuid: 182782f1-44a8-421d-bacc-f08dcf95f58b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# サーバ管理のはじめに{#server-administration-preface}

このドキュメントでは、サーバー管理の問題を説明し、Scene7イメージレンダリングの設定について説明します。

**対象オーディエンス**

このドキュメントは、Scene7イメージレンダリングのインストール、設定、管理を必要とするシステム管理者およびWebマスターを対象としています。

**ドキュメント規則**

このドキュメントで説明する項目は、多くの場合、次の項目タイプのプリフィックスが付けられます。

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>attribute::Item </p></td> 
  <td class="stentry"> <p>「attribute::」というプリフィックスの付いた名前は、画像カタログ属性を参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>catalog::Item </p></td> 
  <td class="stentry"> <p>「catalog::」というプリフィックスが付いた名前は、マテリアルカタログデータフィールドを参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>icc::Item </p></td> 
  <td class="stentry"> <p>「icc:」というプリフィックスが付いた名前は、ICCカラープロファイルマップ内のフィールドを参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>macro::Item </p></td> 
  <td class="stentry"> <p>「macro::」というプリフィックスが付いた名前は、マクロ定義テーブル内のフィールドを参照します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>ruleset::Item </p></td> 
  <td class="stentry"> <p>「ruleset::」というプリフィックスが付いた名前は、URLの事前処理ルールセット内の要素を指します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>default::Item </p></td> 
  <td class="stentry"> <p>「default::」というプリフィックスの付いた名前は、初期設定の画像カタログの属性を参照します。 </p></td> 
 </tr> 
</table>

