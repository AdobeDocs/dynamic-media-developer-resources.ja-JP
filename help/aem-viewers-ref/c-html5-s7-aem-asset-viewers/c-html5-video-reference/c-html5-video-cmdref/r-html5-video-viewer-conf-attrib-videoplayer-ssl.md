---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 969da9ea-c97c-4fa8-9207-21d6302609e5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 2%

---


# VideoPlayer.ssl{#videoplayer-ssl}

ビデオビューアの設定属性。

>[!NOTE]
>
>この設定属性は、[Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)がインストールされているAEM 6.2と、[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)がインストールされているAEM 6.1にのみ適用されます。

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> ビデオを安全なSSL接続(HTTPS)または安全でない接続(HTTP)のどちらで配信するかを制御します。 </p> <p><span class="codeph"> auto</span>に設定すると、ビデオ配信プロトコルは埋め込みWebページのプロトコルから継承されます。 WebページがHTTPS経由で読み込まれる場合、ビデオはHTTPS経由でも配信されます。ビデオページがHTTPS経由で読み込まれる場合も同様です。 WebページがHTTP上にある場合、ビデオはHTTP経由で配信されます。 </p> <p></span>で<span class="codeph">に設定した場合、ビデオ配信は常に、Webページのプロトコルに関係なく、安全な接続を介して発生します。 </span></p> <p>は、公開されたビデオ配信にのみ影響し、作成者モードのビデオプレビューでは無視されます。 </p> </td> 
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

[セキュアビデオ配信](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff)も参照してください。
