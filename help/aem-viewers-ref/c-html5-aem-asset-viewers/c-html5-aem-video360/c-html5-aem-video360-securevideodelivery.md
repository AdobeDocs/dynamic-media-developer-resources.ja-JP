---
title: HTTPS ビデオ配信
description: HTTPS ビデオ配信
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# HTTPS ビデオ配信{#https-video-delivery}

<!-- >[!NOTE]
>
>HTTP Secure Video Delivery applies only to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

この節の最初で説明したように、ビューアが設定で動作する場合、公開済みのビデオ配信は、HTTPS（セキュア）モードと HTTP（セキュアでない）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込み Web ページの配信プロトコルに厳密に従います。 ただし、[Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) 設定属性を使用して Web ページを埋め込むことで、使用するプロトコルに関係なく、HTTPS ビデオ配信を強制できます。 （オーサーモードのビデオプレビューは、常に HTTPS 経由で安全に配信されます）。

Adobe Experience Managerで使用するDynamic Mediaビデオの公開方法に応じて、次に示すように、`Video360Player.ssl` 設定属性の適用方法は異なります。

* URL を含むDynamic Mediaビデオを公開する場合は、URL に `Video360Player.ssl` を追加します。 例えば、ビデオのセキュリティを強制的に保護するには、次のビューア URL の例の最後に `&Video360Player.ssl=on` を追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   [Web アプリケーションへの URL のリンク ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic) も参照してください。

* 埋め込みコードを含むDynamic Mediaビデオを公開する場合は、埋め込みコードスニペット内の他のビューア設定パラメーターのリストに `Video360Player.ssl` を追加します。 例えば、HTTPS ビデオ配信を強制するには、次の例のように `&Video360Player.ssl=on` を追加します。

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
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

   [Web ページへのビデオの埋め込み ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic) も参照してください。
