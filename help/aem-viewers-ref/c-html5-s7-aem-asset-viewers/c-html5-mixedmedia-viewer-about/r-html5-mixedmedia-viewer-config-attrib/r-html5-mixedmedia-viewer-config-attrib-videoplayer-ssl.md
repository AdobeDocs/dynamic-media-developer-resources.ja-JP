---
description: 混在メディアビデオビューアの設定属性。
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5fd3aa39-edb0-4434-aa5f-e511c84cf950
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# VideoPlayer.ssl{#videoplayer-ssl}

混在メディアビデオビューアの設定属性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> ビデオを安全なSSL接続(HTTPS)と安全でない接続(HTTP)のどちらで配信するかを制御します。 </p> <p><span class="codeph"> auto</span>に設定すると、ビデオ配信プロトコルが埋め込みWebページのプロトコルから継承されます。 WebページがHTTPSで読み込まれる場合、ビデオもHTTPSで配信されます。また、WebページがHTTPSで読み込まれる場合も、ビデオがHTTPSで配信されます。 WebページがHTTP上にある場合、ビデオはHTTP経由で配信されます。 </p> <p></span>で<span class="codeph">に設定した場合、ビデオ配信は、Webページのプロトコルに関係なく、常に安全な接続を介しておこなわれます。 </span></p> <p>公開済みのビデオ配信にのみ影響し、オーサーモードのビデオプレビューでは無視されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

[セキュアビデオ配信](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)も参照してください。
