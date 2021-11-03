---
title: HTTP ビデオ配信
description: HTTP ビデオ配信
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# HTTP ビデオ配信{#http-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

この節の最初で説明するようにビューアが設定で動作する場合、公開されたビデオ配信は、HTTPS（セキュア）モードと HTTP（セキュアでない）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込み Web ページの配信プロトコルに厳密に従っています。 ただし、 [SmartCropVideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 設定属性。 （作成者モードのビデオプレビューは、常に HTTPS 経由で安全に配信されます）。

Adobe Experience Managerで使用するDynamic Mediaビデオの公開方法に応じて、 `SmartCropVideoPlayer.ssl` 設定属性の適用方法は、次に示すように異なります。

* URL を含むDynamic Mediaビデオを公開する場合は、「 `SmartCropVideoPlayer.ssl` を URL に追加します。 例えば、セキュアなビデオ配信を強制するには、次の文字列を追加します。 `&SmartCropVideoPlayer.ssl=on` を次のビューア URL の例の最後に追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/SmartCropVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&SmartCropVideoPlayer.ssl=on
   ```

   関連トピック [Web アプリケーションへの URL のリンク](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* 埋め込みコードを含むDynamic Mediaビデオを公開する場合は、 `SmartCropVideoPlayer.ssl` を埋め込みコードスニペット内の他のビューア設定パラメータのリストに追加します。 例えば、HTTPS ビデオ配信を強制するには、 `&SmartCropVideoPlayer.ssl=on` 次の例のようになります。

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.SmartCropVideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "SmartCropVideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   関連トピック [Web ページへのビデオの埋め込み](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
