---
title: SmartCropVideoPlayer.ssl
description: スマート切り抜きビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# SmartCropVideoPlayer.ssl{#smartcropvideoplayer-ssl}

スマート切り抜きビデオビューアの設定属性。

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[SmartCropVideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> ビデオを安全な SSL 接続 (HTTPS) と安全でない接続 (HTTP) のどちらで配信するかを制御します。 </p> <p>に設定する場合 <span class="codeph"> auto</span> ビデオ配信プロトコルは、埋め込み web ページのプロトコルから継承されます。 Web ページが HTTPS で読み込まれる場合、ビデオは HTTPS でも（逆も）配信されます。 Web ページが HTTP 上にある場合、ビデオは HTTP 経由で配信されます。 </p> <p>に設定する場合 <span class="codeph"> オン</span>の場合、ビデオ配信は、Web ページのプロトコルに関係なく、常に安全な接続を介しておこなわれます。 </p> <p>公開されたビデオ配信にのみ影響し、オーサーモードのビデオプレビューでは無視されます。 </p> </td> 
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

関連トピック [ビデオ配信を保護](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-securevideodelivery.md#concept-cf9d1346a07d4429b0c6c32c9cac50ff).
