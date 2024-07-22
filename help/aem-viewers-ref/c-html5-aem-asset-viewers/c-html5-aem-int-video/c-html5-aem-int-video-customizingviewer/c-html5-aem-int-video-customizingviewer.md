---
title: インタラクティブビデオビューアのカスタマイズ
description: インタラクティブビデオビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行います。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c428c3e6-81be-4708-b064-f9d794183209
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 0%

---

# インタラクティブビデオビューアのカスタマイズ{#customizing-interactive-video-viewer}

インタラクティブビデオビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行います。

推奨されるワークフローは、適切なビューアのデフォルトの CSS ファイルを取得し、別の場所にコピーしてカスタマイズし、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

デフォルトの CSS ファイルは、次の場所にあります。

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

ビューアには、「明」と「暗」のカラースキーム用の 2 つの標準 CSS ファイルが用意されています。 デフォルトでは「dark」バージョンが使用されますが、次の標準 CSS を使用すると、「light」バージョンに簡単に切り替えることができます。

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言を含める必要があります。 クラスの宣言を省略すると、ユーザーインターフェイス要素の組み込みの既定のスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、web ページ上で直接埋め込みスタイルを使用するか、リンクされた外部 CSS ルールの 1 つで埋め込みスタイルを使用する方法があります。

カスタム CSS を作成する場合は、ビューアがコンテナの DOM 要素にクラス `.s7interactivevideoviewer` 割り当てることに注意してください。 コマンドで渡された外部 CSS ファイルを使用してい `style=` 場合は、CSS ルールの descendant セレクターで `.s7interactivevideoviewer` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを作成する場合は、次のように、このセレクターをコンテナ DOM 要素の ID で修飾します。

`#<containerId>.s7interactivevideoviewer`

## レスポンシブデザイン CSS の作成 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSS では様々なデバイスや埋め込みサイズをターゲットにすることができ、ユーザーのデバイスや特定の web ページレイアウトに応じて、コンテンツの表示を異なったものにすることができます。 この方法には、レイアウトの違い、ユーザーインターフェイス要素のサイズ、アートワークの解像度などが含まれますが、これらに限定されません。

このビューアは、レスポンシブに設計された CSS を作成する、CSS マーカーと標準の CSS メディアクエリの 2 つのメカニズムをサポートしています。 これらのメカニズムは、個別に使用することも、同時に使用することもできます。

**CSS マーカー**

レスポンシブデザイン CSS の作成に役立つように、ビューアでは CSS マーカーをサポートしています。 これらのマーカーは特別な CSS クラスです。 これらは、実行時ビューアのサイズと、現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられます。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small` の各クラスが含まれます。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 ビューア領域が共通のデスクトップモニターのサイズと同じかそれ以上の場合は、`.s7size_large` が使用されます。ビューア領域が共通のタブレットデバイスに近い場合は、`.s7size_medium` が割り当てられます。 携帯電話画面に類似した領域の場合、`.s7size_small` が設定されます。 これらの CSS マーカーの主な目的は、異なる画面およびビューアのサイズに対して異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 番目のグループには、`.s7mouseinput` と `.s7touchinput` が含まれます。 現在のデバイスにタッチ入力機能がある場合は、マーカー `.s7touchinput` が設定されます。それ以外の場合は、`.s7mouseinput` が使用されます。 通常のタッチ入力にはより大きな要素が必要なため、これらのマーカーは主に、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。

CSS マーカーの 3 番目のグループには、`.s7device_landscape` と `.s7device_portrait` が含まれます。 マーカー `.s7device_landscape` は、タッチデバイスが横向きの場合に設定さ `.s7device_portrait`、タッチデバイスを縦向きに回転させる際に使用される。 これらの CSS マーカーは、デスクトップシステムでの使用のみを目的としています。

次のサンプル CSS では、マウス入力を持つシステムの再生/一時停止ボタンのサイズを 28 x 28 ピクセルに設定し、タッチデバイスの場合は 56 x 56 ピクセルに設定します。 さらに、ビューアのサイズが大幅に削減された場合は、ボタンは完全に非表示になります。

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

次の例では、タッチデバイスが縦向きの場合、ビデオコントロールバーの位置はビューアの下部から 138 ピクセル上になります。 その他のすべての場合では、ビューアの下部に移動されます。

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

ピクセル密度の異なるデバイスをターゲットにするには、CSS メディアクエリを使用する必要があります。 次のメディアクエリーブロックは、高密度画面に固有の CSS を含んでいます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーを使用すると、デバイスの画面サイズだけでなく実際のビューアのサイズもターゲットにできるので、レスポンシブデザイン CSS を構築する最も柔軟な方法です。これは、レスポンシブデザインレイアウトに役立ちます。

CSS マーカーアプローチの例として、デフォルトのビューア CSS ファイルを使用できます。

**CSS メディアクエリ**

また、純粋な CSS メディアクエリを使用して、デバイスの検出を実行することもできます。 特定のメディアクエリブロック内に含まれているすべてが、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、次に示す順序で 4 つの CSS メディアクエリを使用します。これらは CSS で定義されます。

1. すべてのタッチデバイスに固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 高解像度の画面を含むタブレット専用のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. すべての携帯電話に固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. 高解像度画面を使用する携帯電話専用のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

メディアクエリのアプローチを使用して、次のように、デバイスを検出して CSS を整理する必要があります。

* まず、デスクトップ固有のセクションでは、デスクトップ固有またはすべての画面に共通のすべてのプロパティを定義します。
* 2 番目に、4 つのメディアクエリは、上記で定義された順序で、対応するデバイスタイプに固有の CSS ルールを提供します。

各メディアクエリでビューア CSS 全体を複製する必要はありません。 メディアクエリ内で再定義されるのは、特定のデバイスに固有のプロパティのみです。

## CSS スプライト {#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアのユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイルが設定され、複数の異なる表示状態があります。 良い例は、通常、「上」、「オーバー」、「下」の少なくとも 3 つの異なる状態があるボタンです。 各ステートには、独自のビットマップアートワークが割り当てられている必要があります。

スタイル設定への従来のアプローチでは、CSS は、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 フルスクリーンボタンのスタイル設定に使用する CSS のサンプルを以下に示します。

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

このアプローチの欠点は、要素を初めて操作したときに、エンドユーザーのユーザーインターフェイス応答がちらつきしたり、遅延したりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチでは、サーバーへの HTTP 呼び出し数が増加するので、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる異なるアプローチです。 このような「スプライト」では、特定の要素のすべての視覚状態が順番に配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、CSS 内のすべての異なる状態に対して同じスプライト画像が参照されます。 また、`background-position` プロパティは、各状態に対して使用され、「スプライト」画像の使用部分を指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 ビューアでは通常、画像を垂直方向に積み重ねます。 以下は、以前に同じフルスクリーンボタンのスタイルを設定した「スプライト」ベースの例です。

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

## 一般的なスタイル設定のメモとアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS を使用してビューアユーザーインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールを使用してビューア要素のスタイルを設定することはできません。 特に、ビューア `!IMPORTANT` たはビューア SDK で提供されるデフォルトまたは実行時のスタイル設定を上書きする場合は、このルールを使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、適切な特異性を持つ CSS セレクターを使用して、このリファレンスガイドに記載されている CSS プロパティを設定する必要があります。

* CSS 内の外部アセットへのすべてのパスは、ビューアHTMLページの場所ではなく CSS の場所に対して解決されます。 デフォルトの CSS を別の場所にコピーする場合は、このルールに注意してください。 デフォルトアセットもコピーするか、カスタム CSS 内のパスを更新します。
* ビットマップアートワークの形式は PNG が推奨されます。
* ビットマップアートワークは、`background-image` プロパティを使用してユーザーインターフェイス要素に割り当てられます。
* ユーザーインターフェイス要素の `width` プロパティと `height` プロパティは、その論理サイズを定義します。 `background-image` に渡されるビットマップのサイズは、論理サイズに影響しません。

* Retina のような高解像度の画面で高いピクセル密度を使用するには、ビットマップアートワークを論理ユーザーインターフェイス要素のサイズの 2 倍の大きさに指定します。 次に、`-webkit-background-size:contain` プロパティを適用して、背景を論理ユーザーインターフェイス要素サイズに縮小します。
* ユーザーインターフェイスからボタンを削除するには、CSS クラスに `display:none` を追加します。
* CSS がサポートするカラー値に対して様々な形式を使用できます。 透明度が必要な場合は、形式 `rgba(R,G,B,A)` を使用します。 それ以外の場合は、`#RRGGBB` 形式を使用できます。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下は、インタラクティブビデオビューアに適用されるユーザーインターフェイス要素のリファレンスドキュメントです。
