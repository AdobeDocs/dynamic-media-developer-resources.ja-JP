---
description: 混在メディアビデオビューアの設定属性。
seo-description: 混在メディアビデオビューアの設定属性。
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 07e2c55b-2388-44c8-83ab-338997c5cb71
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# VideoPlayer.ssl{#videoplayer-ssl}

混在メディアビデオビューアの設定属性。

>[!NOTE]
>
>この設定属性は、 [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) がインストールされているAEM 6.2と、 [Feature Pack NPR-15011がインストールされているAEM 6.1にのみ適用されます](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)。

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> ビデオを安全なSSL接続(HTTPS)または安全でない接続(HTTP)のどちらで配信するかを制御します。 </p> <p>autoに設定すると <span class="codeph"></span> 、ビデオ配信プロトコルは埋め込みWebページのプロトコルから継承されます。 WebページがHTTPS経由で読み込まれる場合、ビデオはHTTPS経由でも配信され、逆も同様です。 WebページがHTTP上にある場合、ビデオはHTTP経由で配信されます。 </p> <p>onに設定すると、ビ <span class="codeph"> デオ配信は</span>、Webページのプロトコルに関係なく、常に安全な接続を介して行われます。 </p> <p>発行されたビデオ配信にのみ影響し、作成者モードでのビデオプレビューでは無視されます。 </p> </td> 
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

セキュアビデオ配 [信も参照してください](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb)。
