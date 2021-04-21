---
description: HTTPSビデオ配信
solution: Experience Manager
title: HTTPSビデオ配信
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 0%

---

# HTTPSビデオ配信{#https-video-delivery}

>[!NOTE]
>
>HTTPセキュアビデオ配信は、[機能パック —13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)のインストールが有効なAEM 6.2と、[機能パックNPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)のインストールが有効なAEM 6.1にのみ適用されます。

この節の最初に説明するように、ビューアが設定で動作する場合、公開されたビデオの配信は、HTTPS（セキュア）モードとHTTP（セキュア）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みWebページの配信プロトコルに厳密に従います。 ただし、[Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md)設定属性を使用してWebページを埋め込むと、使用するプロトコルに関係なく、HTTPSビデオを強制的に配信することができます。 (作成者モードのビデオプレビューは、常にHTTPS経由で安全に配信されます)。

AEMで使用するDynamic Mediaビデオの公開方法に応じて、`Video360Player.ssl`設定属性の適用方法が変わります。次に示す例を参照してください。

* URLを含むDynamic Mediaビデオを公開する場合、URLに`Video360Player.ssl`を追加します。 例えば、ビデオの配信を強制的に保護するには、次のビューアURLの例の末尾に`&Video360Player.ssl=on`を追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   [Web アプリケーションへのURLのリンク](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)も参照してください。

* 埋め込みコードを含むDynamic Mediaビデオを公開する場合は、埋め込みコードスニペット内の他のビューア設定パラメータのリストに`Video360Player.ssl`を追加します。 例えば、HTTPSビデオ配信を強制するには、次の例のように`&Video360Player.ssl=on`を追加します。

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

   [Webページへのビデオの埋め込み](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)も参照してください。
