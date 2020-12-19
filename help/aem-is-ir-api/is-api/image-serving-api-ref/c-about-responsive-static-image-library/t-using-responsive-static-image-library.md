---
description: レスポンシブ画像ライブラリをWebページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。
seo-description: レスポンシブ画像ライブラリをWebページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。
seo-title: レスポンシブ画像ライブラリの使用
solution: Experience Manager
title: レスポンシブ画像ライブラリの使用
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---


# レスポンシブ画像ライブラリの使用{#using-responsive-image-library}

レスポンシブ画像ライブラリをWebページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。

**レスポンシブ画像ライブラリを使用するには**

1. Scene7 Publishing Systemで、プリセットとレスポンシブ画像ライブラリを使用する場合に備えて、[画像プリセット](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html)を作成します。

   レスポンシブ画像ライブラリで使用する画像プリセットを定義する場合、`wid=`、`hei=`、`scl=`など、画像サイズに影響する設定は使用しないでください。 画像プリセットにはサイズフィールドを指定しないでください。 代わりに、空白の値のままにしてください。
1. ライブラリ追加のJavaScriptファイルをWebページに送信します。

   ライブラリAPIを使用する前に、`responsive_image.js`を必ず含めてください。 このJavaScriptファイルは、次に示すように、ISビューアの標準のデプロイ先の`libs/`サブフォルダーにあります。

   `<s7viewers_root>/libs/responsive_image.js`
1. 既存の画像を設定します。

   ライブラリは、操作している画像インスタンスから特定の設定属性を読み取ります。 `s7responsiveImage` API関数が呼び出される前に属性を定義します。

   また、既存の画像URLを`data-src`属性に入れることをお勧めします。 次に、既存の`src`属性を設定し、1x1 GIF画像をデータURIとしてエンコードします。 これにより、読み込み時にWebページから送信されるHTTP要求の数が減少します。 ただし、SEO（検索エンジンの最適化）が必要な場合は、イメージインスタンスに`title`属性を設定する方が良いことに注意してください。

   次の例は、画像の`data-breakpoints`属性を定義し、データURIとしてエンコードされた1x1 GIFを使用する場合の例です。

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. ライブラリが管理するすべての画像インスタンスに対して`s7responsiveImage` API関数を呼び出します。

   ライブラリが管理するすべての画像インスタンスに対して`s7responsiveImage` API関数を呼び出します。 この呼び出しの後、ライブラリは、Webページレイアウトの`IMG`要素の実行時のサイズとデバイス画面の密度に従って、元の画像を画像サービングからダウンロードされた画像に置き換えます。

   次のコードは、イメージに対して`s7responsiveImage` API関数を呼び出す例です（ここで`responsiveImage`はそのイメージのID）。

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

ライブラリは、Webページ上の多数の画像インスタンスとの同時作業をサポートしています。 したがって、ライブラリで管理する各画像に対して、上記の手順1と2を繰り返します。

画像要素のサイズを柔軟に変更するには、Webページで画像要素のスタイルを設定する必要があります。 レスポンシブ画像ライブラリ自体は、固定サイズの画像と「流動的な」画像を区別しません。 固定サイズの画像に適用した場合、新しい画像は1回だけ読み込まれます。

次のコードは、レスポンシブ画像ライブラリで管理される単一の流体画像を持つ簡単なWebページの例です。 この例には、画像がWebブラウザーのウィンドウサイズに「レスポンシブ」になるように、追加のCSSスタイルが含まれています。

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

* **手動**  — ユーザー定義のブレークポイントおよび対応する画像サービスコマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** ：計算済みのスマート切り抜きレンディションは、配信サーバから自動的に取得されます。最適なレンディションは、画像要素の実行時のサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode`属性を`smart crop`に設定します。 例：

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連付けられたイメージエレメントは、実行時にブレークポイントが変更されると`s7responsiveViewer`イベントをディスパッチします。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
