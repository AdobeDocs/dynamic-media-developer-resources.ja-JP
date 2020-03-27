---
description: Video360ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
keywords: responsive
seo-description: Video360ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
seo-title: ビデオ360ビューアのカスタマイズ
solution: Experience Manager
title: ビデオ360ビューアのカスタマイズ
topic: Dynamic media
uuid: 1f021a11-856e-4bbc-a2ee-454ab0a60adb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ビデオ360ビューアのカスタマイズ{#customizing-video-viewer}

Video360ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、コマンドでカスタマイズしたファイルの場所を指定すること `style=` です。

初期設定のCSSファイルは、次の場所にあります。

`<s7_viewers_root>/html5/Video360Viewer_dark.css`

カスタムCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素にク `.s7video360viewer` ラスを割り当てることに注意してください。 コマンドで渡された外部CSSファイルを使用する場合 `style=` は、CSSルールの子 `.s7video360viewer` 孫セレクターでクラスを親クラスとして使用します。 Webページ上で埋め込みスタイルを使用する場合は、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7video360viewer`

## レスポンシブデザインCSSの構築 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSSで様々なデバイスや埋め込みサイズをターゲットにして、ユーザーのデバイスや特定のWebページのレイアウトに応じてコンテンツの表示を変えることができます。 例えば、レイアウト、ユーザインターフェイス要素のサイズ、アートワークの解像度などがあります。

ビューアでは、レスポンシブデザインCSSの作成メカニズムが2つサポートされています。CSSマーカーと標準のCSSメディアクエリ。 これらは、個別に、または一緒に使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成に役立つように、ビューアではCSSマーカーがサポートされています。 これらは、実行時のビューアのサイズと現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられる特殊なCSSクラスです。

CSSマーカーの最初のグループには、、、 `.s7size_large`および `.s7size_medium`クラスが含ま `.s7size_small` れます。 これらは、ビューアのコンテナの実行時の領域に基づいて適用されます。 ビューアの領域が一般的なデスクトップモニターと同じかそれ以上の場合は、が使 `.s7size_large` 用されます。領域が一般的なタブレットデバイスに近い場合は、が割り当 `.s7size_medium` てられます。 携帯電話の画面に似た領域に対しては、が設 `.s7size_small` 定されます。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、とが含ま `.s7mouseinput` れま `.s7touchinput`す。 `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合は、 `.s7mouseinput` が使用されます。 これらのマーカーは、通常、タッチ入力にはより大きな要素が必要なので、入力タイプごとに異なる画面サイズのユーザーインターフェイス入力要素を作成することを意図しています。 デバイスにマウス入力とタッチの両方の機能がある場合は、が設定され、 `.s7touchinput` ビューアによってタッチ操作に適したユーザインターフェイスがレンダリングされます。

以下のサンプルCSSでは、再生/一時停止ボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに、タッチデバイスでは56 x 56ピクセルに設定します。 また、ビューアのサイズが大幅に小さくなると、ボタンは完全に非表示になります。

```
.s7video360viewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7video360viewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7video360viewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

ピクセル密度の異なるデバイスをターゲットにするには、CSSメディアクエリを使用する必要があります。 次のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSSマーカーの使用は、レスポンシブデザインCSSを構築する最も柔軟な方法です。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにできるので、これはレスポンシブデザインレイアウトに便利です。

初期設定のビューアCSSファイルを、CSSマーカーアプローチの例として使用できます。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用して行うこともできます。 特定のメディアクエリブロック内に含まれるすべての要素は、対応するデバイスで実行された場合にのみ適用されます。

HTML5モバイルビューアに適用される場合、4つのCSSメディアクエリが使用されます。このクエリは、CSS内で次に示す順に定義されます。

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

多くのビューアのユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例は、通常は少なくとも3つの異なる状態を持つボタンです。「up」、「over」および「down」 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSは、ユーザインターフェイス要素の状態ごとに、サーバ上の個々の画像ファイルを個別に参照します。 次に、フルスクリーンボタンのスタイル設定用のCSSの例を示します。

```
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7video360viewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

このアプローチの欠点は、エンドユーザーが、要素が初めて操作されたときに、ちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法は、サーバーへのHTTP呼び出しの数が増えたため、パフォーマンスに若干悪影響を与える可能性があります。

CSSスプライトは、すべての要素の状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合する別の方法です。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して同じスプライト画像が参照されます。 また、このプロ `background-position` パティは、「スプライト」画像のどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に積み重ねられます。 以下に、前述の「スプライト」ベースの同じフルスクリーンボタンのスタイル設定例を示します。

```
.s7video360viewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7video360viewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## スタイルに関する一般的な注意とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS内の外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、このルールに注意してください。 初期設定のアセットもコピーするか、カスタムCSS内のパスを更新します。
* ビットマップアートワークに推奨される形式はPNGです。
* ビットマップアートワークは、このプロパティを使用してユーザインターフェイス要素に割り当 `background-image` てられます。
* ユーザイン `width` ターフ `height` ェイス要素の論理サイズは、およびプロパティで定義します。 に渡されるビットマップのサイズは、論 `background-image` 理サイズに影響しません。

* Retinaなどの高ピクセル密度の高解像度画面を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、このプロパティを適 `-webkit-background-size:contain` 用して、背景を論理ユーザインターフェイス要素のサイズに合わせて縮小します。
* ユーザーインターフェイスからボタンを削除するには、CSSク `display:none` ラスにを追加します。
* カラー値には、CSSでサポートされる様々な形式を使用できます。 透明度が必要な場合は、形式を使用しま `rgba(R,G,B,A)`す。 それ以外の場合は、形式を使用できま `#RRGGBB`す。

* CSSでビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のス `!IMPORTANT` タイル設定に対するルールの使用はサポートされていません。 特に、ビューアま `!IMPORTANT` たはビューアSDKが提供するデフォルトのスタイルや実行時のスタイルを上書きする際には、ルールを使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このリファレンスガイドに記載されているCSSプロパティを設定するには、CSSセレクターを適切な仕様で使用する必要があります。

## 共通のユーザインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオ360ビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
