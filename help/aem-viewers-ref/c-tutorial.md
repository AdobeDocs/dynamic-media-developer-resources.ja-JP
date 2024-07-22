---
title: ビューア SDK チュートリアル
description: Viewer SDK は、カスタムビューア開発用のJavaScript ベースのコンポーネントのセットを提供します。 ビューアは web ベースのアプリケーションで、AdobeDynamic Mediaから提供されるリッチメディアコンテンツを web ページに埋め込むことができます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 0%

---

# ビューア SDK チュートリアル{#viewer-sdk-tutorial}

Viewer SDK は、カスタムビューア開発用のJavaScript ベースのコンポーネントのセットを提供します。 ビューアは web ベースのアプリケーションで、AdobeDynamic Mediaから提供されるリッチメディアコンテンツを web ページに埋め込むことができます。

例えば、SDK はインタラクティブなズームとパンを提供します。 また、Dynamic Media Classicと呼ばれるバックエンドアプリケーションを介してAdobe Dynamic Mediaにアップロードされたアセットの 360 度ビューおよびビデオ再生も提供します。

これらのコンポーネントはHTML5 の機能に依存しますが、Android™Apple iOSのデバイスおよび Internet Explorer 以降を含むデスクトップで動作するように設計されています。 この種のエクスペリエンスにより、サポートされるすべてのプラットフォームに対して単一のワークフローを提供できるようになります。

SDK は、ビューアコンテンツを構成する UI コンポーネントで構成されます。 これらのコンポーネントは、CSS を通じて、およびセット定義の取得、解析、トラッキングなど、何らかのサポート役割を持つ UI 以外のコンポーネントのスタイルを設定できます。 すべてのコンポーネントの動作は、修飾子を使用してカスタマイズできます。修飾子は、URL 内の `name=value` ペアなどのさまざまな方法で指定できます。

このチュートリアルでは、基本的なズームビューアの作成に役立つ、次のタスクの順序を示します。

* [ 最新のビューア SDK をAdobe Developer Connectionからダウンロードします ](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Viewer SDK のロード ](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [ ビューアへのスタイルの追加 ](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [ コンテナと ZoomView を含む ](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [ ビューアへのメディアセットコンポーネントとスウォッチコンポーネントの追加 ](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [ ビューアへのボタンの追加 ](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [スウォッチの垂直方向の設定](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Adobe Developer Connectionから最新のビューア SDK をダウンロードします {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) --> から最新のビューア SDK をダウンロードします。

   >[!NOTE]
   >
   >SDK はリモートでロードされるため、Viewer SDK パッケージをダウンロードしなくても、このチュートリアルを完了できます。 ただし、ビューアパッケージには、独自のビューアを作成するのに役立つ追加の例と API リファレンスガイドが含まれています。

## Viewer SDK のロード {#section-98596c276faf4cf79ccf558a9f4432c6}

1. まず、新しいページを設定して、作成する基本的なズームビューアを開発します。

   空の SDK アプリケーションを設定するために使用するBootstrap（またはローダー）コードを、この新しいページで使用することを検討してください。 お気に入りのテキストエディターを開き、次のHTMLマークアップを貼り付けます。

   ```html {.line-numbers}
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

   次のJavaScript コードを `script` タグ内に追加して、`ParameterManager` を初期化するようにします。 これにより、`initViewer` 関数内で SDK コンポーネントを作成し、インスタンス化する準備を整えることができます。

   ```javascript {.line-numbers}
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

   この空のテンプレートファイルは、今後ビューアを作成する際の参照として使用できます。 このテンプレートは、ローカルで、また web サーバーから提供される場合は機能します。

次に、ビューアにスタイルを追加します。

## ビューアへのスタイルの追加 {#section-3783125360a1425eae5a5a334867cc32}

1. 作成しているこの完全ページビューアでは、いくつかの基本スタイルを追加できます。

   `head` の下部に次の `style` ブロックを追加します。

   ```html {.line-numbers}
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

コンポーネント `Container` と `ZoomView` を含めるようにします。

## コンテナと ZoomView を含める {#section-1a01730663154a508b88cc40c6f35539}

1. コンポーネント `Container` と `ZoomView` を含めて、実際のビューアを作成します。

   [!DNL Utils.js] スクリプトが読み込まれた後で、次の `include` ステートメントを `<head>` 要素の下部に挿入します。

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. 次に、様々な SDK コンポーネントを参照する変数を作成します。

   メインの匿名関数の上部（`s7sdk.Util.init()` のすぐ上）に、次の変数を追加します。

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. 次のコードを `initViewer` 関数内に挿入して、いくつかの修飾子を定義し、それぞれのコンポーネントをインスタンス化できるようにします。

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full-screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full-screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. 上記のコードを正しく実行するには、`containerResize` イベントハンドラーとヘルパー関数を追加します。

   ```javascript {.line-numbers}
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

1. ページをプレビューして、作成した内容を確認します。 ページは次のようになります。

   ![ ビューアの例 1 イメージ ](assets/viewer-1.jpg)

次に、コンポーネント `MediaSet` と `Swatches` をビューアに追加します。

## ビューアへのメディアセットおよびスウォッチコンポーネントの追加 {#section-02b8c21dd842400e83eae2a48ec265b7}

1. ユーザーがセットから画像を選択できるようにするには、コンポーネントを追加して `Swatches` を追加 `MediaSet` ます。

   次の SDK インクルードを追加します。

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 変数リストを次のように更新します。

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. `initViewer` 関数内の `MediaSet` および `Swatches` コンポーネントをインスタンス化します。

   `ZoomView` および `Container` のコンポーネントの後に、必ず `Swatches` インスタンスをインスタンス化してください。そうしないと、スタック順序によって `Swatches` が非表示になります。

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 次のイベント ハンドラー関数を追加します。

   ```javascript {.line-numbers}
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

1. スウォッチをビューアの下部に配置するには、次の CSS を `style` 要素に追加します。

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. ビューアをプレビューします。

   スウォッチはビューアの左下に表示されます。 スウォッチがビューアの幅全体を取得するようにするには、ユーザーがブラウザーのサイズを変更するたびにスウォッチのサイズを手動で変更する呼び出しを追加します。 `resizeViewer` 関数に以下を追加します。

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   ビューアは次の画像のようになります。 ビューアのブラウザーウィンドウのサイズを変更してみて、結果として生じる動作に注目してください。

   ![ ビューアの例 2 つの画像 ](assets/viewer-2.jpg)

次に、ビューアにズームイン、ズームアウト、ズームリセットのボタンを追加します。

## ビューアへのボタンの追加 {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 現在、ユーザーは、クリックジェスチャまたはタッチジェスチャを使用してのみズームできます。 そのため、ビューアに基本的なズームコントロールボタンをいくつか追加します。

   次のボタンコンポーネントを追加します。

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 変数リストを次のように更新します。

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. 関数の下部にあるボタン `initViewer` インスタンス化。

   CSS で `z-index` を指定しない限り、順序は重要です。

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. 次に、ファイルの上部にある `style` ブロックに次の内容を追加して、ボタンの基本スタイルをいくつか定義します。

   ```CSS {.line-numbers}
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

   ![ ビューアの例 3 つの画像 ](assets/viewer-3.jpg)

   次に、スウォッチを右側に垂直に並べるように設定します。

## スウォッチの垂直方向の設定 {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 修飾子は、`ParameterManager` インスタンスで直接設定できます。

   `initViewer` 関数の上部に次のコードを追加して、`Swatches` しいサムレイアウトを 1 行として設定できるようにします。

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. `resizeViewer` 内で次のサイズ変更呼び出しを更新します。

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. `ZoomViewer.css` で次の `s7swatches` ルールを編集します。

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. ビューアをプレビューします。 次のようになります。

   ![ ビューアの例 4 つの画像 ](assets/viewer-4.jpg)

   これで、基本ズームビューアが完成しました。

   このビューアチュートリアルでは、Dynamic Media Viewer SDK が提供する基本的な機能について説明します。 SDK を操作すると、様々な標準コンポーネントを使用して、ターゲットオーディエンス向けの豊富な表示エクスペリエンスを簡単に構築およびスタイル設定できます。
