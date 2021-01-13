---
description: ビデオビューアのカスタマイズ
keywords: responsive
solution: Experience Manager
title: ビデオビューアのカスタマイズ
topic: Dynamic media
uuid: e18fdf8b-5834-4c99-b8a3-90d1f8310dc1
translation-type: tm+mt
source-git-commit: 846069e15c622efb1b899956ef84efba9e1a6729
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 0%

---


# ビデオビューアのカスタマイズ{#customizing-video-viewer}

すべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローとして、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を`style=`コマンドで指定します。

初期設定のCSSファイルは、次の場所にあります。

`<s7_viewers_root>/html5/VideoViewer.css`

カスタムのCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正常に機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素に`.s7videoviewer`クラスを割り当てることに注意してください。 `style=`コマンドで渡される外部CSSファイルを使用する場合は、CSSルールの子孫セレクターで`.s7videoviewer`クラスを親クラスとして使用します。 Webページ上にスタイルを埋め込む場合、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7videoviewer`

## レスポンシブデザインCSSの構築{#section-63e8f93ee2f14fd8bba1ce33a6870b80}

CSSでは、様々なデバイスをターゲットして、ユーザーのデバイスに応じてコンテンツの表示を変えることができます。 例えば、ユーザーインターフェイス要素のサイズやアートワークの解像度を変えることができます。

ビューアでは、レスポンシブデザインCSSの作成メカニズムが2つサポートされています。CSSマーカーと標準のCSSメディアクエリ これらは、個別にも、一緒にも使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成に役立つように、ビューアでは、CSSマーカーがサポートされています。このCSSマーカーは、実行時のビューアサイズと現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられます。

CSSマーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small`の各クラスが含まれます。 これらは、ビューアコンテナの実行時の領域に基づいて適用されます。 つまり、ビューアの領域が一般的なデスクトップモニター`.s7size_large`と同じかそれ以上である場合、領域のサイズが一般的なタブレットデバイス`.s7size_medium`に近い場合は、が割り当てられます。 携帯電話の画面に似た領域に対しては`.s7size_small`が設定される。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、`.s7mouseinput`と`.s7touchinput`が含まれます。 `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合 `.s7mouseinput` は、が使用されます。これらのマーカーは、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを目的としています。通常は、タッチ入力にはより多くの要素が必要なためです。 デバイスにマウス入力機能とタッチ機能の両方がある場合は、`.s7touchinput`が設定され、ビューアはタッチに対応したユーザーインターフェイスをレンダリングします。

以下のサンプルCSSでは、再生/一時停止ボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに設定し、タッチデバイスでは56 x 56ピクセルに設定します。 また、ビューアのサイズが非常に小さくなると、ボタンは完全に非表示になります。

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

ピクセル密度が異なるデバイスをターゲットするには、CSSメディアクエリを使用します。 以下のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

レスポンシブデザインCSSを構築する最も柔軟性の高い方法は、CSSマーカーを使用することです。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットできるので、レスポンシブデザインページレイアウトに便利です。

初期設定のビューアCSSファイルを、CSSマーカーアプローチの例として使用します。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用して行うこともできます。 特定のメディアクエリブロック内に含まれるすべては、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用される場合は、4つのCSSメディアクエリが使用されます。これらのメディアメソッドはCSS内で次の一覧の順に定義されます。

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

CSSメディアクエリアプローチを使用する場合は、デバイス検出機能を持つCSSを次のように整理する必要があります。

* まず、デスクトップに固有のセクションを記述し、デスクトップに固有またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4つのメディアクエリを上記の定義の順に記述し、対応するデバイスタイプに固有のCSSルールを指定します。

各メディアクエリでビューアのCSS全体を重複する必要はありません。 特定のデバイスに固有のプロパティのみがメディアクエリ内で再定義されます。

## CSSスプライト{#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例として、通常は少なくとも3つの状態を持つボタンが挙げられます。「up」、「over」および「down」 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSはユーザインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 以下は、フルスクリーンボタンのスタイル設定に使用するCSSの例です。

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

このアプローチの欠点は、エンドユーザーが要素との初回のインタラクション時にちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出しの数が増えたので、パフォーマンスに若干悪影響を及ぼす場合があります。

CSSスプライトは、異なるアプローチで、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合します。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザーインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して、同じスプライト画像が参照されます。 また、`background-position`プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に並べられます。 下の例は、「スプライト」ベースで、上述と同じフルスクリーンボタンのスタイル設定を行った例です。

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## スタイルに関する一般的な注意とアドバイス{#section-097418bd618740bba36352629e4d88e1}

* CSS内で指定されている外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、この点を考慮してください。 初期設定のアセットをコピーするか、カスタムCSS内でパスを更新します。
* ビットマップアートワークの推奨される形式はPNGです。
* ビットマップアートワークは、`background-image`プロパティを使用してユーザインターフェイス要素に割り当てます。
* ユーザーインターフェイス要素の`width`プロパティと`height`プロパティは、論理サイズを定義します。 `background-image`に渡されるビットマップのサイズは論理サイズに影響しません。

* Retinaなど高ピクセル密度の高解像度画面を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、`-webkit-background-size:contain`プロパティを適用して、背景を、論理ユーザーインターフェイス要素のサイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、そのCSSクラスに`display:none`を追加します。
* カラー値には、CSSでサポートされている様々な形式を使用できます。 透明度が必要な場合は、`rgba(R,G,B,A)`の形式を使用します。 それ以外の場合は、`#RRGGBB`の形式を使用できます。

* CSSでビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のスタイル設定に`!IMPORTANT`ルールの使用はサポートされていません。 特に、`!IMPORTANT`ルールは、ビューアまたはビューアSDKが提供するデフォルトまたは実行時のスタイル設定を上書きする場合には使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、CSSセレクターを適切な仕様で使用して、このリファレンスガイドに記載されているCSSプロパティを設定する必要があります。

## 共通のユーザーインターフェイス要素{#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
