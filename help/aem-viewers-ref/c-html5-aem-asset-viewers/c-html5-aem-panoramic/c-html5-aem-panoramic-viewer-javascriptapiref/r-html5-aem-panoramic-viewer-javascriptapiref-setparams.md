---
title: setParams
description: パノラマビューアの JavaScript API リファレンス。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# setParams{#setparams}

パノラマビューアの JavaScript API リファレンス。

` setParams( *`params`*)`

1 つ以上のパラメータを指定された値に設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、name=value のペアを `&`. クエリ文字列と同様に、名前と値は UTF8 を使用してパーセントでエンコードされます。 電話する前に `init()`に設定する場合は、このパラメーターを呼び出す必要があります。

ビューアの設定情報がで渡された場合は、このメソッドはオプションです。 `config` JSON オブジェクトをコンストラクターに渡します。


## パラメータ {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value パラメーターのペアを区切って指定します。 <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 戻り値 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PanoramicView.fmt=png&PanoramicView.iscommand=op_sharpen%3d1")
```
