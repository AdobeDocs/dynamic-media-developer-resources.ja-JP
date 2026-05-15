---
description: 置換変数は、リクエスト URLからサーバーに保存されたFXG テンプレートに値を転送するために使用されます。
solution: Experience Manager
title: 置換変数
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 0%

---

# 置換変数{#substitution-variables}

置換変数は、リクエスト URLからサーバーに保存されたFXG テンプレートに値を転送するために使用されます。

` $ *`var`*= *`値`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">値</span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

* 変数の定義と参照は、リクエスト URLのクエリ部分で発生する場合があります。
* 変数は、他のIS コマンドと同様に上記のように定義されます。先頭の&#39;$&#39;は、コマンドを変数定義として識別します。
* 変数名`*`var`*`は大文字と小文字を区別し、任意の文字、数字、「 – 」、「_」の組み合わせで構成できます。
* 重要な値は、安全なHTTP送信のためにシングルパス URL エンコードにする必要があります。
