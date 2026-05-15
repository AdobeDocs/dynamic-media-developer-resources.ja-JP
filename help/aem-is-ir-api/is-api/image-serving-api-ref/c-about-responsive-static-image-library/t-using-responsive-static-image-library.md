---
title: レスポンシブ画像ライブラリの使用
description: レスポンシブ画像ライブラリをweb ページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
TQID: 'https://experienceleague.adobe.com/06qs3B4mQcS7CSQs46RYnhTTpSa2xONlzN4Nfg0oU0g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 567
ht-degree: 0%

---

# レスポンシブ画像ライブラリの使用{#using-responsive-image-library}

レスポンシブ画像ライブラリをweb ページに追加し、ライブラリを使用して既存の画像を管理するには、次の手順を実行します。

**レスポンシブ画像ライブラリを使用するには**

1. Dynamic Media Classicでは、[&#x200B; プリセットでレスポンシブ画像ライブラリを使用する予定がある場合に備えて、画像プリセット &#x200B;](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html?lang=ja#image-sizing)を作成します。

   レスポンシブ画像ライブラリで使用する画像プリセットを定義する場合は、`wid=`、`hei=`、`scl=`など、画像サイズに影響を与える設定は使用しないでください。 画像プリセットでは、サイズフィールドを指定しないでください。 代わりに、空白の値のままにします。
1. ライブラリのJavaScript ファイルをweb ページに追加します。

   ライブラリ APIを使用する前に、必ず`responsive_image.js`を含めてください。 このJavaScript ファイルは、標準のIS-Viewers デプロイメントの`libs/` サブフォルダーにあります。

   `<s7viewers_root>/libs/responsive_image.js`
1. 既存の画像を設定する。

   ライブラリは、作業中の画像インスタンスから特定の設定属性を読み取ります。 `s7responsiveImage` API関数が呼び出される前に属性を定義します。

   また、既存の画像URLを`data-src`属性に入れることも推奨されます。 次に、既存の`src`属性を設定して、1x1 GIF イメージをData URIとしてエンコードするように設定します。 これにより、読み込み時にweb ページによって送信されるHTTP リクエストの数が減少します。 ただし、SEO （検索エンジン最適化）が必要な場合は、画像インスタンスに`title`属性を設定することをお勧めします。


   次に、画像の`data-breakpoints`属性を定義し、Data URIとしてエンコードされた1x1 GIFを使用する例を示します。

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```


1. ライブラリが管理するすべての画像インスタンスに対して`s7responsiveImage` API関数を呼び出します。

   ライブラリが管理するすべての画像インスタンスに対して`s7responsiveImage` API関数を呼び出します。 この呼び出しの後、ライブラリは、元の画像を、web ページレイアウトの`IMG`要素のランタイムサイズとデバイス画面の密度に従って、画像サービングからダウンロードされた画像に置き換えます。

   次のコードは、`responsiveImage`がその画像のIDであると仮定して、画像で`s7responsiveImage` API関数を呼び出す例です。

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## 例 {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

ライブラリでは、web ページ上の多数の画像インスタンスを同時に操作できます。 したがって、ライブラリを管理する各画像について、上記の手順1と2を繰り返します。

画像エレメントのスタイルを設定して、サイズを柔軟にするのはweb ページの責任です。 レスポンシブ画像ライブラリ自体は、固定サイズ画像と「可変」画像を区別しません。 固定サイズの画像に適用した場合、新しい画像は1回だけ読み込まれます。


次のコードは、レスポンシブ画像ライブラリによって管理される1つのフルード画像を持つ面倒なweb ページの完全な例です。 この例には、web ブラウザーのウィンドウサイズに合わせて画像を「レスポンシブ」にする追加のCSS スタイルが含まれています。

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

AEM 6.4とDynamic Media Viewers 5.9では、次の2つのスマート切り抜きモードを利用できます。

* **手動** - ユーザー定義のブレークポイントと対応するImage Service コマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** – 計算されたスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。 最適なレンディションは、画像エレメントのランタイムサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode`属性を`smart crop`に設定します。 以下に例を挙げます。

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連付けられた画像要素は、ブレークポイントが変更されたときに、ランタイム中に`s7responsiveViewer` イベントをディスパッチします。

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
