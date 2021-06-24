---
description: キャッシュ制御 内部のPlatform Serverキャッシュで、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできます。
solution: Experience Manager
title: キャッシュ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# キャッシュ{#cache}

キャッシュ制御 内部のPlatform Serverキャッシュで、クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）とキャッシュを選択的に無効にできます。

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

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

*`cacheControl`*&#x200B;値を1つだけ指定した場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

リクエスト属性。 要求が返信イメージを返さない場合は無視されます。 *`clientControl`* は、画像カタログでクライアント側のキャッシュが無効な場合(が負の値の場 `catalog::Expiration` 合)は無視されます。

デフォルトは`cache=on,on`です。
