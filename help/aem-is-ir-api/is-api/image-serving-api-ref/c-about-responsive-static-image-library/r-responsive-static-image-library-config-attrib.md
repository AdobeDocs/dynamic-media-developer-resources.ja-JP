---
description: 設定属性は、レスポンシブ画像ライブラリが管理するIMG要素で直接属性として定義されます。 各画像には、独自の属性セットを設定できます。
seo-description: 設定属性は、レスポンシブ画像ライブラリが管理するIMG要素で直接属性として定義されます。 各画像には、独自の属性セットを設定できます。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

設定属性は、レスポンシブ画像ライブラリが管理するIMG要素で直接属性として定義されます。 各画像には、独自の属性セットを設定できます。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

（オプション）

画像サービングが提供する画像のURL。 URLが存在しない場合、ライブラリはフォールバックとして`src`属性に設定された値を使用します。 この属性は、レスポンシブ画像ライブラリが管理する初期画像と動的画像を様々な場所で提供します。

**例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

`data-src`が設定されている場合、`src`はオプションで、追加する任意のURLを含めることができます。 例えば、ライブラリで使用されているのと同じ画像サービングベースの画像へのURLを含めることができます。 また、GIFプレースホルダーを含めたり、データURIを含めたりして、起動時に余分なサーバーのラウンドトリップを回避することもできます。

`data-src`が設定されていない場合、`src`は必須で、画像サービングが提供する画像のURLを含める必要があります。

**例**

`src`属性にデータURIを、`data-src`属性に画像サービングURLを使用します。

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

ブレークポイントのカンマ区切りのリスト。オプションでコロン(`:`)と画像サービングコマンドまたは画像プリセットを付けます。 各ブレークポイントは、論理CSSピクセルで定義される画像の幅の値です。 ライブラリは、リストから最も近い大きい値で画像を読み込み、ランタイムCSS画像の幅に合わせてクライアント上で縮小します。 （高密度の画面で作業する場合、サーバから読み込まれた画像レンディションは、ブレークポイント値にデバイスのピクセル比を乗じた値を表します）。

リストの任意のブレークポイントに対して、1つ以上の画像サービングコマンドまたは画像プリセット名を定義できます。 このような追加のパラメーターは、この特定のブレークポイントが現在アクティブな場合にのみ、イメージに適用されます。

`wid=`、`hei=`、`scl=`など、応答画像のサイズに影響する表示コマンドを除き、サポートされている任意の画像サービングコマンドを使用できます。 画像プリセットにも同じ制限が適用されます。レスポンシブ画像ライブラリで使用される画像プリセットにこのようなコマンドを含めることはできません。

複数の画像サービングコマンドまたは画像プリセット名は、「`&`」文字で区切られます。 画像サービングコマンドの値にカンマが含まれている場合、このようなカンマは`%2C`に置き換えられます。 画像プリセット名はドル記号(`$`)で囲まれます。

**例**

**ブレークポイントのみの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**画像プリセットの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**画像プリセットおよび画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4以降とDynamic Mediaビューア5.9以降では、次の2つのスマート切り抜きモードを使用できます。

* **手動**  — ユーザー定義のブレークポイントおよび対応する画像サービスコマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** ：計算済みのスマート切り抜きレンディションは、配信サーバから自動的に取得されます。最適なレンディションは、画像要素の実行時のサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode`属性を`smart crop`に設定します。

**例**

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

