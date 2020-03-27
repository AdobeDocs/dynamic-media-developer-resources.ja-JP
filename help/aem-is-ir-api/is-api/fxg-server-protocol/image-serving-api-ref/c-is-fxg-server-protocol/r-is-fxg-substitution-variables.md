---
description: 代替変数は、値を要求URLからサーバーに保存されているFXGテンプレートに転送するために使用されます。
seo-description: 代替変数は、値を要求URLからサーバーに保存されているFXGテンプレートに転送するために使用されます。
seo-title: 代替変数
solution: Experience Manager
title: 代替変数
topic: Scene7 Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 代替変数{#substitution-variables}

代替変数は、値を要求URLからサーバーに保存されているFXGテンプレートに転送するために使用されます。

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>変数名。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 価 </span> 値 </span> </p> </td> 
  <td class="stentry"> <p>変数を設定する値（文字列）。 </p> </td> 
 </tr> 
</table>

* 変数の定義と参照は、リクエストURLのクエリー部分で発生する場合があります。
* 変数は、他のISコマンドと同様に、上記のように定義されます。先頭の「$」は、コマンドを変数定義として識別します。
* 変数名 ` *`varは`*` 、大文字と小文字が区別され、英数字、「 — 」、「_」の任意の組み合わせで構成できます。
* 重要な値は、安全なHTTP送信を実現するために、シングルパスURLエンコードする必要があります。

