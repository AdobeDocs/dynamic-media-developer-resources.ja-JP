---
description: 'null'
seo-description: 'null'
seo-title: HTTPSビデオ配信
solution: Experience Manager
title: HTTPSビデオ配信
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# HTTPSビデオ配信{#https-video-delivery}

>[!NOTE]
>
>セキュアビデオ配信は、 [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) 、および [Feature Pack NPR-15011がインストールされているAEM 6.2にのみ適用されます](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011)。

この節の最初に説明するように、ビューアが設定で動作する場合、公開されたビデオ配信は、HTTPS（セキュア）モードとHTTP（セキュア）モードの両方で発生する可能性があります。 デフォルト設定では、ビデオ配信プロトコルは、埋め込みWebページの配信プロトコルに厳密に従います。 ただし、VideoPlayer.ssl設定属性を使用してWebページを埋め込むことで使用されるプロトコルに関係なく、HTTPSビデオ配信を強制する [ことができます](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) 。 （作成者モードのビデオプレビューは、常にHTTPS経由で安全に配信されます）。

AEMで使用するダイナミックメディアビデオの公開方法に応じて、設定属性の適用方法が異なります。 `VideoPlayer.ssl` 次に示すように、設定属性の適用方法は異なります。

* URLを使用してダイナミックメディアビデオを公開する場合、URLに `VideoPlayer.ssl` 追加されます。 例えば、ビデオ配信のセキュリティを強制するには、 `&VideoPlayer.ssl=on` 次のビューアのURLの例の末尾に追加します。

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   See also [(Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* 埋め込みコードを含むダイナミックメディアビデオを公開する場合は、埋め込みコ `VideoPlayer.ssl` ードスニペット内の他のビューア設定パラメータのリストにを追加します。 例えば、HTTPSビデオ配信を強制するには、次の例のよ `&VideoPlayer.ssl=on` うに追加します。

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

   See also [(Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

