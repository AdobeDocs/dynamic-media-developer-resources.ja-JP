---
description: 設定属性は、レスポンシブ画像ライブラリが管理するIMG要素に直接属性として定義されます。 各画像には、独自の属性セットを設定できます。
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 1%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

設定属性は、レスポンシブ画像ライブラリが管理するIMG要素に直接属性として定義されます。 各画像には、独自の属性セットを設定できます。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

（オプション）

画像サービングが提供する画像のURL。 URLが存在しない場合、ライブラリはフォールバックとして`src`属性に設定された値を使用します。 この属性は、レスポンシブ画像ライブラリが様々な場所から管理する初期画像と動的画像を提供します。

**例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

`data-src`が設定されている場合、`src`はオプションで、追加する任意のURLを含めることができます。 例えば、ライブラリが使用するのと同じ画像サービングベースの画像へのURLを含めることができます。 また、GIFプレースホルダーやデータURIを含めて、起動時に余分なサーバーのラウンドトリップを回避することもできます。

`data-src`が設定されていない場合、`src`は必須で、画像サービングが提供する画像のURLを含める必要があります。

**例**

`src`属性のデータURIと`data-src`属性の画像サービングURLを使用します。

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

ブレークポイントのコンマ区切りリストと、必要に応じてコロン(`:`)、画像サービングコマンドまたは画像プリセットと続くリスト。 各ブレークポイントは、論理CSSピクセルで定義される画像の幅の値です。 ライブラリは、リストから最も大きい値で画像を読み込み、実行時のCSS画像の幅に合わせてクライアント上で縮小します。 （高密度の画面で作業する場合、サーバーから読み込まれる画像レンディションは、ブレークポイント値にデバイスのピクセル比を掛けた値を表します）。

リスト内のブレークポイントに対して、1つ以上の画像サービングコマンドまたは画像プリセット名を定義できます。 この特定のブレークポイントが現在アクティブな場合にのみ、追加のパラメーターが画像に適用されます。

`wid=`、`hei=`、`scl=`など、応答画像のサイズに影響する表示コマンドを除き、サポートされている任意の画像サービングコマンドを使用できます。 同じ制限が画像プリセットに適用されます。レスポンシブ画像ライブラリで使用する画像プリセットには、このようなコマンドを含めないでください。

複数の画像サービングコマンドまたは画像プリセット名は「`&`」文字で区切ります。 画像サービングコマンドの値にコンマが含まれている場合、そのコンマは`%2C`に置き換えられます。 画像プリセット名はドル記号(`$`)で囲まれます。

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

AEM 6.4以降およびDynamic Mediaビューア5.9以降では、次の2つのスマート切り抜きモードを使用できます。

* **手動**  — ユーザー定義のブレークポイントと対応する画像サービスコマンドは、画像要素の属性内で定義します。
* **スマート切り抜き**  — 計算済みのスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。最適なレンディションは、画像要素の実行時のサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode`属性を`smart crop`に設定します。

**例**

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
