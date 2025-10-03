---
description: レスポンシブ画像ライブラリは、Dynamic Media から提供され、レスポンシブ web ページに埋め込まれる画像の品質を動的に調整するJavaScript モジュールです。 また、高密度画面を使用するデバイスの画質も向上します。 このライブラリは、スマート切り抜きとスマートスウォッチから結果をレスポンシブにレンダリングすることもできます。
solution: Experience Manager
title: レスポンシブ画像ライブラリについて
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# レスポンシブ画像ライブラリについて{#about-responsive-image-library}

レスポンシブ画像ライブラリは、Dynamic Media から提供され、レスポンシブ web ページに埋め込まれる画像の品質を動的に調整するJavaScript モジュールです。 また、高密度画面を使用するデバイスの画質も向上します。 このライブラリは、スマート切り抜きとスマートスウォッチから結果をレスポンシブにレンダリングすることもできます。

## デモ URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

レスポンシブ画像ライブラリの最も簡単なユースケースは、画像の幅のブレークポイント値のリストを定義することです。 このリストにより、ブラウザーウィンドウのサイズを変更したユーザーやデバイスの向きを変更したユーザーの web ページのレイアウト変更が原因で画像のサイズが変更された場合、適切なレンディションが読み込まれて表示されるようになります。 ライブラリは画面上の画像サイズを継続的に監視し、新しいブレークポイントの幅に達するたびに Dynamic Media から新しい画像レンディションを取得します。

<!--

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Demo URL </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p></td> 
   <td colname="col2"> <p>The following is a simple example where the responsive image is within a container that takes 50% of the web page width. Every time the browser window is resized the container width changes. When the image width reaches one of the configured breakpoints-which are set at 200, 400, 600 and 800 pixels for illustrative purposes-a new rendition is downloaded and displayed. The goal is to avoid loading unnecessary large images and save network bandwidth. </p> <p>Click the URL so you open the web page, resize the browser window, and monitor network traffic. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p></td> 
   <td colname="col2"> <p>The following Bootstrap example illustrates the same use case in a web page. According to Bootstrap CSS, the layout cell to which the responsive image is added can take one of the following widths: 360, 720 and 940 pixels. These values are exactly what is passed as breakpoints to the Responsive Image Library. As such, Dynamic Media ensures that the client's network bandwidth is used effectively. And, it also ensures that the image is displayed in the exact size needed-given the current web page layout-without any visual artifacts from scaling the client-side browser. </p> <p>Click the URL so you open the web page, resize the browser window to hit different layout breakpoints, and monitor network traffic. </p> <p>More advanced use cases include associating different Image Presets, or Image Serving commands, or both, with different breakpoint values. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p></td> 
   <td colname="col2"> <p>In this next example, Image Presets of different image quality and format for different breakpoint sizes are used. For a small breakpoint, a low-quality preset is applied which forces Image Serving to return the GIF image compressed to six colors only. A medium breakpoint is using an Image Preset configured for JPEG with high compression. The largest breakpoint is associated with a high-quality Image Preset using lossless PNG. Such method ensures that high-quality images are delivered to such devices, based on the assumption that devices with larger screens have greater bandwidth and processing power. </p> <p>Click the URL so you open the web page, resize the web browser window from larger to smaller and notice how the image quality degrades. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p></td> 
   <td colname="col2"> <p>In addition to Image Presets, it is possible to associate specific Image Serving commands with breakpoints. The following example shows how it is possible to gradually crop the banner image to the region of interest as the onscreen image size becomes smaller. Here, the largest breakpoint does not have any Image Serving commands at all, so the banner image is fully visible. At medium breakpoint applies moderate cropping, making only the runner with text "Running" visible. At small breakpoint, more cropping is applied so that only the product is shown. </p> <p>Click the URL so you open the web page and resize your browser window. Notice how the image crops gradually as you go from a larger to a smaller size. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p></td> 
   <td colname="col2"> <p>You can also use Image Serving commands with Image Serving Templates to control certain template parameters based on the image size. In this next example, an Image Serving Template is used where the font size of the text overlay is parameterized using <span class="codeph"> $fontsize </span> parameter. Responsive image is configured to use a larger font size for smaller image sizes to ensure that text always remains readable: </p> </td> 
  </tr> 
 </tbody> 
</table>

-->

## 必要システム構成 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**サーバのハードウェアとソフトウェア**

* Dynamic Media 画像サービング 6.0.1 以降。

**クライアントブラウザーの最小要件**

* Microsoft® Windows® 7 以降、macOS X 10.8 以降。
* Firefox 23、Safari 6、Chrome 29、IE 9 以降。
* iOS 6 以降。
* iPhone3GS 以降およびiPad2 以降（ネイティブブラウザーのみ）で認定済み。
* Android™ OS 2.3 以降。
* モバイル デバイスの Internet Explorer は現在サポートされていません。
