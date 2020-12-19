---
description: 'null'
keywords: responsive
seo-description: 'null'
seo-title: フライアウトビューアのカスタマイズ
solution: Experience Manager
title: フライアウトビューアのカスタマイズ
topic: Dynamic media
uuid: 10b5caa4-5298-43fa-af86-4f0b77be967b
translation-type: tm+mt
source-git-commit: 8d7fdab78c5d23d0e541effa9b9c470921bd144b
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---


# フライアウトビューアのカスタマイズ{#customizing-flyout-viewer}

すべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローとして、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を`style=`コマンドで指定します。

初期設定のCSSファイルは、次の場所にあります。

`<s7_viewers_root>/html5/FlyoutViewer.css`

カスタムのCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正常に機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素に`.s7flyoutviewer`クラスを割り当てることに注意してください。 `style=`コマンドによって渡された外部CSSファイルを使用する場合は、CSSルールの子孫セレクターで`.s7flyoutviewer`クラスを親クラスとして使用します。 Webページ上で埋め込みスタイルを使用する場合、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7flyoutviewer`

## レスポンシブデザインCSSの構築{#section-c1e74f5114ad418884ca1c95f5ea5b63}

CSSで様々なデバイスや埋め込みサイズをターゲットして、ユーザーのデバイスや特定のWebページのレイアウトに応じてコンテンツの表示を変えることができます。 例えば、Webページのレイアウト、ユーザインターフェイス要素のサイズ、アートワークの解像度を変えることができます。

ビューアでは、レスポンシブデザインCSSの作成方法が2つサポートされています。CSSマーカーと標準のCSSメディアクエリ これらの方法は、個別にも、一緒にも使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成に役立つように、ビューアでは、CSSマーカーがサポートされています。このCSSマーカーは、実行時のビューアサイズと現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられます。

CSSマーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small`の各クラスが含まれます。 これらは、ビューアコンテナの実行時の領域に基づいて適用されます。 つまり、ビューアの領域が一般的なデスクトップモニター`.s7size_large`と同じかそれ以上である場合、領域のサイズが一般的なタブレットデバイス`.s7size_medium`に近い場合は、&lt;a1/>が割り当てられます。 携帯電話の画面に似た領域に対しては`.s7size_small`が設定される。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、`.s7mouseinput`と`.s7touchinput`が含まれます。 `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合 `.s7mouseinput` は、が使用されます。これらのマーカーは、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを目的としています。通常は、タッチ入力にはより多くの要素が必要なためです。 デバイスにマウス入力とタッチの両方の機能がある場合は、`.s7touchinput`が設定され、ビューアはタッチに対応したユーザーインターフェイスをレンダリングします。

以下のサンプルCSSでは、ズームインボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに設定し、タッチデバイスでは56 x 56ピクセルに設定します。 また、ビューアのサイズが非常に小さくなると、ボタンは完全に非表示になります。

```
.s7flyoutviewer.s7mouseinput .s7swatches .s7thumb {  
 width: 28px; 
 height: 28px; 
} 
.s7flyoutviewer.s7touchinput .s7swatches .s7thumb {  
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer.s7size_small .s7swatches {  
 visibility: hidden; 
}
```

ピクセル密度が異なるデバイスをターゲットするには、CSSメディアクエリを使用します。 以下のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSSマーカーを使用すると、レスポンシブデザインCSSを構築する最も柔軟性の高い方法です。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットできます。これはレスポンシブデザインWebページレイアウトに便利です。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用して行うこともできます。 特定のメディアクエリブロック内に含まれるすべては、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用される場合は、4つのCSSメディアクエリが使用されます。これらのメディアはCSS内で次の順序で定義されます。

1. すべてのタッチデバイスに固有のルールのみを含める。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

## CSSスプライト{#section-0711ece44a4740168cfd7624c9010bd1}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例として、通常は少なくとも3つの状態を持つボタンが挙げられます。「up」、「over」および「down」 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSはユーザインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 以下は、スクロールボタンのスタイル設定に使用するCSSの例です。

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-image:url(images/v2/ScrollLeftButton_up.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-image:url(images/v2/ScrollLeftButton_down.png);  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-image:url(images/v2/ScrollLeftButton_disabled.png);  
}
```

このアプローチの欠点は、エンドユーザーが要素との初回のインタラクション時にちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出しの数が増えたので、パフォーマンスに若干悪影響を及ぼす場合があります。

CSSスプライトは、異なるアプローチで、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合します。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザーインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して、同じスプライト画像が参照されます。 また、`background-position`プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に並べられます。 下の例は、「スプライト」ベースの、上から同じスクロールボタンのスタイル設定例です。

```
.s7flyoutviewer .s7scrollleftbutton[state]  { 
    background-image: url(images/v2/ScrollLeftButton_light_sprite.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{  
background-position: -56px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{  
background-position: -0px -504px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{  
background-position: -56px -448px;  
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{  
background-position: -0px -448px;  
}
```

## スタイルに関する一般的な注意とアドバイス{#section-95855dccbbc444e79970f1aaa3260b7b}

* CSSでビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のスタイル設定に`!IMPORTANT`ルールの使用はサポートされていません。 特に、`!IMPORTANT`ルールは、ビューアまたはビューアSDKが提供するデフォルトまたは実行時のスタイル設定を上書きする場合には使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、CSSセレクターを適切な仕様で使用して、このリファレンスガイドに記載されているCSSプロパティを設定する必要があります。
* CSS内で指定されている外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、この点に注意してください。 初期設定のアセットもコピーするか、カスタムCSS内でパスを更新します。
* ビットマップアートワークの推奨される形式はPNGです。
* ビットマップアートワークは、`background-image`プロパティを使用してユーザインターフェイス要素に割り当てます。
* ユーザーインターフェイス要素の`width`プロパティと`height`プロパティは、論理サイズを定義します。 `background-image`に渡されるビットマップのサイズは論理サイズに影響しません。
* Retinaなど高ピクセル密度の高解像度画面を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、`-webkit-background-size:contain`プロパティを適用して、背景を、論理ユーザーインターフェイス要素のサイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、そのCSSクラスに`display:none`を追加します。
* カラー値には、CSSでサポートされている様々な形式を使用できます。 透明度が必要な場合は、`rgba(R,G,B,A)`の形式を使用します。 それ以外の場合は、`#RRGGBB`の形式を使用できます。

## 共通のユーザーインターフェイス要素{#section-d6330c9be8c444aa9b2a07886e3dbc2a}

フライアウトビューアに適用されるユーザインターフェイス要素リファレンスドキュメントを次に示します。

* [フライアウトズーム表示](r-html5-flyout-viewer-20-customize-flyoutzoomview.md)
* [フォーカスハイライト](r-html5-flyout-viewer-20-customize-focushighlight.md)
* [メインビューア領域](r-html5-flyout-viewer-20-customize-mainviewerarea.md)
* [スウォッチ](r-html5-flyout-viewer-20-customize-swatches.md)
* [ツールチップ](r-html5-flyout-viewer-20-customize-tooltips.md)
