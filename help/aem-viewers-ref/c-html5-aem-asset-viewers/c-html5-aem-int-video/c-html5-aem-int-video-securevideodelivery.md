---
title: HTTPS ビデオ配信
description: HTTPS ビデオ配信
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 68d37b5d-5015-4a98-84b8-8911ace327ed
TQID: 'https://experienceleague.adobe.com/2hNT89eDvhOe28dej85MxFog3VnOqzpe66MeIVNVbWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 196
ht-degree: 0%

---

# HTTPS ビデオ配信{#https-video-delivery}

<!--
 >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).
-->

この節の冒頭で説明したように、ビューアが設定で動作する場合、公開されたビデオ配信は、HTTPS （セキュア）モードとHTTP （非セキュア）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みweb ページの配信プロトコルに厳密に従います。 ただし、[VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771)構成属性を使用してweb ページを埋め込むことで使用されるプロトコルに関係なく、HTTPS ビデオ配信を強制することができます。 （作成者モードのビデオプレビューは、常にHTTPS経由で安全に配信されます）。

Adobe Experience Managerで使用する[!DNL Dynamic Media] ビデオの公開方法に応じて、`VideoPlayer.ssl`構成属性は次の例に示すように異なる方法で適用されます。

* URLを含む[!DNL Dynamic Media]動画を公開する場合は、URLに`VideoPlayer.ssl`を追加します。

<!-- For example, to force secure video delivery, you append `&VideoPlayer.ssl=on` to the end of the following viewer URL example:-->

<!--

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
  ```

-->

Web アプリケーションへのURLのリンク [も参照してください](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)

* 埋め込みコードを含む[!DNL Dynamic Media] ビデオを公開する場合は、埋め込みコードスニペット内の他のビューア設定パラメーターのリストに`VideoPlayer.ssl`を追加します。

<!-- For example, to force HTTPS video delivery, you append `&VideoPlayer.ssl=on` as in the following example: -->

<!--

  ```html {.line-numbers}
  <style type="text/css"> 
   #s7interactivevideo_div.s7interactivevideoviewer{ 
     width:100%;  
     height:auto; 
   } 
  </style> 
  <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
  <div id="s7interactivevideo_div"></div> 
  <script type="text/javascript"> 
   var s7interactivevideoviewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId" : "s7interactivevideo_div", 
    "params" : {  
     "VideoPlayer.ssl" : "on", 
     "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
     "contenturl" : "https://demos-pub.assetsadobe.com/",  
     "config" : "/etc/dam/presets/viewer/Shoppable_Video_light", 
     "config2": "/etc/dam/presets/analytics", 
     "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
     "interactivedata": "content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt", 
     "VideoPlayer.contenturl": "https://adobedemo62-h.assetsadobe.com/is/content", 
     "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
   }) 
   /* // Example of interactive video event for quick view. 
     s7interactivevideoviewer.setHandlers({  
     "quickViewActivate": function(inData) { 
       var sku=inData.sku; //SKU for product ID 
      //To pass other parameter from the hotspot, you must add custom parameter during the hotspot setup as parameterName=value 
      loadQuickView(sku); //Replace this call with your quickview plugin 
      //Please refer to your quickviewer plugin for the quickview call 
      },  
  "initComplete":function() {  
      //--- Attach quickview pop-up to viewer container so pop-up works in fullscreen mode --- 
      var popup = document.getElementById('quickview_div'); // get custom quick view container 
      popup.parentNode.removeChild(popup); // remove it from current DOM 
      var sdkContainerId = s7interactivevideoviewer.getComponent("container").getInnerContainerId(); // get viewer container component 
      var inner_container = document.getElementById(sdkContainerId);  
      inner_container.appendChild(popup); //Attach custom quick view container to viewer 
      }  
     }); 
   */ 
   s7interactivevideoviewer.init(); 
  </script>
  ```
-->

「[Web ページへのビデオの埋め込み](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)」も参照してください。
