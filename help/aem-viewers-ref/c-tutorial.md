---
description: ビューアSDKは、カスタムビューア開発用のJavaScriptベースのコンポーネントセットを提供します。 ビューアは、AdobeDynamic Mediaが提供するリッチメディアコンテンツをWebページに埋め込むことができるWebベースのアプリケーションです。
solution: Experience Manager
title: ビューアSDKのチュートリアル
feature: Dynamic Media Classic，ビューア，SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# ビューアSDKのチュートリアル{#viewer-sdk-tutorial}

ビューアSDKは、カスタムビューア開発用のJavaScriptベースのコンポーネントセットを提供します。 ビューアは、AdobeDynamic Mediaが提供するリッチメディアコンテンツをWebページに埋め込むことができるWebベースのアプリケーションです。

例えば、SDKはインタラクティブなズームとパンを提供します。 また、Dynamic Media Classicと呼ばれるバックエンドアプリケーションを使用してAdobeDynamic Mediaにアップロードされたアセットの360°ビューとビデオ再生も提供します。

コンポーネントはHTML5機能に依存していますが、Android、Apple iOSデバイス、およびInternet Explorer以降を含むデスクトップで動作するように設計されています。 この種のエクスペリエンスは、サポートされるすべてのプラットフォームに対して1つのワークフローを提供できることを意味します。

SDKは、ビューアコンテンツを構成するUIコンポーネントで構成されます。 これらのコンポーネントは、CSSを使用してスタイルを設定できます。また、セット定義の取得や解析、追跡など、何らかの役割を持つ非UIコンポーネントを使用することもできます。 すべてのコンポーネントの動作は、修飾子を使用してカスタマイズできます。この修飾子は、様々な方法で指定できます。例えば、URLの`name=value`ペアのように指定できます。

このチュートリアルでは、基本ズームビューアを作成するのに役立つ、次の順序で作業を行います。

* [Adobe Developer Connectionから最新のビューアSDKをダウンロードします。](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [ビューアSDKの読み込み](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [ビューアへのスタイルの追加](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [コンテナとZoomViewを含める](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [ビューアへのMediaSetおよびSwatchesコンポーネントの追加](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [ビューアへのボタンの追加](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [スウォッチの垂直方向の設定](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Adobe Developer Connectionから最新のビューアSDKをダウンロードします。 {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. 最新のビューアSDKをAdobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->からダウンロードします。

   >[!NOTE]
   >
   >SDKは実際にリモートで読み込まれるので、ビューアSDKパッケージをダウンロードしなくても、このチュートリアルを完了できます。 ただし、ビューアパッケージには追加の例と、独自のビューアを作成する際に役立つAPIリファレンスガイドが含まれています。

## ビューアSDKの読み込み {#section-98596c276faf4cf79ccf558a9f4432c6}

1. まず、新しいページを設定し、作成する基本ズームビューアを開発します。

   空のSDKアプリケーションを設定するためのブートストラップ（ローダー）コードを考えてみましょう。 お気に入りのテキストエディターを開き、次のHTMLマークアップを貼り付けます。

   ```
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   `script`タグ内に次のJavaScriptコードを追加して、`ParameterManager`を初期化します。 これは、 `initViewer`関数内でSDKコンポーネントを作成およびインスタンス化する準備に役立ちます。

   ```
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. ファイルを空のテンプレートとして保存します。 任意のファイル名を使用できます。

   今後新しいビューアを作成する際には、この空のテンプレートファイルを参照として使用します。 このテンプレートは、ローカルで、Webサーバーから提供される場合に機能します。

次に、ビューアにスタイルを追加します。

## ビューアへのスタイルの追加 {#section-3783125360a1425eae5a5a334867cc32}

1. 作成するこのフルページビューア用に、いくつかの基本的なスタイルを追加できます。

   次の`style`ブロックを`head`の下に追加します。

   ```
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

コンポーネント`Container`と`ZoomView`を含めます。

## コンテナとZoomViewを含める {#section-1a01730663154a508b88cc40c6f35539}

1. コンポーネント`Container`と`ZoomView`を含めて、実際のビューアを作成します。

   [!DNL Utils.js]スクリプトの読み込み後に、次の`include`ステートメントを`<head>`要素の末尾に挿入します。

   ```
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 次に、様々なSDKコンポーネントを参照する変数を作成します。

   次の変数を、メインの匿名関数の先頭（`s7sdk.Util.init()`のすぐ上）に追加します。

   ```
   var container, zoomView;
   ```

1. `initViewer`関数内に次を挿入して、修飾子を定義し、それぞれのコンポーネントをインスタンス化します。

   ```
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. 上記のコードを正しく実行するには、`containerResize`イベントハンドラーとヘルパー関数を追加します。

   ```
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. 作成内容が表示されるように、ページをプレビューします。 ページは次のようになります。

   ![](assets/viewer-1.jpg)

次に、コンポーネント`MediaSet`と`Swatches`をビューアに追加します。

## ビューアへのMediaSetおよびSwatchesコンポーネントの追加 {#section-02b8c21dd842400e83eae2a48ec265b7}

1. ユーザーがセットから画像を選択できるように、コンポーネント`MediaSet`と`Swatches`を追加できます。

   次のSDKインクルードを追加します。

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 変数リストを次のように更新します。

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. `initViewer`関数内で`MediaSet`および`Swatches`コンポーネントをインスタンス化します。

   `ZoomView`コンポーネントと`Container`コンポーネントの後に`Swatches`インスタンスをインスタンス化してください。それ以外の場合は、`Swatches`が重ね順に表示されません。

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 次のイベントハンドラ関数を追加します。

   ```
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. スウォッチをビューアの下部に配置するには、次のCSSを`style`要素に追加します。

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. ビューアをプレビューします。

   スウォッチがビューアの左下に表示されます。 スウォッチをビューアの幅全体に合わせるには、ユーザがブラウザのサイズを変更するたびにスウォッチのサイズを手動で変更する呼び出しを追加します。 `resizeViewer`関数に次のコードを追加します。

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   これで、ビューアは次の画像のようになります。 ビューアのブラウザウィンドウのサイズを変更してみて、結果の動作に注意してください。

   ![](assets/viewer-2.jpg)

次に、ズームイン、ズームアウトおよびズームリセットボタンをビューアに追加します。

## ビューアへのボタンの追加 {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 現在、ユーザーはクリックまたはタッチジェスチャを使用してのみズームできます。 そのため、ビューアに基本ズームコントロールボタンを追加します。

   次のボタンコンポーネントを追加します。

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 変数リストを次のように更新します。

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. `initViewer`関数の下部にあるボタンをインスタンス化します。

   CSSで`z-index`を指定しない限り、順序は重要です。

   ```
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 次に、ファイルの最上部にある`style`ブロックに次の内容を追加して、ボタンの基本的なスタイルを定義します。

   ```
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. ビューアをプレビューします。 次のようになります。

   ![](assets/viewer-3.jpg)

   次に、スウォッチが右上に垂直に並ぶように設定します。

## スウォッチの垂直方向の設定 {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 修飾子は`ParameterManager`インスタンス上で直接設定できます。

   `initViewer`関数の先頭に次のコードを追加して、`Swatches`サムのレイアウトを1行に設定します。

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. `resizeViewer`内で次のサイズ変更呼び出しを更新します。

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. `ZoomViewer.css`で次の`s7swatches`ルールを編集します。

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. ビューアをプレビューします。 次のようになります。

   ![](assets/viewer-4.jpg)

   これで、基本ズームビューアが完了しました。

   このビューアチュートリアルでは、Dynamic Media Viewer SDKの基本事項に触れます。 SDKを使用すると、様々な標準コンポーネントを使用して、ターゲットオーディエンスに対するリッチな表示エクスペリエンスを簡単に作成およびスタイル設定できます。
