---
description: カルーセルビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
keywords: responsive
seo-description: カルーセルビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
seo-title: カルーセルビューアのカスタマイズ
solution: Experience Manager
title: カルーセルビューアのカスタマイズ
topic: Dynamic media
uuid: a35dac3c-8785-42bf-8284-e400128f213c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# カルーセルビューアのカスタマイズ{#customizing-carousel-viewer}

カルーセルビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、コマンドでカスタマイズしたファイルの場所を指定すること `style=` です。

初期設定のCSSファイルは、次の場所にあります。

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

ビューアには、数値と点線の設定インジケーター用の、あらかじめ用意されている4つのCSSファイルが用意されており、それぞれが「明」と「暗」のカラースキームで表示されます。 初期設定では「Dotted light」バージョンが使用されますが、異なる標準CSSを使用し、パラメーターを設定することで、別のバージョンに簡単に切り替えることがで `SetIndicator.mode` きます。 その他の標準的なCSSは、次の場所にあります。

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

カスタムCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素にク `.s7carouselviewer` ラスを割り当てることに注意してください。 コマンドで渡された外部CSSファイルを使用する場合は、CSS `style=` ルールの子孫セレ `.s7carouselviewer` クターでクラスを親クラスとして使用します。 Webページに埋め込みスタイルを追加する場合は、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7carouselviewer`

## レスポンシブデザインCSSの構築 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSSで様々なデバイスや埋め込みサイズをターゲットにして、ユーザーのデバイスや特定のWebページのレイアウトに応じてコンテンツの表示を変えることができます。 例えば、レイアウト、ユーザインターフェイス要素のサイズ、アートワークの解像度などがあります。

ビューアでは、レスポンシブデザインCSSの作成メカニズムが2つサポートされています。CSSマーカーと標準のCSSメディアクエリ。 これらは、個別に、または一緒に使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成に役立つように、ビューアではCSSマーカーがサポートされています。 これらは、最上位のビューアコンテナ要素に動的に割り当てられる特殊なCSSクラスです。 これらは、実行時のビューアのサイズと、現在のデバイスで使用されている入力タイプに基づきます。

CSSマーカーの最初のグループには、、、 `.s7size_large`およびク `.s7size_medium`ラスが含ま `.s7size_small` れます。 これらは、ビューアコンテナの実行時の領域に基づいて適用されます。 例えば、ビューアの領域が一般的なデスクトップモニターのサイズと等しいか、それより大きい場合は、を使用しま `.s7size_large`す。 領域が一般的なタブレットデバイスに近い場合は、を割り当てま `.s7size_medium`す。 携帯電話の画面に似た領域の場合は、を使用しま `.s7size_small`す。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、とが含ま `.s7mouseinput` れま `.s7touchinput`す。 CSSマーカーは、現 `.s7touchinput` 在のデバイスがタッチ入力に対応している場合に設定されます。 それ以外の場合は、 `.s7mouseinput` が使用されます。 これらのマーカーは、通常、タッチ入力にはより大きな要素が必要なので、入力タイプごとに異なる画面サイズのユーザーインターフェイス入力要素を作成することを意図しています。

以下のサンプルCSSでは、ズームインボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに、タッチ入力デバイスでは56 x 56ピクセルに設定します。 ビューアのサイズがさらに小さい場合は、20 x 20ピクセルに設定されます。

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

ピクセル密度の異なるデバイスをターゲットにするには、CSSメディアクエリを使用する必要があります。 次のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSSマーカーの使用は、レスポンシブデザインCSSを構築する最も柔軟な方法です。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにできるので、これはレスポンシブデザインレイアウトに便利です。

初期設定のビューアのCSSファイルを、CSSマーカーアプローチの例として使用できます。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用して行うこともできます。 特定のメディアクエリブロック内に含まれるすべての要素は、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用される場合、CSSで次に示す順序で定義された4つのCSSメディアクエリが使用されます。

1. すべてのタッチデバイスに固有のルールのみを含みます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 高解像度画面のタブレットに固有のルールのみを含めます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. すべての携帯電話に固有のルールのみを含みます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 高解像度画面の携帯電話に固有のルールのみを含めます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

メディアクエリアプローチを使用する場合は、次のようにデバイス検出を行うCSSを整理する必要があります。

* まず、デスクトップ固有のセクションで、デスクトップ固有またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4つのメディアクエリを上記の定義の順に記述し、対応するデバイスタイプに固有のCSSルールを指定します。

各メディアクエリでビューアのCSS全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみがメディアクエリ内で再定義されます。

## CSSスプライト {#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアのユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例は、通常は少なくとも3つの異なる状態を持つボタンです。 `up`、、 `over`および `down`。 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSはユーザインターフェイス要素の状態ごとに、サーバ上の個々の画像ファイルに対する個別の参照を持ちます。 以下は、ズームインボタンのスタイル設定に使用するCSSの例です。

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

このアプローチの欠点は、エンドユーザーが、要素が初めて操作されたときに、ちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法は、サーバーへのHTTP呼び出しの数が増えたため、パフォーマンスに若干悪影響を与える可能性があります。

CSSスプライトは、すべての要素の状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合する別の方法です。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して同じスプライト画像が参照されます。 また、このプロ `background-position` パティは、「スプライト」画像のどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に積み重ねられます。

次に、「スプライト」ベースの同じホットスポットアイコンのスタイル設定例を示します。

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## スタイルに関する一般的な注意とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSSでビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のス `!IMPORTANT` タイル設定に対するルールの使用はサポートされていません。 特に、ビューアま `!IMPORTANT` たはビューアSDKが提供するデフォルトのスタイルや実行時のスタイルを上書きする際に、ルールを使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このビューアリファレンスガイドに記載されているCSSプロパティを設定するには、CSSセレクターを適切な仕様で使用する必要があります。
* CSS内の外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、このルールに注意してください。 初期設定のアセットもコピーするか、カスタムCSS内のすべてのパスを更新します。
* ビットマップアートワークに推奨される形式はPNGです。
* ビットマップアートワークは、このプロパティを使用してユーザインターフェイス要素に割り当 `background-image` てられます。
* ユーザイン `width` ターフ `height` ェイス要素の論理サイズは、およびプロパティで定義します。 に渡されるビットマップのサイズは、論 `background-image` 理サイズに影響を与えません。
* Retinaなどの高ピクセル密度の高解像度画面を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、このプロパティを適 `-webkit-background-size:contain` 用して、背景を論理ユーザインターフェイス要素のサイズに合わせて縮小します。
* ユーザーインターフェイスからボタンを削除するには、CSSク `display:none` ラスにを追加します。
* カラー値には、CSSでサポートされる様々な形式を使用できます。 透明度が必要な場合は、形式を使用しま `rgba(R,G,B,A)`す。 それ以外の場合は、形式を使用できま `#RRGGBB`す。

## 共通のユーザインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオ画像ビューアに適用されるユーザインターフェイス要素リファレンスドキュメントを次に示します。
