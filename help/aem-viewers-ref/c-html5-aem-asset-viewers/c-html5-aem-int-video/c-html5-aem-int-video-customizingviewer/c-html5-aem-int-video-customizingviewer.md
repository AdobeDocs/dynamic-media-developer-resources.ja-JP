---
title: インタラクティブビデオビューアのカスタマイズ
description: インタラクティブビデオビューアのビジュアルカスタマイズと動作のカスタマイズは、すべてカスタム CSSを作成することによって行われます。
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c428c3e6-81be-4708-b064-f9d794183209
TQID: 'https://experienceleague.adobe.com/0qeQ-Rt61o6di8DsKRHoWq5efNgGsGxRt7AbhY0cXPQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1409
ht-degree: 0%

---

# インタラクティブビデオビューアのカスタマイズ{#customizing-interactive-video-viewer}

インタラクティブビデオビューアのビジュアルカスタマイズと動作のカスタマイズは、すべてカスタム CSSを作成することによって行われます。

推奨されるワークフローは、適切なビューアのデフォルトのCSS ファイルを取得し、別の場所にコピーしてカスタマイズし、`style=` コマンドでカスタマイズしたファイルの場所を指定することです。

デフォルトのCSS ファイルは次の場所にあります。

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

ビューアには、「ライト」と「ダーク」のカラースキーム用に、2つの標準CSS ファイルが用意されています。 デフォルトでは「暗い」バージョンが使用されますが、次の標準CSSを使用して「明るい」バージョンに簡単に切り替えることができます。

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言が含まれている必要があります。 クラス宣言を省略すると、ユーザーインターフェイス要素に組み込みのデフォルトスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、埋め込みスタイルをweb ページまたはリンクされた外部CSS ルールのいずれかに直接使用する方法があります。

カスタム CSSを作成する場合、ビューアはコンテナ DOM要素に`.s7interactivevideoviewer` クラスを割り当てることに注意してください。 `style=` コマンドで渡された外部CSS ファイルを使用している場合は、CSS ルールの子孫セレクターで`.s7interactivevideoviewer` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを行う場合は、このセレクターをコンテナ DOM要素のIDで次のように修飾します。

`#<containerId>.s7interactivevideoviewer`

## レスポンシブデザインのCSSを作成する {#section-0bb49aca42d242d9b01879d5ba59d33b}

異なるデバイスやCSSの埋め込みサイズをターゲットにして、ユーザーのデバイスや特定のweb ページレイアウトに応じてコンテンツの表示を異ならせることができます。 この方法には、様々なレイアウト、ユーザーインターフェイス要素のサイズ、アートワークの解像度が含まれますが、これらに限定されません。

ビューアは、レスポンシブデザインのCSSを作成する2つのメカニズム（CSS マーカーと標準のCSS メディアクエリ）をサポートしています。 これらのメカニズムは、単独でも一緒でも使用できます。

**CSS マーカー**

レスポンシブデザインのCSSの作成に役立つように、ビューアはCSS マーカーをサポートしています。 これらのマーカーは特殊なCSS クラスです。 実行時のビューアサイズと、現在のデバイスで使用されている入力タイプに基づいて、トップレベルビューアコンテナ要素に動的に割り当てられます。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`および`.s7size_small`個のクラスが含まれています。 ビューアコンテナの実行時領域に基づいて適用されます。 ビューア領域が一般的なデスクトップモニターのサイズと同じかそれ以上の場合は、`.s7size_large`が使用されます。その領域が一般的なタブレットデバイスに近い場合は、`.s7size_medium`が割り当てられます。 携帯電話の画面に似た領域には、`.s7size_small`が設定されています。 これらのCSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの2番目のグループに`.s7mouseinput`と`.s7touchinput`が含まれています。 現在のデバイスにタッチ入力機能がある場合は、マーカー`.s7touchinput`が設定されます。それ以外の場合は、`.s7mouseinput`が使用されます。 これらのマーカーは主に、通常タッチ入力には大きな要素が必要なため、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。

CSS マーカーの3番目のグループには`.s7device_landscape`と`.s7device_portrait`が含まれています。 タッチデバイスが横方向の場合はマーカー`.s7device_landscape`が設定され、タッチデバイスが縦方向に回転する場合は`.s7device_portrait`が使用されます。 これらのCSS マーカーは、デスクトップシステムでのみ使用することを目的としています。

次のCSSの例では、マウス入力のあるシステムでは再生/一時停止ボタンのサイズを28 x 28 ピクセルに、タッチデバイスでは56 x 56 ピクセルに設定しています。 さらに、ビューアのサイズが大幅に小さくなると、ボタンが完全に非表示になります。

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

次の例では、タッチデバイスが縦向きの場合、ビデオコントロールバーはビューアの下部の138 ピクセル上に配置されます。 その他のすべての場合は、ビューアの下部に移動します。

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

異なるピクセル密度のデバイスをターゲットにするには、CSS メディアクエリを使用する必要があります。 次のメディアクエリブロックには、高密度スクリーンに固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーを使用すると、デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにできるため、レスポンシブデザイン CSSを作成する最も柔軟な方法です。これは、レスポンシブデザインレイアウトに役立ちます。

デフォルトのビューア CSS ファイルは、CSS マーカーアプローチの例として使用できます。

**CSS メディアクエリ**

純粋なCSS メディアクエリを使用して、デバイス検出を実行することもできます。 特定のメディアクエリブロック内に囲まれたすべてが、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、CSSで定義された4つのCSS メディアクエリを次の順序で使用します。

1. すべてのタッチデバイスに固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 高解像度の画面を持つタブレットに固有のルールのみが含まれます。

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

1. 高解像度の画面を持つ携帯電話に固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

メディアクエリのアプローチを使用して、デバイスセンシングでCSSを整理する必要があります。

* まず、「デスクトップ固有」セクションでは、デスクトップ固有またはすべてのスクリーンに共通するすべてのプロパティを定義します。
* 2つ目は、4つのメディアクエリが上記で定義された順序で行われ、対応するデバイスタイプに固有のCSS ルールが提供されます。

各メディアクエリでビューア CSS全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSS スプライト {#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアーユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる視覚状態を持ちます。 良い例は、通常は「up」、「over」、「down」の3つの異なる状態を持つボタンです。 各ステートには、割り当てられた独自のビットマップアートワークが必要です。

スタイル設定に対する従来のアプローチでは、CSSはユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 フルスクリーンボタンのスタイルを設定するためのCSSの例を次に示します。

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

このアプローチの欠点は、要素が初めて操作されたときに、エンドユーザーがちらついたり、ユーザーインターフェイスの応答が遅れたりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出し数が増加するため、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべてのエレメント状態の画像アートワークを「スプライト」と呼ばれる1つのPNG ファイルに結合する別のアプローチです。 このような「スプライト」には、特定の要素のすべての視覚状態が次から次へと配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、同じスプライトイメージがCSSのすべての異なるステートに対して参照されます。 また、`background-position` プロパティは各状態に対して使用され、「スプライト」画像のどの部分を使用するかを指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 通常、ビューアは垂直方向に積み重ねられます。 以下は、先ほど同じフルスクリーンボタンをスタイル設定した「スプライト」ベースの例です。

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

## 一般的なスタイリングノートとアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSSを使用してビューアのユーザーインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールの使用はビューア要素のスタイル設定には対応していません。 特に、`!IMPORTANT` ルールは、ビューアまたはビューア SDKが提供するデフォルトまたは実行時のスタイル設定を上書きするために使用しないでください。 その理由は、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このリファレンスガイドに記載されているCSS プロパティを設定するには、適切な特異性を持つCSS セレクターを使用する必要があります。

* CSS内の外部アセットへのすべてのパスは、ビューアのHTML ページの場所ではなく、CSSの場所に対して解決されます。 デフォルトのCSSを別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタム CSS内のパスを更新します。
* ビットマップアートワークにはPNG形式が適しています。
* ビットマップアートワークは、`background-image` プロパティを使用してユーザーインターフェイス要素に割り当てられます。
* ユーザーインターフェイス要素の`width`および`height` プロパティが、その論理サイズを定義します。 `background-image`に渡されたビットマップのサイズは、論理サイズに影響しません。

* Retinaのような高解像度の画面の高いピクセル密度を使用するには、ビットマップアートワークを論理ユーザーインターフェイス要素サイズの2倍のサイズで指定します。 次に、`-webkit-background-size:contain` プロパティを適用して、背景を論理ユーザーインターフェイス要素サイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、そのCSS クラスに`display:none`を追加します。
* CSSがサポートするカラー値には、様々な形式を使用できます。 透明性が必要な場合は、形式`rgba(R,G,B,A)`を使用してください。 それ以外の場合は、形式`#RRGGBB`を使用できます。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

次に、インタラクティブビデオビューアに適用されるユーザーインターフェイス要素のリファレンスドキュメントを示します。
