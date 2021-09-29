---
title: インタラクティブ画像ビューアのカスタマイズ
description: インタラクティブ画像ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: bb3cfe4a-ec60-4c10-82fe-9e4f8f7c586f
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# インタラクティブ画像ビューアのカスタマイズ{#customizing-interactive-image-viewer}

インタラクティブ画像ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定の CSS ファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

初期設定の CSS ファイルは次の場所にあります。

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

カスタムの CSS ファイルには、初期設定の CSS ファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正常に機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタム CSS ルールを指定する別の方法は、Web ページ上またはリンクされたいずれかの外部 CSS ルール内で、埋め込みスタイルを直接使用することです。

カスタム CSS を作成する場合、ビューアはコンテナの DOM 要素に `.s7interactiveimage` クラスを割り当てることに注意してください。 `style=` コマンドで渡された外部 CSS ファイルを使用する場合は、CSS ルールの子孫セレクターで `.s7interactiveimage` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを追加する場合は、次のようにコンテナの DOM 要素の ID を使用してこのセレクターを修飾します。

`#<containerId>.s7interactiveimage`

## レスポンシブデザイン CSS の構築 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSS で様々なデバイスや埋め込みサイズをターゲットにして、ユーザーのデバイスや特定の Web ページのレイアウトに応じて、コンテンツの表示を変えることができます。 この手法には、レイアウト、ユーザインターフェイス要素のサイズ、アートワークの解像度などが該当しますが、これらに限定されません。

ビューアでは、レスポンシブデザイン CSS の作成メカニズムが 2 つサポートされています。CSS マーカーと標準の CSS メディアクエリ。 これらのマーカーやクエリは、個別に使用することも、一緒に使用することもできます。

**CSS マーカー**

レスポンシブデザイン CSS を作成するのに役立つように、ビューアでは CSS マーカーがサポートされています。 これらのマーカーは、最上位のビューアのコンテナ要素に動的に割り当てられる特別な CSS クラスです。 実行時のビューアのサイズと、現在のデバイスで使用されている入力タイプに基づきます。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small` の各クラスが含まれます。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 例えば、ビューアの領域が一般的なデスクトップモニターと同じかそれ以上の場合は、`.s7size_large` を使用します。 領域が共通のタブレットデバイスに近い場合は、`.s7size_medium` を割り当てます。 携帯電話の画面に似た領域の場合は、`.s7size_small` を使用します。 これらの CSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 番目のグループには、`.s7mouseinput` と `.s7touchinput` が含まれます。 現在のデバイスにタッチ入力がある場合、CSS マーカー `.s7touchinput` が設定されます。 それ以外の場合は、`.s7mouseinput` が使用されます。 通常、タッチ入力にはより大きな要素が必要なので、これらのマーカーは、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを主目的としています。

次のサンプル CSS では、ズームインボタンのサイズを、マウス入力のシステムでは 28 x 28 ピクセルに設定し、タッチ入力デバイスでは 56 x 56 ピクセルに設定します。 ビューアのサイズがさらに小さい場合は、20 x 20 ピクセルに設定されます。

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

ピクセル密度が異なるデバイスをターゲットにするには、CSS メディアクエリを使用する必要があります。 次のメディアクエリブロックには、高密度画面に固有の CSS が含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

レスポンシブデザイン CSS を構築する最も柔軟な方法は、CSS マーカーを使用することです。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにでき、レスポンシブデザインのレイアウトに役立ちます。

初期設定のビューア CSS ファイルを、CSS マーカーアプローチの例として使用できます。

**CSS メディアクエリ**

デバイスの検出は、純粋な CSS メディアクエリを使用しておこなうこともできます。 特定のメディアクエリブロック内に含まれるすべての要素は、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合、4 つの CSS メディアクエリが使用されます。これらは CSS 内で以下の順に定義されます。

1. すべてのタッチデバイスに固有のルールのみを含む。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 高解像度の画面を含むタブレットに固有のルールのみを含めます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. すべての携帯電話に固有のルールのみを含む。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 高解像度画面の携帯電話に固有のルールのみを含みます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

メディアクエリアプローチを使用する場合、デバイス検出をおこなう CSS を次のように整理する必要があります。

* まず、デスクトップ固有のセクションで、デスクトップに固有のプロパティまたはすべての画面に共通のプロパティをすべて定義します。
* 次に、4 つのメディアクエリを上記の定義の順に記述し、対応するデバイスタイプに固有の CSS ルールを指定します。

各メディアクエリでビューアの CSS 全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSS スプライト {#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイルを設定し、複数の異なる表示状態を持ちます。 良い例は、通常、少なくとも 3 つの異なる状態を持つボタンです。`up`、`over`、および `down`。 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定アプローチでは、CSS は、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 次に、ズームインボタンのスタイル設定に使用する CSS の例を示します。

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

このアプローチの欠点は、要素が初めてでインタラクションを受けると、エンドユーザーがユーザーインターフェイスの応答がちらつく、または遅れるということです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法では、サーバーへの HTTP 呼び出しの数が増えるので、パフォーマンスに若干悪影響を与える場合があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる別のアプローチです。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSS 内のすべての異なる状態に対して、同じスプライト画像が参照されます。 また、`background-position` プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態で使用されます。 「スプライト」イメージは、適切な方法で構築できます。 通常、ビューアは垂直方向に積み重ねられます。

以下は、前述の「スプライト」ベースの同じズームインボタンのスタイル設定例です。

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## スタイルに関する一般的な注意とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS を使用してビューアのユーザインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールを使用してビューア要素のスタイルを設定することはできません。 特に、`!IMPORTANT` ルールを使用して、ビューアまたはビューア SDK が提供するデフォルトのスタイルや実行時のスタイルを上書きしないでください。 この理由は、適切なコンポーネントの動作に影響を与える可能性があるからです。 代わりに、CSS セレクターを適切な特異性で使用して、このビューアリファレンスガイドに記載されている CSS プロパティを設定する必要があります。
* CSS 内で指定されている外部アセットへのパスは、ビューアの HTML ページの場所ではなく、CSS の場所を基準に解決されます。 初期設定の CSS を別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタム CSS 内のすべてのパスを更新します。
* ビットマップアートワークの推奨される形式は PNG です。
* ビットマップアートワークは、 `background-image` プロパティを使用してユーザインターフェイス要素に割り当てます。
* ユーザーインターフェイス要素の `width` プロパティと `height` プロパティで論理サイズを定義します。 `background-image` に渡されたビットマップのサイズは、論理サイズに影響しません。
* Retina のような高解像度画面の高ピクセル密度を使用するには、論理ユーザインターフェイス要素の 2 倍の大きさのビットマップアートワークを指定します。 次に、 `-webkit-background-size:contain` プロパティを適用して、背景を、論理ユーザインターフェイス要素のサイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、その CSS クラスに `display:none` を追加します。
* カラーの値には、CSS でサポートされている様々な形式を使用できます。 透明度が必要な場合は、`rgba(R,G,B,A)` の形式を使用します。 それ以外の場合は、`#RRGGBB` の形式を使用できます。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオ画像ビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
