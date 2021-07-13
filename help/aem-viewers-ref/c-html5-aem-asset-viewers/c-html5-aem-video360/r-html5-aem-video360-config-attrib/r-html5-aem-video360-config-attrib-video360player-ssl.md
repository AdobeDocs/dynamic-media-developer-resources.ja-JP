---
description: ビデオ360ビューアの設定属性。
solution: Experience Manager
title: Video360Player.ssl
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: 44efa378-c911-4449-8a10-61212d4392c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 4%

---

# Video360Player.ssl{#video-player-ssl}

ビデオ360ビューアの設定属性。

>[!NOTE]
>
>この設定属性は、[機能パックNPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)がインストールされたAEM 6.2と、[機能パックNPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)がインストールされたAEM 6.1にのみ適用されます。

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

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

[セキュアビデオ配信](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27)も参照してください。
