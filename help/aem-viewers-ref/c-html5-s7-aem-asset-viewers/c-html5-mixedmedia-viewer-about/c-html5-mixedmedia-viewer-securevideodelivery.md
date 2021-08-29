---
description: HTTPSビデオ配信
solution: Experience Manager
title: HTTPSビデオ配信
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# HTTPSビデオ配信{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

この節の最初に説明するようにビューアが設定で動作する場合、公開されたビデオ配信は、HTTPS（セキュア）モードとHTTP（セキュア）モードの両方でおこなわれます。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みWebページの配信プロトコルに厳密に従います。 ただし、[VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)設定属性を使用してWebページを埋め込むことで、使用するプロトコルに関係なく、HTTPSビデオ配信を強制できます。 （オーサーモードのビデオプレビューは、常にHTTPS経由で安全に配信されます）。

AEMで使用するDynamic Mediaビデオの公開方法に応じて、次に示すように、`VideoPlayer.ssl`設定属性の適用方法は異なります。

* URLを含むDynamic Mediaビデオを公開する場合は、URLに`VideoPlayer.ssl`を追加します。 例えば、ビデオのセキュア配信を強制するには、次のビューアURLの例の最後に`&VideoPlayer.ssl=on`を追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   [(WebアプリケーションへのURLのリンク](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)も参照してください。

* 埋め込みコードを含むDynamic Mediaビデオを公開する場合は、埋め込みコードスニペット内の他のビューア設定パラメーターのリストに`VideoPlayer.ssl`を追加します。 例えば、HTTPSビデオ配信を強制するには、次の例のように`&VideoPlayer.ssl=on`を追加します。

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   [(Webページへのビデオの埋め込み](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)も参照してください。
