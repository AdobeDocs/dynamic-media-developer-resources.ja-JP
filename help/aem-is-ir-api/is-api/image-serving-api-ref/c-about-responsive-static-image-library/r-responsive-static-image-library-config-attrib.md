---
description: 設定属性は、レスポンシブ画像ライブラリが管理する IMG 要素に対して直接属性として定義されます。 各画像には、独自の属性セットを設定できます。
solution: Experience Manager
title: コマンドリファレンス – 設定属性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

設定属性は、レスポンシブ画像ライブラリが管理する IMG 要素に対して直接属性として定義されます。 各画像には、独自の属性セットを設定できます。

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

オプション。

画像サービングが提供する画像への URL。 URL が存在しない場合、ライブラリはフォールバックとして属性に設定された値 `src` 使用します。 この属性は、初期画像と、レスポンシブ画像ライブラリが様々な場所から管理する動的画像を提供します。

**例**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

`data-src` が設定されている場合、`src` はオプションであり、追加する任意の URL を含めることができます。 例えば、ライブラリが使用するのと同じ画像サービングベースの画像への URL を含めることができます。 また、起動時に追加のサーバーラウンドトリップを避けるために、GIFプレースホルダーやデータ URI を含めることもできます。

`data-src` が設定されていない場合、`src` は必須であり、画像サービングが提供する画像への URL を含める必要があります。

**例**

`src` 属性にデータ URI を使用し、`data-src` 属性に画像サービング URL を使用します。

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoint {#section-3bf62a89ff3e40569848c1fe3ac7886c}

ブレークポイントのコンマ区切りリスト。オプションで、その後にコロン（`:`）と画像サービングコマンドまたは画像プリセットを付けることができます。 各ブレークポイントは、論理 CSS ピクセルで定義された画像の幅の値です。 ライブラリは、リストから最も近い値で画像を読み込み、ランタイム CSS 画像幅に一致するように、クライアント上で画像をダウンスケールします。 （高密度の画面で作業する場合、サーバーから読み込まれる画像レンディションは、ブレークポイント値にデバイスのピクセル比を掛けた値を表します）。

リストの任意のブレークポイントに対して、1 つ以上の画像サービングコマンドまたは画像プリセット名を定義できます。 このような追加のパラメーターは、この特定のブレークポイントが現在アクティブな場合にのみ、画像に適用されます。

`wid=`、`hei=`、`scl=` など、応答画像のサイズに影響する表示コマンドを除き、サポートされている任意の画像サービングコマンドを使用できます。 画像プリセットにも同じ制限が適用されます。レスポンシブ画像ライブラリで使用する画像プリセットには、このようなコマンドを含めないでください。

複数の画像サービングコマンドまたは画像プリセット名は、「`&`」文字で区切られています。 画像サービングコマンドの値にコンマが含まれている場合、そのコンマは `%2C` に置き換えられます。 画像プリセット名はドル記号（`$`）で囲まれます。

**例**

**ブレークポイントのみ使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**画像プリセットの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**画像プリセットおよび画像サービングコマンドの使用**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## data-mode {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

AEM 6.4 以降およびDynamic Media Viewers 5.9 以降では、次の 2 つのスマート切り抜きモードを使用できます。

* **手動** - ユーザー定義のブレークポイントと、対応する画像サービスコマンドは、画像要素の属性内で定義します。
* **スマート切り抜き** – 計算されたスマート切り抜きレンディションは、配信サーバーから自動的に取得されます。 最適なレンディションは、画像要素のランタイムサイズを使用して選択されます。

スマート切り抜きモードを使用するには、`data-mode` 属性を `smart crop` に設定します。

**例**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

関連する画像要素は、ブレークポイントが変更されたときに、実行時に `s7responsiveViewer` イベントをディスパッチします。

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
