---
description: インタラクティブビデオビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
keywords: responsive
seo-description: インタラクティブビデオビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
seo-title: インタラクティブビデオビューアのカスタマイズ
solution: Experience Manager
title: インタラクティブビデオビューアのカスタマイズ
topic: Dynamic media
uuid: a24e7ada-c874-468b-ac44-a51d581d4479
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 0%

---


# インタラクティブビデオビューアのカスタマイズ{#customizing-interactive-video-viewer}

インタラクティブビデオビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローとして、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を`style=`コマンドで指定します。

初期設定のCSSファイルは、次の場所にあります。

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

このビューアには、「ライト」と「ダーク」のカラースキームに対応する2つのCSSファイルが付属し、すぐに使用できます。 初期設定では「ダーク」バージョンが使用されますが、次の標準CSSを使用すると「ライト」バージョンに簡単に切り替えることができます。

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

カスタムのCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正常に機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素に`.s7interactivevideoviewer`クラスを割り当てることに注意してください。 `style=`コマンドによって渡された外部CSSファイルを使用する場合は、CSSルールの子孫セレクターで`.s7interactivevideoviewer`クラスを親クラスとして使用します。 Webページ上で埋め込みスタイルを使用する場合、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7interactivevideoviewer`

## レスポンシブデザインCSSの構築{#section-0bb49aca42d242d9b01879d5ba59d33b}

CSSで様々なデバイスや埋め込みサイズをターゲットして、ユーザーのデバイスや特定のWebページのレイアウトに応じてコンテンツの表示を変えることができます。 例えば、レイアウト、ユーザインターフェイス要素のサイズおよびアートワークの解像度を変えることができます。

ビューアでは、レスポンシブデザインCSSの作成メカニズムが2つサポートされています。CSSマーカーと標準のCSSメディアクエリ これらは、個別にも、一緒にも使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成に役立つように、ビューアではCSSマーカーがサポートされています。 これらは特殊なCSSクラスで、実行時のビューアのサイズと現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に割り当てられます。

CSSマーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small`の各クラスが含まれます。 これらは、ビューアコンテナの実行時の領域に基づいて適用されます。 ビューアの領域が一般的なデスクトップモニター以上の場合は、`.s7size_large`が使用されます。領域が一般的なタブレットデバイスに近い場合は、`.s7size_medium`が割り当てられます。 携帯電話の画面に似た領域に対しては`.s7size_small`が設定されます。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、`.s7mouseinput`と`.s7touchinput`が含まれています。 `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合 `.s7mouseinput` は、が使用されます。これらのマーカーは、主に、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを意図しています。通常は、タッチ入力にはより大きな要素が必要だからです。

CSSマーカーの3番目のグループには、`.s7device_landscape`と`.s7device_portrait`が含まれます。 `.s7device_landscape` は、タッチデバイスが横置きの場合に設定されます。 `.s7device_portrait` は、タッチデバイスを回転して縦長にする場合に使用します。これらのCSSマーカーは、デスクトップシステムでのみ使用されます。

以下のサンプルCSSでは、再生/一時停止ボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに設定し、タッチデバイスでは56 x 56ピクセルに設定します。 また、ビューアのサイズを大幅に縮小すると、ボタンは完全に非表示になります。

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

次の例では、タッチデバイスが縦置きの場合、ビデオコントロールバーはビューアの下部の138ピクセル上に配置され、それ以外の場合はビューアの下部に移動します。

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
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

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例として、通常は少なくとも3つの状態を持つボタンが挙げられます。「up」、「over」および「down」 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSはユーザインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 以下は、フルスクリーンボタンのスタイル設定に使用するCSSの例です。

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

このアプローチの欠点は、エンドユーザーが要素との初回のインタラクション時にちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出しの数が増えたので、パフォーマンスに若干悪影響を及ぼす場合があります。

CSSスプライトは、異なるアプローチで、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合します。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザーインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して、同じスプライト画像が参照されます。 また、`background-position`プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に並べられます。 以下に、前述の「スプライト」ベースの同じフルスクリーンボタンのスタイル設定例を示します。

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
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

インタラクティブビデオビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
