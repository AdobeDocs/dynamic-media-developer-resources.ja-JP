---
title: setParams
description: パノラマビューアのJavaScript API リファレンス。
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
autotag-review: '2026-05-13T22:11:56.850Z'
TQID: 'https://experienceleague.adobe.com/bgl9zea0OpuRZc9HG0VMPpQmJH3Mjdk0jRS47Lu4MDA'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# setParams{#setparams}

パノラマビューアのJavaScript API リファレンス。

` setParams( *` パラメーター`*)`

指定された値に1つ以上のパラメーターを設定します。 メソッド引数の構文は、URL クエリ文字列と同じです。 つまり、`&`で区切られたname=value ペアを表します。 クエリ文字列と同様に、名前と値はUTF8を使用してパーセント エンコードされます。 `init()`を呼び出す前に、このパラメーターを呼び出す必要があります。

ビューア設定情報が`config` JSON オブジェクトでコンストラクターに渡された場合、このメソッドはオプションです。


## パラメータ {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> パラメーター</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value パラメーターのペアが<span class="codeph">および</span>で区切られています。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返品 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

なし

## 例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PanoramicView.fmt=png&PanoramicView.iscommand=op_sharpen%3d1")
```
