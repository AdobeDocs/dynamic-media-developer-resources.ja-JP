---
description: HTTPSビデオ配信
solution: Experience Manager
title: HTTPSビデオ配信
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# HTTPSビデオ配信{#https-video-delivery}

>[!NOTE]
>
>セキュアビデオ配信は、[Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480)のインストールを含むAEM 6.2と、[Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)のインストールを含むAEM 6.1にのみ適用されます。

この節の最初に説明するように、ビューアが設定で動作する場合、公開されたビデオの配信は、HTTPS（セキュア）モードとHTTP（セキュア）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みWebページの配信プロトコルに厳密に従います。 ただし、[VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e)設定属性を使用してWebページを埋め込むときのプロトコルに関係なく、HTTPSビデオを強制的に配信させることはできます。 (作成者モードのビデオプレビューは、常にHTTPS経由で安全に配信されます)。

AEMで使用するDynamic Mediaビデオの公開方法に応じて、`VideoPlayer.ssl`設定属性の適用方法が変わります。次に示す例を参照してください。

* URLを含むDynamic Mediaビデオを公開する場合、URLに`VideoPlayer.ssl`を追加します。 例えば、ビデオの配信を強制的に保護するには、次のビューアURLの例の末尾に`&VideoPlayer.ssl=on`を追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   [(URLをWeb アプリケーションにリンクする](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic)も参照してください。

* 埋め込みコードを含むDynamic Mediaビデオを公開する場合は、埋め込みコードスニペット内の他のビューア設定パラメータのリストに`VideoPlayer.ssl`を追加します。 例えば、HTTPSビデオ配信を強制するには、次の例のように`&VideoPlayer.ssl=on`を追加します。

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

