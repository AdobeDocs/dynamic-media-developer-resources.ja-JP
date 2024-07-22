---
description: 代替変数は、リクエスト URL の値を、サーバーに保存されている FXG テンプレートに転送するために使用されます。
solution: Experience Manager
title: 代替変数
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# 代替変数{#substitution-variables}

代替変数は、リクエスト URL の値を、サーバーに保存されている FXG テンプレートに転送するために使用されます。

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 値 </span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

* 変数の定義と参照は、リクエスト URL のクエリ部分で使用できます。
* 変数は、他の IS コマンドと同様に、上記のように定義されます。先頭の「$」は、コマンドを変数定義として識別します。
* 変数名 `*`var`*` は大文字と小文字が区別され、文字、数字、「–」、「_」の任意の組み合わせで構成されます。
* 安全な HTTP 送信を行うには、重要な値をシングルパス URL でエンコードする必要があります。
