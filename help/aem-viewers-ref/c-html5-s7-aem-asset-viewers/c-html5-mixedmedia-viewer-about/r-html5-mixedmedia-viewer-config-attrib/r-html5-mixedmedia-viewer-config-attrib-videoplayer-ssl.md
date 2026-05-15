---
title: VideoPlayer.ssl
description: 混在メディアビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
TQID: 'https://experienceleague.adobe.com/Vf2-JtHlTsRIPhFUWVFm6NoeZnYgkc1LUcvx-r-JiPQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# VideoPlayer.ssl{#videoplayer-ssl}

混在メディアビデオビューアの設定属性。

<!--
 >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).
-->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">自動|</span> </p> </td> 
   <td colname="col2"> <p> ビデオが安全なSSL接続（HTTPS）または安全でない接続（HTTP）を介して配信されるかどうかを制御します。 </p> <p><span class="codeph"> auto</span>に設定すると、ビデオ配信プロトコルは埋め込みweb ページのプロトコルから継承されます。 web ページがHTTPS経由で読み込まれる場合、ビデオもHTTPS経由で配信され、逆に配信されます。 web ページがHTTP上にある場合、ビデオはHTTP経由で配信されます。 </p> <p></span>で<span class="codeph">に設定すると、ビデオ配信は常にWeb ページプロトコルに関係なく、安全な接続を通じて行われます。 </p> <p>公開済みのビデオ配信のみに影響し、作成者モードでのビデオプレビューでは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

[&#x200B; セキュアビデオ配信](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)も参照してください。
