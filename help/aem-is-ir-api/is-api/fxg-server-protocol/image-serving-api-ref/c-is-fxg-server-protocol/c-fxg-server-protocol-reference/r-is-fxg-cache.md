---
description: キャッシュ制御： クライアントサイドのキャッシュ （ブラウザー、プロキシサーバー、ネットワークキャッシュシステム）および内部 [!DNL Platform Server]  キャッシュのキャッシュを選択的に無効にできます。
solution: Experience Manager
title: キャッシュ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
TQID: 'https://experienceleague.adobe.com/X6q0OKRjjjpgNxl8XDuzkNBzrzTBS4E5BtXQGuJWgmk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 0%

---

# キャッシュ{#cache}

キャッシュ制御： クライアント側のキャッシュ （ブラウザー、プロキシ サーバー、ネットワーク キャッシュ システム）および内部[!DNL Platform Server] キャッシュのキャッシュを選択的に無効にできます。

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

1つの&#x200B;*`cacheControl`*&#x200B;値のみを指定した場合、クライアントとサーバーの両方のキャッシュに適用されます。

リクエスト属性： リクエストが返信画像を返さない場合は無視されます。 画像カタログによってクライアント側のキャッシュが無効になっている場合、*`clientControl`*&#x200B;は無視されます（`catalog::Expiration`に負の値がある場合）。

デフォルトは`cache=on,on`です。
