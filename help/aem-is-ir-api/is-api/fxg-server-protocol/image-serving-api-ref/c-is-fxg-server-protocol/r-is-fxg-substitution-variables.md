---
description: 代替変数は、値を要求URLからサーバーに保存されているFXGテンプレートに転送するために使用します。
solution: Experience Manager
title: 代替変数
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# 代替変数{#substitution-variables}

代替変数は、値を要求URLからサーバーに保存されているFXGテンプレートに転送するために使用します。

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

* 変数の定義と参照は、リクエストURLのクエリ部分で発生する場合があります。
* 変数は、他のISコマンドと同様、上記のように定義されます。先頭の「$」は、コマンドが変数定義であることを示します。
* 変数名`*`var`*`は大文字と小文字が区別され、文字、数字、「 — 」、「_」の組み合わせで構成することができます。
* 重要な値は、安全なHTTP送信を実現するために、シングルパスでURLエンコードする必要があります。

