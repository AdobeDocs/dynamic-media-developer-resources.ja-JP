---
description: レスポンシブ画像ライブラリをWebページに追加し、ライブラリで既存の画像を管理するには、次の手順を実行します。
seo-description: レスポンシブ画像ライブラリをWebページに追加し、ライブラリで既存の画像を管理するには、次の手順を実行します。
seo-title: レスポンシブ画像ライブラリの使用
solution: Experience Manager
title: レスポンシブ画像ライブラリの使用
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# レスポンシブ画像ライブラリの使用{#using-responsive-image-library}

レスポンシブ画像ライブラリをWebページに追加し、ライブラリで既存の画像を管理するには、次の手順を実行します。

**レスポンシブ画像ライブラリを使用するには**

1. SPSで、レスポンシ [ブ画像ライブラリをプリセットと共に使用する場合](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) 、画像プリセットを作成します。

   レスポンシブ画像ライブラリで使用する画像プリセットを定義する場合、、、などの画像サイズに影響する設定を使用し `wid=`ないで `hei=`くださ `scl=`い。 画像プリセットにはサイズフィールドを指定しないでください。 代わりに、空白の値のままにします。
1. ライブラリのJavaScriptファイルをWebページに追加します。

   ライブラリAPIを使用する前に、を必ず含めてくださ `responsive_image.js`い。 次のJavaScriptファイルは、標準のISビューア `libs/` のデプロイ先のサブフォルダーにあります。

   `<s7viewers_root>/libs/responsive_image.js`
1. 既存の画像を設定します。

   ライブラリは、使用しているイメージインスタンスから特定の設定属性を読み取ります。 このような画像に対して `s7responsiveImage` API関数が呼び出される前に、属性を定義します。

   また、既存の画像URLを属性に含めることもお勧めし `data-src` ます。 次に、既存の属性を設定し、1x1 GIF `src` 画像をデータURIとしてエンコードするようにします。 これにより、読み込み時にWebページから送信されるHTTP要求の数が減ります。 ただし、SEO（検索エンジンの最適化）が必要な場合は、画像インスタンスに属性を設定する `title` 方がよいことに注意してください。

   次の例では、画像の属性を定義し、デ `data-breakpoints` ータURIとしてエンコードされた1x1 GIFを使用しています。

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. ライブラリが管理するすべての画像インスタンスに対して、 `s7responsiveImage` API関数を呼び出します。

   ライブラリが管理するすべての画像インスタンスに対して、 `s7responsiveImage` API関数を呼び出します。 この呼び出しの後、ライブラリは、Webページレイアウトの要素の実行時のサイズとデバイス画面の密度に従って、元の画像を画像サービングからダウンロードした画像に置き換え `IMG` ます。

   次のコードは、画像の `s7responsiveImage` IDを前提として、画像に対して `responsiveImage` API関数を呼び出す例です。

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

ライブラリは、Webページ上の多くの画像インスタンスの同時作業をサポートしています。 したがって、ライブラリで管理する各画像に対して、上記の手順1と2を繰り返します。

Webページでは、画像要素のスタイルを設定して、サイズを柔軟に設定する必要があります。 レスポンシブ画像ライブラリ自体は、固定サイズの画像と「流動」の画像を区別しません。 固定サイズの画像に適用すると、新しい画像が1回だけ読み込まれます。

次のコードは、レスポンシブ画像ライブラリで管理される単一の流体画像を持つ簡単なWebページの例です。 この例には、画像をWebブラウザーのウィンドウサイズに「レスポンシブ」にする追加のCSSスタイルが含まれています。

```
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**スマート切り抜きの使用**

AEM 6.4およびScene7ビューア5.9では、次の2つのスマート切り抜きモードを使用できます。

* **手動** — ユーザ定義のブレークポイントと、対応する画像サービスコマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** — 計算済みのスマート切り抜きレンディションが、配信サーバーから自動的に取得されます。 最適なレンディションは、画像要素の実行時のサイズを使用して選択されます。

スマート切り抜きモードを使用するには、属性をに `data-mode` 設定しま `smart crop`す。 例：

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連する画像要素は、実行時にブレークポ `s7responsiveViewer` イントが変更されたときにイベントをディスパッチします。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
