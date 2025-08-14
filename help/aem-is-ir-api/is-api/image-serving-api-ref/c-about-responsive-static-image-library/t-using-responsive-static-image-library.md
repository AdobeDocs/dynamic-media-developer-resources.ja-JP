---
title: レスポンシブ画像ライブラリの使用
description: レスポンシブ画像ライブラリを web ページに追加し、このライブラリで既存の画像を管理するには、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# レスポンシブ画像ライブラリの使用{#using-responsive-image-library}

レスポンシブ画像ライブラリを web ページに追加し、このライブラリで既存の画像を管理するには、次の手順を実行します。

**レスポンシブ画像ライブラリを使用するには**

1. プリセットと共にレスポンシブ画像ライブラリを使用する場合は、Dynamic Media Classicで [ 画像プリセットを作成 ](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) します。

   レスポンシブ画像ライブラリで使用する画像プリセットを定義する場合は、画像サイズに影響を与える設定（`wid=`、`hei=`、`scl=` など）を使用しないでください。 画像プリセットでは、「サイズ」フィールドを指定しないでください。 代わりに、空の値のままにします。
1. ライブラリのJavaScript ファイルを Web ページに追加します。

   ライブラリ API を使用する前に、`responsive_image.js` を含めてください。 このJavaScript ファイルは、標準の IS-Viewers デプロイメントの `libs/` サブフォルダーにあります。

   `<s7viewers_root>/libs/responsive_image.js`
1. 既存の画像を設定します。

   ライブラリは、操作対象の画像インスタンスから特定の設定属性を読み取ります。 このような画像に対して `s7responsiveImage` API 関数が呼び出される前に属性を定義します。

   既存の画像 URL を `data-src` 属性に配置することをお勧めします。 次に、既存の `src` 属性を、データ URI としてエンコードされた 1x1 GIF画像を持つように設定します。 これにより、読み込み時に web ページから送信される HTTP リクエストの数が減ります。 ただし、SEO （検索エンジン最適化）が必要な場合は、画像インスタンスに `title` 属性を設定する方が良いでしょう。

   次に、画像の属性を定義し、データ URI`data-breakpoints` してエンコードされた 1x1 GIFを使用する例を示します。

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. ライブラリが管理するすべての画像インスタンスに対して、`s7responsiveImage` API 関数を呼び出します。

   ライブラリが管理するすべての画像インスタンスに対して、`s7responsiveImage` API 関数を呼び出します。 そのような呼び出しの後、ライブラリは、web ページレイアウト内の `IMG` 要素の実行時サイズとデバイス画面の密度に応じて、元の画像を画像サービングからダウンロードされた画像に置き換えます。

   次のコードは、画像に対して API 関数 `s7responsiveImage` 呼び出す例です。画像が `responsiveImage` の画像の ID であると仮定しています。

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

ライブラリは、Web ページ上の多数の画像インスタンスの同時操作をサポートしています。 そのため、ライブラリで管理する各画像に対して、上記の手順 1 と 2 を繰り返します。

画像要素のサイズを柔軟に調整するには、web ページが責任を負います。 レスポンシブ画像ライブラリ自体は、固定サイズの画像と「可変」画像を区別しません。 固定サイズの画像に適用した場合、新しい画像は 1 回だけ読み込まれます。

次のコードは、レスポンシブ画像ライブラリによって管理される単一の流動画像を持つ単純な web ページの完全な例です。 この例には、web ブラウザーのウィンドウサイズに合わせて画像を「レスポンシブ」にするための追加の CSS スタイルが含まれています。

```html {.line-numbers}
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

AEM 6.4 と Dynamic Media Viewers 5.9 では、次の 2 つのスマート切り抜きモードを使用できます。

* **手動** - ユーザー定義のブレークポイントと、対応する画像サービスコマンドは、画像要素の属性内で定義します。
* **スマート切り抜き** – 計算されたスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。 最適なレンディションは、画像要素のランタイムサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode` 属性を `smart crop` に設定します。 以下に例を挙げます。

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連する画像要素は、ブレークポイントが変更されたときに、実行時に `s7responsiveViewer` イベントをディスパッチします。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
