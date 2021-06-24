---
description: レスポンシブ画像ライブラリをWebページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。
solution: Experience Manager
title: レスポンシブ画像ライブラリの使用
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# レスポンシブ画像ライブラリの使用{#using-responsive-image-library}

レスポンシブ画像ライブラリをWebページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。

**レスポンシブ画像ライブラリを使用するには**

1. Dynamic Media Classicでは、レスポンシブ画像ライブラリをプリセットで使用する予定がある場合に備えて、[画像プリセット](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing)を作成します。

   レスポンシブ画像ライブラリで使用する画像プリセットを定義する際には、`wid=`、`hei=`、`scl=`など、画像サイズに影響を与える設定を使用しないでください。 画像プリセットにサイズフィールドを指定しないでください。 代わりに、空白の値のままにします。
1. ライブラリのJavaScriptファイルをWebページに追加します。

   ライブラリAPIを使用する前に、`responsive_image.js`を必ず含めてください。 このJavaScriptファイルは、次に示すように、ISビューアの標準のデプロイ先の`libs/`サブフォルダーにあります。

   `<s7viewers_root>/libs/responsive_image.js`
1. 既存の画像を設定します。

   ライブラリは、作業中の画像インスタンスから特定の設定属性を読み取ります。 このような画像に対して`s7responsiveImage` API関数を呼び出す前に、属性を定義します。

   また、既存の画像URLを`data-src`属性に入れることをお勧めします。 次に、既存の`src`属性を設定し、データURIとして1 x 1のGIF画像をエンコードします。 これにより、読み込み時にWebページから送信されるHTTP要求の数が減ります。 ただし、SEO（検索エンジン最適化）が必要な場合は、画像インスタンスに`title`属性を設定する方が良いことに注意してください。

   次の例では、画像の`data-breakpoints`属性を定義し、データURIとしてエンコードされた1x1 GIFを使用します。

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. ライブラリが管理するすべての画像インスタンスに対して`s7responsiveImage` API関数を呼び出します。

   ライブラリが管理するすべての画像インスタンスに対して`s7responsiveImage` API関数を呼び出します。 この呼び出しの後、ライブラリは、Webページレイアウトの`IMG`要素の実行時のサイズとデバイス画面の密度に従って、元の画像を画像サービングからダウンロードした画像に置き換えます。

   次のコードは、画像で`s7responsiveImage` API関数を呼び出す例です（`responsiveImage`はその画像のIDです）。

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

ライブラリは、Webページ上の多くの画像インスタンスの同時操作をサポートします。 したがって、ライブラリで管理する各画像に対して、上記の手順1と2を繰り返します。

画像要素のサイズを柔軟に設定できるように、Webページでスタイルを設定する必要があります。 レスポンシブ画像ライブラリ自体は、固定サイズの画像と「流動的」な画像を区別しません。 固定サイズの画像に適用すると、新しい画像が1回だけ読み込まれます。

次のコードは、レスポンシブ画像ライブラリで管理される単一の流体画像を持つ簡単なWebページの例です。 この例には、Webブラウザーのウィンドウサイズに対して画像を「レスポンシブ」にする追加のCSSスタイルが含まれています。

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

AEM 6.4およびDynamic Mediaビューア5.9では、2つのスマート切り抜きモードを使用できます。

* **手動**  — ユーザー定義のブレークポイントと対応する画像サービスコマンドは、画像要素の属性内で定義します。
* **スマート切り抜き**  — 計算済みのスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。最適なレンディションは、画像要素の実行時のサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode`属性を`smart crop`に設定します。 例：

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連する画像要素は、ブレークポイントが変更されたときに、実行時に`s7responsiveViewer`イベントをディスパッチします。

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
