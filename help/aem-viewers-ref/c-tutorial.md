---
description: ビューアSDKは、カスタムビューア開発用に、JavaScriptベースのコンポーネントのセットを提供します。 ビューアは、Adobe Scene7が提供するリッチメディアコンテンツをWebページに埋め込むことができるWebベースのアプリケーションです。
seo-description: ビューアSDKは、カスタムビューア開発用に、JavaScriptベースのコンポーネントのセットを提供します。 ビューアは、Adobe Scene7が提供するリッチメディアコンテンツをWebページに埋め込むことができるWebベースのアプリケーションです。
seo-title: ビューアSDKチュートリアル
solution: Experience Manager
title: ビューアSDKチュートリアル
topic: Dynamic media
uuid: ea331f05-0c58-4e6b-b5a1-d9b8372d8e94
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---


# ビューアSDKチュートリアル{#viewer-sdk-tutorial}

ビューアSDKは、カスタムビューア開発用に、JavaScriptベースのコンポーネントのセットを提供します。 ビューアは、Adobe Scene7が提供するリッチメディアコンテンツをWebページに埋め込むことができるWebベースのアプリケーションです。

例えば、SDKはインタラクティブなズームとパンを提供します。 また、SPS(Scene7Publishing System)と呼ばれるバックエンドアプリケーションを通じてAdobe Scene7にアップロードされたアセットの360°の表示とビデオ再生も提供します。

コンポーネントはHTML5の機能に依存していますが、Android、Apple iOSデバイス、およびInternet Explorer以降を含むデスクトップで動作するように設計されています。 この種のエクスペリエンスは、サポートされるすべてのプラットフォームに対して単一のワークフローを提供できることを意味します。

SDKは、ビューアコンテンツを構成するUIコンポーネントで構成されます。 これらのコンポーネントは、CSSを介してスタイルを設定できます。UI以外のコンポーネントは、セット定義の取得や解析、追跡など、何らかのサポート役割を持ちます。 すべてのコンポーネントの動作は、修飾子を使用してカスタマイズ可能で、URLの`name=value`ペアのように、様々な方法で指定できます。

このチュートリアルでは、基本ズームビューアを作成する際に役立つタスクの順序を次に示します。

* [最新のビューアSDKをAdobe Developer Connectionからダウンロード](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [ビューアSDKの読み込み](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [ビューアへのスタイルの追加](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [コンテナとZoomViewの追加](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [ビューアへのMediaSetおよびSwatchesコンポーネントの追加](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Viewerへのボタンの追加](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [スウォッチの垂直方向の設定](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## 最新のビューアSDKをAdobe Developer Connection{#section-84dc74c9d8e24a2380b6cf8fc28d7127}からダウンロード

1. Adobe Developer Connection[ここ](https://marketing.adobe.com/developer/devcenter/scene7/show)から最新のビューアSDKをダウンロードします。

   >[!NOTE]
   >
   >ビューアSDKは実際にリモートで読み込まれるので、ビューアSDKパッケージをダウンロードしなくても、このチュートリアルを完了できます。 ただし、ビューアパッケージには、その他の例とAPIリファレンスガイドが含まれており、独自のビューアを作成すると便利です。

## ビューアSDKの読み込み{#section-98596c276faf4cf79ccf558a9f4432c6}

1. 作成する基本ズームビューアを開発するために、新規ページを設定して開始します。

   空のSDKアプリケーションを設定するためのブートストラップ（ローダ）コードを考えてみましょう。 お気に入りのテキストエディターを開き、次のHTMLマークアップをそのエディターに貼り付けます。

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
               can use a relative path if the viewer is deployed on one of the Adobe Scene7 servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Scene7 servers that have the SDK  
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

   追加`script`タグ内の次のJavaScriptコードを使用して`ParameterManager`を初期化します。 これは、`initViewer`関数内でSDKコンポーネントを作成およびインスタンス化する準備に役立ちます。

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

   今後新しいビューアを作成する場合は、この空のテンプレートファイルを参照用として使用します。 このテンプレートは、ローカルでもWebサーバーから提供された場合でも機能します。

Viewerにスタイルを追加します。

## ビューアへのスタイルの追加{#section-3783125360a1425eae5a5a334867cc32}

1. 自分で作成するこの完全なページビューアに対して、いくつかの基本的なスタイルを追加できます。

   追加次の`style`ブロックを`head`の下に置きます。

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

次に、コンポーネント`Container`と`ZoomView`を含めます。

## コンテナとZoomView {#section-1a01730663154a508b88cc40c6f35539}を含む

1. コンポーネント`Container`と`ZoomView`を含めて、実際のビューアを作成します。

   [!DNL Utils.js]スクリプトが読み込まれた後、次の`include`ステートメントを`<head>`要素の末尾に挿入します。

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

   次の追加変数は、メインの匿名関数の最上部（`s7sdk.Util.init()`のすぐ上）に配置されます。

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

1. ページにプレビューを設定して、作成した内容を確認できます。 ページは次のようになります。

   ![](assets/viewer-1.jpg)

次に、コンポーネント`MediaSet`と`Swatches`をビューアに追加します。

## ビューアへのMediaSetおよびSwatchesコンポーネントの追加{#section-02b8c21dd842400e83eae2a48ec265b7}

1. ユーザーがセットから画像を選択できるようにするには、コンポーネント`MediaSet`と`Swatches`を追加します。

   次追加のSDKが含まれます。

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. 変数リストを次のように更新します。

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. `initViewer`関数内で`MediaSet`および`Swatches`コンポーネントをインスタンス化します。

   `ZoomView`コンポーネントと`Container`コンポーネントの後に`Swatches`インスタンスを必ずインスタンス化してください。そうしないと、`Swatches`が非表示になります。

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. 次に、次のイベントハンドラー関数を追加します。

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

1. `style`要素に次のCSSを追加して、スウォッチをビューアの下部に配置します。

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Viewerのプレビュー

   スウォッチがビューアの左下に表示されます。 スウォッチをビューアの幅全体に合わせるには、ユーザがブラウザのサイズを変更するたびに、スウォッチのサイズを手動で変更する呼び出しを追加します。 追加`resizeViewer`関数に対して次の操作を行います。

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   Viewerは次の画像のようになります。 ビューアのブラウザウィンドウのサイズを変更してみて、結果の動作を確認してください。

   ![](assets/viewer-2.jpg)

ここで、ズームイン、ズームアウトおよびズームリセットボタンをビューアに追加します。

## ビューアへのボタンの追加{#section-1fc334fa0d2b47eb9cdad461725c07be}

1. 現在、ユーザーがズームできるのは、クリックまたはタッチジェスチャーのみです。 そのため、ビューアに基本的なズームコントロールボタンを追加します。

   追加次のボタンコンポーネント：

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. 変数リストを次のように更新します。

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. `initViewer`関数の下部にボタンをインスタンス化します。

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

1. 次に、ファイルの上部にある`style`ブロックに次を追加して、ボタンの基本的なスタイルを定義します。

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

1. Viewerのプレビュー 次のようになります。

   ![](assets/viewer-3.jpg)

   次に、スウォッチが右側に垂直に並ぶように設定します。

## スウォッチの垂直方向の設定{#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. 修飾子は`ParameterManager`インスタンスで直接設定できます。

   次追加に示すように、`initViewer`関数の先頭にあり、`Swatches`サムのレイアウトを1行に設定します。

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. `resizeViewer`内で次のresize呼び出しを更新します。

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

1. Viewerのプレビュー 次のようになります。

   ![](assets/viewer-4.jpg)

   これで基本ズームビューアが完成しました。

   このビューアチュートリアルでは、Scene7ビューアSDKの基本事項について説明します。 SDKを使用する際、様々な標準コンポーネントを使用して、ターゲットオーディエンス向けのリッチな表示エクスペリエンスを簡単に構築し、スタイルを設定できます。

