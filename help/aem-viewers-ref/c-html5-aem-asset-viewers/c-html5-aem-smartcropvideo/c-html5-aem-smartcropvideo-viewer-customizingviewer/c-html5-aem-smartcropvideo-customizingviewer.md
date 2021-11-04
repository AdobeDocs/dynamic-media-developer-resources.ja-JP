---
title: スマート切り抜きビデオビューアのカスタマイズ
description: スマート切り抜きビデオビューアのカスタマイズ
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# スマート切り抜きビデオビューアのカスタマイズ{#customizing-smartcrop-video-viewer}

すべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定の CSS ファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を `style=` コマンドを使用します。

初期設定の CSS ファイルは次の場所にあります。

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

カスタム CSS ファイルには、デフォルトの CSS ファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていないからです。

カスタム CSS ルールを指定する別の方法は、Web ページ上またはリンクされた外部 CSS ルールの 1 つで、埋め込みスタイルを直接使用することです。

カスタム CSS を作成する場合、ビューアは `.s7smartcropvideoviewer` クラスをコンテナの DOM 要素に追加します。 で渡された外部 CSS ファイルを使用する場合、 `style=` コマンド、使用 `.s7smartcropvideoviewer` クラスを親クラスとして、CSS ルールの子孫セレクターに含めます。 Web ページにスタイルを埋め込む場合は、次のようにコンテナの DOM 要素の ID でもこのセレクターを修飾します。

`#<containerId>.s7smartcropvideoviewer`

## レスポンシブデザイン CSS の構築 {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

CSS では、様々なデバイスをターゲットにして、ユーザーのデバイスに応じてコンテンツの表示を異なる方法でおこなうことができます。 このターゲット設定では、ユーザーインターフェイス要素のサイズやアートワークの解像度を変えることもできますが、これらに限定されません。

ビューアは、レスポンシブデザイン CSS の 2 つのメカニズムをサポートしています。CSS マーカーと標準の CSS メディアクエリ。 この 2 つのメカニズムは、個別に、または同時に使用できます。

**CSS マーカー**

レスポンシブデザイン CSS の作成に役立つように、ビューアでは CSS マーカーがサポートされています。このマーカーは、最上位のビューアコンテナ要素に動的に割り当てられる特別な CSS クラスです。 この割り当ては、実行時のビューアサイズと、現在のデバイスで使用されている入力タイプに基づいて行われます。

CSS マーカーの最初のグループには、以下が含まれます。 `.s7size_large`, `.s7size_medium`、および `.s7size_small` クラス。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 つまり、ビューアの領域が一般的なデスクトップモニターのサイズ以上の場合 `.s7size_large` が使用されます。領域のサイズが一般的なタブレットデバイスに近い場合 `.s7size_medium` が割り当てられます。 携帯電話の画面に似た領域の場合、 `.s7size_small` が設定されている。 これらの CSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 つ目のグループには、 `.s7mouseinput` および `.s7touchinput`. マーカー `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合は `.s7mouseinput` が使用されます。 これらのマーカーは、入力タイプごとに異なる画面サイズでユーザインターフェイス入力要素を作成することを目的としています。通常、タッチ入力にはより大きな要素が必要になるからです。 デバイスにマウス入力機能とタッチ機能の両方がある場合、 `.s7touchinput` が設定され、ビューアによってタッチ操作に適したユーザーインターフェイスがレンダリングされます。

以下のサンプル CSS では、再生/一時停止ボタンのサイズを、マウス入力のシステムでは 28 x 28 ピクセルに設定し、タッチデバイスでは 56 x 56 ピクセルに設定します。 また、ビューアのサイズが小さくなると、ボタンは完全に非表示になります。

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

ピクセル密度が異なるデバイスをターゲットにするには、CSS メディアクエリを使用します。 次のメディアクエリブロックには、高密度の画面に固有の CSS が含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーを使用すると、レスポンシブデザイン CSS を柔軟に構築できます。 この柔軟性により、デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにでき、レスポンシブデザインのページレイアウトに役立ちます。

初期設定のビューア CSS ファイルを、CSS マーカーアプローチの例として使用します。

**CSS メディアクエリ**

デバイスの検出は、純粋な CSS メディアクエリを使用しておこなうこともできます。 特定のメディアクエリブロック内に含まれるすべての要素は、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、4 つの CSS メディアクエリを使用します。CSS では、次の順序で定義されます。

1. すべてのタッチデバイスに固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

1. 高解像度画面を持つ携帯電話に固有のルールのみを含みます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

CSS メディアクエリアプローチを使用する場合、デバイス検出を含む CSS を次のように整理する必要があります。

* まず、デスクトップ固有の節で、デスクトップに固有の、またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4 つのメディアクエリを上記の定義の順に記述し、対応するデバイスタイプに固有の CSS ルールを指定します。

各メディアクエリでビューアの CSS 全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSS スプライト {#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイルを設定し、複数の異なる視覚状態を持ちます。 良い例として、通常は少なくとも 3 つの異なる状態を持つボタンがあります。&quot;up&quot;、&quot;over&quot;、&quot;down&quot; 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定アプローチでは、CSS には、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照が含まれていました。 フルスクリーンボタンのスタイル設定に使用する CSS の例を以下に示します。

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

このアプローチの欠点は、要素が初めてで操作されると、エンドユーザーがユーザーインターフェイスの応答がちらつく、または遅延することです。 このアクションは、新しい要素の状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法では、サーバーへの HTTP 呼び出しの数が増えるので、パフォーマンスに若干の悪影響が及ぶ場合があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる場合とは異なるアプローチです。 このような「スプライト」は、指定された要素のすべての視覚状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSS 内のすべての異なる状態で同じスプライト画像が参照されます。 また、 `background-position` プロパティは、「sprite」イメージのどの部分を使用するかを指定するために各状態に対して使用されます。 「スプライト」イメージを適切な方法で構築できます。 通常、ビューアは垂直方向に積み重ねられます。 以下は、上記と同じフルスクリーンボタンのスタイルを設定する「スプライト」ベースの例です。

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## スタイルに関する一般的な注意事項とアドバイス {#section-097418bd618740bba36352629e4d88e1}

* CSS 内で指定されている外部アセットへのパスは、ビューアのパスページの場所ではなく、CSS の場所を基準にHTMLされます。 デフォルトの CSS を別の場所にコピーする場合は、このルールを忘れないでください。 デフォルトのアセットをコピーするか、カスタム CSS 内でパスを更新します。
* ビットマップアートワークの推奨される形式は PNG です。
* ビットマップアートワークは、 `background-image` プロパティ。
* この `width` および `height` ユーザーインターフェイス要素のプロパティは、論理サイズを定義します。 に渡すビットマップのサイズ `background-image` は論理サイズに影響しません。

* Retina のような高解像度画面の高ピクセル密度を使用するには、論理ユーザインターフェイス要素の 2 倍の大きさのビットマップアートワークを指定します。 次に、 `-webkit-background-size:contain` プロパティを使用して、背景を論理ユーザーインターフェイス要素のサイズまで縮小できます。
* ユーザーインターフェイスからボタンを削除するには、 `display:none` を CSS クラスに追加する。
* カラー値には、CSS でサポートされる様々な形式を使用できます。 透明度が必要な場合は、次の形式を使用します。 `rgba(R,G,B,A)`. それ以外の場合は、 `#RRGGBB`.

* CSS を使用してビューアのユーザインターフェイスをカスタマイズする場合、 `!IMPORTANT` ルールは、ビューア要素のスタイル設定に対してサポートされていません。 特に `!IMPORTANT` ルールを使用して、ビューアまたは Viewer SDK が提供するデフォルトのスタイルや実行時のスタイルを上書きしないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このリファレンスガイドに記載されている CSS プロパティを設定するには、適切な特異性を持つ CSS セレクターを使用する必要があります。

## 共通のユーザインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

スマート切り抜きビデオビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
