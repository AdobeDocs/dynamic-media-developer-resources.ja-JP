---
description: 設定属性は、レスポンシブ画像ライブラリで管理されるIMG要素で直接属性として定義されます。 各画像には、独自の属性セットを設定できます。
seo-description: 設定属性は、レスポンシブ画像ライブラリで管理されるIMG要素で直接属性として定義されます。 各画像には、独自の属性セットを設定できます。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Scene7 Image Serving - Image Rendering API
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

設定属性は、レスポンシブ画像ライブラリで管理されるIMG要素で直接属性として定義されます。 各画像には、独自の属性セットを設定できます。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

（オプション）

画像サービングが提供する画像のURL。 URLが存在しない場合、ライブラリはフォールバックとして属性に設定された値 `src` を使用します。 この属性は、レスポンシブ画像ライブラリが管理する初期画像と動的画像を様々な場所から提供します。

**例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

が設 `data-src` 定されて `src` いる場合、はオプションで、追加する任意のURLを含めることができます。 例えば、ライブラリで使用されているのと同じ画像サービングベースの画像のURLを含めることができます。 また、GIFプレースホルダーを含めたり、データURIを含めたりして、起動時に余分なサーバーのラウンドトリップを防ぐことができます。

が設定 `data-src` されていない場 `src` 合、は必須で、画像サービングが提供する画像のURLを含める必要があります。

**例**

属性にデータURIを使用 `src` し、属性に画像サービングURLを使用 `data-src` する：

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## データブレークポイント {#section-3bf62a89ff3e40569848c1fe3ac7886c}

ブレークポイントのコンマ区切りのリスト。オプションでコロン( `:`)、画像サービングコマンドまたは画像プリセットを後に付けます。 各ブレークポイントは、論理CSSピクセルで定義される画像の幅の値です。 ライブラリは、最も近い大きい値を持つ画像をリストから読み込み、実行時のCSS画像の幅に合わせてクライアント上で縮小します。 （高密度の画面で作業する場合、サーバから読み込まれた画像レンディションは、ブレークポイント値にデバイスのピクセル比を掛けた値を表します）。

リスト内の任意のブレークポイントに対して、1つ以上の画像サービングコマンドまたは画像プリセット名を定義できます。 このような追加のパラメーターは、この特定のブレークポイントが現在アクティブな場合にのみ、イメージに適用されます。

応答画像のサイズ（、など）に影響するビューコマンドを除き、サポートされている任意の画像サービングコマンドを使 `wid=`用で `hei=`きま `scl=`す。 同じ制限が画像プリセットにも適用されます。レスポンシブ画像ライブラリで使用する画像プリセットに、このようなコマンドを含めることはできません。

複数の画像サービングコマンドまたは画像プリセット名は、「」文字で区 `&`切られます。 画像サービングコマンドの値にコンマが含まれている場合、このコンマはに置き換えられま `%2C`す。 画像プリセット名はドル記号( `$`)で囲まれます。

**例**

**ブレークポイントのみの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**画像プリセットの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**画像プリセットと画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## データモード {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

次の2つのスマート切り抜きモードは、AEM 6.4以降およびScene7ビューア5.9以降で使用できます。

* **手動** — ユーザ定義のブレークポイントと、対応する画像サービスコマンドは、画像要素の属性内で定義されます。
* **スマート切り抜き** — 計算済みのスマート切り抜きレンディションが、配信サーバーから自動的に取得されます。 最適なレンディションは、画像要素の実行時のサイズを使用して選択されます。

スマート切り抜きモードを使用するには、属性をに `data-mode` 設定しま `smart crop`す。

**例**

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

