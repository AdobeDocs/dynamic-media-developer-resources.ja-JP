---
description: 構成属性は、レスポンシブ画像ライブラリが管理するIMG要素に直接属性として定義されます。 各画像には、それぞれ独自の属性セットを設定できます。
solution: Experience Manager
title: コマンドリファレンス – 設定属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
TQID: 'https://experienceleague.adobe.com/nOar-x6dy8Z9czsPjxlOzin8WJTnt26b3Lv32voi5e8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 504
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

構成属性は、レスポンシブ画像ライブラリが管理するIMG要素に直接属性として定義されます。 各画像には、それぞれ独自の属性セットを設定できます。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

オプション。

画像サービングが提供する画像へのURL。 URLが存在しない場合、ライブラリは`src`属性で設定された値をフォールバックとして使用します。 この属性は、レスポンシブ画像ライブラリが異なる場所から管理する初期画像と動的画像を提供します。

**例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```


## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

`data-src`が設定されている場合、`src`はオプションであり、追加する任意のURLを含めることができます。 例えば、ライブラリが使用するのと同じ画像サービングベースの画像へのURLを含めることができます。 また、起動時にサーバーのラウンドトリップを回避するために、GIF プレースホルダーやデータ URIを含めることもできます。

`data-src`が設定されていない場合、`src`は必須であり、画像サービングが提供する画像のURLを含める必要があります。


**例**

`src`属性にデータ URIを使用し、`data-src`属性に画像サービング URLを使用：

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```


## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

ブレークポイントのコンマ区切りリスト。オプションでコロン（`:`）、画像サービングコマンドまたは画像プリセットが続きます。 各ブレークポイントは、論理CSS ピクセルで定義された画像幅の値です。 ライブラリは、リストから最も大きい値の画像を読み込み、ランタイム CSSの画像幅に合わせてクライアント上で画像をダウンスケールします。 （高密度の画面で作業する場合、サーバーから読み込まれた画像レンディションは、デバイスのピクセル比を掛けたブレークポイント値を表します）。

リストの任意のブレークポイントに対して、1つ以上の画像サービングコマンドまたは画像プリセット名を定義できます。 このような追加パラメーターは、この特定のブレークポイントが現在アクティブな場合にのみ画像に適用されます。

サポートされている画像サービングコマンドを使用できますが、`wid=`、`hei=`、`scl=`など、応答の画像サイズに影響を与えるビューコマンドは使用できません。 同じ制限が画像プリセットにも適用されます。レスポンシブ画像ライブラリで使用される画像プリセットには、このようなコマンドを含めないでください。

複数の画像サービングコマンドまたは画像プリセット名は、「`&`」文字で区切られます。 画像サービングコマンドの値にコンマが含まれている場合、そのようなコンマは`%2C`に置き換えられます。 画像プリセット名は、ドル記号（`$`）で囲まれます。


**例**

**ブレークポイントのみを使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**画像プリセットの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**画像プリセットと画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`



## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4以降およびDynamic Media Viewers 5.9以降では、次の2つのスマート切り抜きモードを使用できます。

* **手動** - ユーザー定義のブレークポイントと対応するImage Service コマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** – 計算されたスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。 最適なレンディションは、画像エレメントのランタイムサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode`属性を`smart crop`に設定します。

**例**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連付けられた画像要素は、ブレークポイントが変更されたときに、ランタイム中に`s7responsiveViewer` イベントをディスパッチします。

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
