---
description: キャッシュ制御。 内部で、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできる [!DNL Platform Server] キャッシュ。
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

キャッシュ制御。 内部で、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできる [!DNL Platform Server] キャッシュ。

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

1 つのみの場合 *`cacheControl`* 値を指定した場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

要求属性。 リクエストが返信画像を返さない場合は無視されます。 *`clientControl`* は、画像カタログでクライアント側のキャッシュが無効になっている場合は無視されます ( `catalog::Expiration` は負の値です )。

デフォルトはです。 `cache=on,on`.
