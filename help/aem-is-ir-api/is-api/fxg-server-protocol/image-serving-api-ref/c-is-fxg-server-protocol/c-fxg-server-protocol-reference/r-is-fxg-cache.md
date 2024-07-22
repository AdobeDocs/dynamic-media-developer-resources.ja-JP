---
description: キャッシュコントロール。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と内部キャッシュのキャッシュを選択的に無効にするこ  [!DNL Platform Server]  ができます。
solution: Experience Manager
title: キャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# キャッシュ{#cache}

キャッシュコントロール。 クライアント側キャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と内部 [!DNL Platform Server] キャッシュのキャッシュを選択的に無効にできます。

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

*`cacheControl`* 値を 1 つだけ指定した場合は、クライアントとサーバーの両方のキャッシュに適用されます。

リクエスト属性。 リクエストが返信画像を返さない場合は無視されます。 画像カタログでクライアントサイドのキャッシュが無効になっている場合（`catalog::Expiration` の値が負の場合）、*`clientControl`* は無視されます。

デフォルトは `cache=on,on` です。
