---
description: 'null'
seo-description: 'null'
seo-title: HTTPSビデオ配信
solution: Experience Manager
title: HTTPSビデオ配信
topic: Dynamic media
uuid: acda9c8f-e8f4-4855-9b14-82838ec5a1b9
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# HTTPSビデオ配信{#https-video-delivery}

>[!NOTE]
>
>セキュアビデオ配信は、 [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 、および [Feature Pack NPR-15011がインストールされているAEM 6.2にのみ適用されます](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)。

この節の最初に説明するように、ビューアが設定で動作する場合、公開されたビデオ配信は、HTTPS（セキュア）モードとHTTP（セキュア）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みWebページの配信プロトコルに厳密に従います。 ただし、VideoPlayer.ssl設定属性を使用してWebページを埋め込むことで使用されるプロトコルに関係なく、HTTPSビデオ配信を強制する [ことができます](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771) 。 （作成者モードのビデオプレビューは、常にHTTPS経由で安全に配信されます）。

AEMで使用するダイナミックメディアビデオの公開方法に応じて、設定属性の適用方法が異なります。 `VideoPlayer.ssl` 次に示すように、設定属性の適用方法は異なります。

* URLを使用してダイナミックメディアビデオを公開する場合、URLに `VideoPlayer.ssl` 追加されます。 例えば、ビデオ配信のセキュリティを強制するには、 `&VideoPlayer.ssl=on` 次のビューアのURLの例の末尾に追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
   ```

   See also [Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

* 埋め込みコードを含むダイナミックメディアビデオを公開する場合は、埋め込みコ `VideoPlayer.ssl` ードスニペット内の他のビューア設定パラメータのリストにを追加します。 例えば、HTTPSビデオ配信を強制するには、次の例のよ `&VideoPlayer.ssl=on` うに追加します。

   ```
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
       //To pass other parameter from the hotspot, you will need to add custom parameter during the hotspot setup as parameterName=value 
       loadQuickView(sku); //Replace this call with your quickview plugin 
       //Please refer to your quickviewer plugin for the quickview call 
       },  
   "initComplete":function() {  
       //--- Attach quickview popup to viewer container so popup will work in fullscreen mode --- 
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

   See also [Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

