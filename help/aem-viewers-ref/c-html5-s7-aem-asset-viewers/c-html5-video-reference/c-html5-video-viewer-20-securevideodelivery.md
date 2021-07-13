---
description: HTTPビデオ配信
solution: Experience Manager
title: HTTPビデオ配信
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,User
exl-id: 33907e22-107b-4345-82bb-cad47cb7a839
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# HTTPビデオ配信{#http-video-delivery}

>[!NOTE]
>
>セキュアビデオ配信は、[機能パック13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)のインストールでAEM 6.2に適用され、[機能パックNPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)のインストールでAEM 6.1に適用されます。

この節の最初に説明するようにビューアが設定で動作する場合、公開されたビデオ配信は、HTTPS（セキュア）モードとHTTP（セキュア）モードの両方でおこなわれます。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みWebページの配信プロトコルに厳密に従います。 ただし、[VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)設定属性を使用してWebページを埋め込むことで、使用するプロトコルに関係なく、HTTPSビデオ配信を強制できます。 （オーサーモードのビデオプレビューは、常にHTTPS経由で安全に配信されます）。

AEMで使用するDynamic Mediaビデオの公開方法に応じて、次に示すように、`VideoPlayer.ssl`設定属性の適用方法は異なります。

* URLを含むDynamic Mediaビデオを公開する場合は、URLに`VideoPlayer.ssl`を追加します。 例えば、ビデオのセキュア配信を強制するには、次のビューアURLの例の最後に`&VideoPlayer.ssl=on`を追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/VideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&VideoPlayer.ssl=on
   ```

   [WebアプリケーションへのURLのリンク](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)も参照してください。

* 埋め込みコードを含むDynamic Mediaビデオを公開する場合は、埋め込みコードスニペット内の他のビューア設定パラメーターのリストに`VideoPlayer.ssl`を追加します。 例えば、HTTPSビデオ配信を強制するには、次の例のように`&VideoPlayer.ssl=on`を追加します。

   ```
   <style type="text/css"> 
    #s7video_div.s7videoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/VideoViewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7videoviewer = new s7viewers.VideoViewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
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
