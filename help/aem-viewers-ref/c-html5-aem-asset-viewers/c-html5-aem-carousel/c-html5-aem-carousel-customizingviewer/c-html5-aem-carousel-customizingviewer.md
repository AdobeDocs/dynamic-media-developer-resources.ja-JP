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
workflow-type: tm+mt
source-wordcount: '1356'
ht-degree: 0%

---


# カルーセルビューアのカスタマイズ{#customizing-carousel-viewer}

カルーセルビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローとして、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を`style=`コマンドで指定します。

初期設定のCSSファイルは、次の場所にあります。

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

このビューアには、数値と点線の設定インジケーター用の、あらかじめ用意されている4つのCSSファイルが付属しており、それぞれ「明」と「暗」のカラースキームで表示されます。 初期設定では「Dotted light」バージョンが使用されますが、異なる標準CSSを使用し、`SetIndicator.mode`パラメーターを設定することで、別のバージョンに簡単に切り替えることができます。 その他の標準的なCSSは、次の場所にあります。

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

カスタムのCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正常に機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素に`.s7carouselviewer`クラスを割り当てることに注意してください。 `style=`コマンドによって渡された外部CSSファイルを使用する場合は、CSSルールの子孫セレクターで`.s7carouselviewer`クラスを親クラスとして使用します。 Webページ上に埋め込みスタイルを追加する場合、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7carouselviewer`

## レスポンシブデザインCSSの構築{#section-0bb49aca42d242d9b01879d5ba59d33b}

CSSで様々なデバイスや埋め込みサイズをターゲットして、ユーザーのデバイスや特定のWebページのレイアウトに応じてコンテンツの表示を変えることができます。 例えば、レイアウト、ユーザインターフェイス要素のサイズおよびアートワークの解像度を変えることができます。

ビューアでは、レスポンシブデザインCSSの作成メカニズムが2つサポートされています。CSSマーカーと標準のCSSメディアクエリ これらは、個別にも、一緒にも使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成に役立つように、ビューアではCSSマーカーがサポートされています。 これらは、最上位レベルのビューアコンテナ要素に動的に割り当てられる特殊なCSSクラスです。 これらは、実行時のビューアのサイズと、現在のデバイスで使用されている入力タイプに基づきます。

CSSマーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small`の各クラスが含まれます。 これらは、ビューアコンテナの実行時の領域に基づいて適用されます。 例えば、ビューアの領域が一般的なデスクトップモニターと同じかそれ以上である場合は、`.s7size_large`を使用します。 領域が共通のタブレットデバイスに近い場合は、`.s7size_medium`を割り当てます。 携帯電話の画面に似た領域の場合は、`.s7size_small`を使用します。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、`.s7mouseinput`と`.s7touchinput`が含まれます。 現在のデバイスがタッチ入力に対応している場合、CSSマーカー`.s7touchinput`が設定されます。 それ以外の場合は、`.s7mouseinput`が使用されます。 これらのマーカーは、主に、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを意図しています。通常は、タッチ入力にはより大きな要素が必要だからです。

以下のサンプルCSSでは、ズームインボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに設定し、タッチ入力デバイスでは56 x 56ピクセルに設定します。 ビューアのサイズをさらに小さくする場合は、20 x 20ピクセルに設定します。

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

ピクセル密度の異なるターゲットデバイスをデバイスに適用するには、CSSメディアクエリを使用する必要があります。 以下のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

レスポンシブデザインCSSを構築する最も柔軟性の高い方法は、CSSマーカーを使用することです。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットできるので、レスポンシブデザインレイアウトに便利です。

初期設定のビューアCSSファイルを、CSSマーカーアプローチの例として使用できます。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用して行うこともできます。 特定のメディアクエリブロック内に含まれるすべては、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用される場合、4つのCSSメディアクエリが使用されます。これらのメディアはCSS内で次に示す順に定義されます。

1. すべてのタッチデバイスに固有のルールのみを含める。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 高解像度画面のタブレットに固有のルールのみを含める。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. すべての携帯電話に固有のルールのみを含める。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 高解像度画面の携帯電話に固有のルールのみを含める。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

メディアクエリアプローチを使用する場合は、デバイス検出機能を持つCSSを次のように整理する必要があります。

* まず、デスクトップに固有のセクションを記述し、デスクトップに固有またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4つのメディアクエリを上記の定義の順に並べ、対応するデバイスタイプに固有のCSSルールを指定します。

各メディアクエリでビューアのCSS全体を重複する必要はありません。 特定のデバイスに固有のプロパティのみがメディアクエリ内で再定義されます。

## CSSスプライト{#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例として、通常は少なくとも3つの状態を持つボタンがあります。`up`、`over`、`down`。 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSはユーザインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 以下は、ズームインボタンのスタイル設定に使用するCSSの例です。

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

このアプローチの欠点は、エンドユーザーが要素との初回のインタラクション時にちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出しの数が増えたので、パフォーマンスに若干悪影響を及ぼす場合があります。

CSSスプライトは、異なるアプローチで、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合します。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザーインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して、同じスプライト画像が参照されます。 また、`background-position`プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に並べられます。

以下は、「スプライト」ベースの同じホットスポットアイコンのスタイル設定例です。

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## スタイルに関する一般的な注意とアドバイス{#section-95855dccbbc444e79970f1aaa3260b7b}

* CSSでビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のスタイル設定に`!IMPORTANT`ルールの使用はサポートされていません。 特に、`!IMPORTANT`ルールは、ビューアまたはビューアSDKが提供するデフォルトのスタイルまたは実行時のスタイルを上書きする場合には使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、CSSセレクターを適切な仕様で使用して、このビューアリファレンスガイドに記載されているCSSプロパティを設定する必要があります。
* CSS内で指定されている外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、この点に注意してください。 初期設定のアセットもコピーするか、カスタムCSS内のすべてのパスを更新します。
* ビットマップアートワークの推奨される形式はPNGです。
* ビットマップアートワークは、`background-image`プロパティを使用してユーザインターフェイス要素に割り当てます。
* ユーザーインターフェイス要素の`width`プロパティと`height`プロパティは、論理サイズを定義します。 `background-image`に渡されるビットマップのサイズは、論理サイズに影響しません。
* Retinaなど高ピクセル密度の高解像度画面を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、`-webkit-background-size:contain`プロパティを適用して、背景を、論理ユーザーインターフェイス要素のサイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、そのCSSクラスに`display:none`を追加します。
* カラー値には、CSSでサポートされている様々な形式を使用できます。 透明度が必要な場合は、`rgba(R,G,B,A)`の形式を使用します。 それ以外の場合は、`#RRGGBB`の形式を使用できます。

## 共通のユーザーインターフェイス要素{#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオ画像ビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
