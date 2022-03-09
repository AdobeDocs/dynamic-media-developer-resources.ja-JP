---
title: レスポンシブ画像ライブラリの使用
description: レスポンシブ画像ライブラリを Web ページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# レスポンシブ画像ライブラリの使用{#using-responsive-image-library}

レスポンシブ画像ライブラリを Web ページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。

**レスポンシブ画像ライブラリを使用するには**

1. Dynamic Media Classicでは、 [画像プリセットの作成](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) レスポンシブ画像ライブラリをプリセットで使用する予定の場合。

   レスポンシブ画像ライブラリで使用する画像プリセットを定義する際に、画像サイズに影響を与える設定（例： ）を使用しないでください。 `wid=`, `hei=`または `scl=`. 画像プリセットでサイズフィールドを指定しないでください。 代わりに、空白の値のままにします。
1. ライブラリの JavaScript ファイルを Web ページに追加します。

   ライブラリ API を使用する前に、次を必ず含めてください： `responsive_image.js`. この JavaScript ファイルは、 `libs/` 標準の IS-Viewers デプロイメントのサブフォルダー

   `<s7viewers_root>/libs/responsive_image.js`
1. 既存の画像を設定します。

   ライブラリは、作業中の画像インスタンスから特定の設定属性を読み取ります。 属性を `s7responsiveImage` このような画像に対して API 関数が呼び出されます。

   また、既存の画像 URL を `data-src` 属性。 次に、 `src` の属性には、1 x 1GIFの画像をデータ URI としてエンコードする必要があります。 これにより、読み込み時に Web ページから送信される HTTP リクエストの数が減ります。 ただし、SEO（検索エンジン最適化）が必要な場合は、 `title` 属性を画像インスタンスに設定します。

   次に、 `data-breakpoints` 属性を指定し、データ URI としてエンコードされた 1 x 1GIFを使用します。

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. を `s7responsiveImage` ライブラリが管理するすべての画像インスタンスの API 関数。

   を `s7responsiveImage` ライブラリが管理するすべての画像インスタンスの API 関数。 この呼び出しの後、ライブラリでは、元の画像が、 `IMG` 要素を選択し、デバイスの画面の密度を指定します。

   次のコードは、 `s7responsiveImage` 画像の API 関数 ( `responsiveImage` はその画像の ID です。

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

このライブラリは、Web ページ上の多くの画像インスタンスの同時操作をサポートします。 したがって、ライブラリで管理する画像ごとに、上記の手順 1 と 2 を繰り返します。

画像要素のサイズを柔軟に設定できるようにするには、Web ページでのスタイル設定をおこなう必要があります。 レスポンシブ画像ライブラリ自体は、固定サイズの画像と「流動的」な画像を区別しません。 固定サイズの画像に適用した場合、新しい画像は 1 回だけ読み込まれます。

次のコードは、レスポンシブ画像ライブラリで管理される単一の流体画像を持つ簡単な Web ページの例です。 この例には、Web ブラウザーのウィンドウサイズに対して画像を「レスポンシブ」にする追加の CSS スタイルが含まれています。

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

AEM 6.4 およびDynamic Mediaビューア 5.9 では、2 つのスマート切り抜きモードを使用できます。

* **手動** ：ユーザー定義のブレークポイントと、対応する画像サービスコマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** ：計算済みのスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。 最適なレンディションは、画像要素のランタイムサイズを使用して選択されます。

スマート切り抜きモードを使用するには、 `data-mode` 属性 `smart crop`. 例：

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連する画像要素は、 `s7responsiveViewer` イベントを設定します。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
