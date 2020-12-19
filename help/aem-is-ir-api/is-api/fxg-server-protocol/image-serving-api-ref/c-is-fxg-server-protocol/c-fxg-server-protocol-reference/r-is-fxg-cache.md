---
description: キャッシュ制御 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュ内のキャッシュを選択的に無効にできます。
seo-description: キャッシュ制御 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュ内のキャッシュを選択的に無効にできます。
seo-title: キャッシュ
solution: Experience Manager
title: キャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# キャッシュ{#cache}

キャッシュ制御 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュ内のキャッシュを選択的に無効にできます。

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

*`cacheControl`*&#x200B;値を1つだけ指定した場合、その値はクライアントとサーバーの両方のキャッシュに適用されます。

要求属性。 要求が返信画像を返さない場合は無視されます。 *`clientControl`* は、画像カタログでクライアント側のキャッシュが無効な場合(負の値 `catalog::Expiration` の場合)は無視されます。

デフォルトは`cache=on,on`です。
