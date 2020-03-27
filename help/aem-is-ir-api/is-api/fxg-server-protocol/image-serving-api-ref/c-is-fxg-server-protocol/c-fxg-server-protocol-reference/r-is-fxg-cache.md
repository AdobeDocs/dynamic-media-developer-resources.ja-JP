---
description: キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。
seo-description: キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。
seo-title: キャッシュ
solution: Experience Manager
title: キャッシュ
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

キャッシュ制御。 クライアント側のキャッシュ（ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）と、内部のプラットフォームサーバーキャッシュのキャッシュを選択的に無効にできます。

`&cache= *`cacheControl`*`

`&cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> cacheControl <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> clientControl <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> serverControl <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

値が1つだけ指定さ *`cacheControl`* れた場合、クライアントキャッシュとサーバーキャッシュの両方に適用されます。

リクエスト属性。 要求が返信画像を返さない場合は無視されます。 *`clientControl`* は、画像カタログでクライアント側のキャッシュが無効な場合（負の値の場合） `catalog::Expiration` は無視されます。

Defaults to `cache=on,on`.
