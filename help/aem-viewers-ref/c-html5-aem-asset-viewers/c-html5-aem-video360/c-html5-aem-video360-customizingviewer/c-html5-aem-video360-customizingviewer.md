---
title: ビデオ 360 ビューアのカスタマイズ
description: Video360 ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1295'
ht-degree: 0%

---

# ビデオ 360 ビューアのカスタマイズ{#customizing-video-viewer}

Video360 ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定の CSS ファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

初期設定の CSS ファイルは次の場所にあります。

`<s7_viewers_root>/html5/Video360Viewer_dark.css`

カスタムの CSS ファイルには、デフォルトの CSS ファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正常に機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタム CSS ルールを指定する別の方法は、Web ページ上またはリンクされたいずれかの外部 CSS ルール内で、埋め込みスタイルを直接使用することです。

カスタム CSS を作成する場合、ビューアはコンテナの DOM 要素に `.s7video360viewer` クラスを割り当てることに注意してください。 `style=` コマンドで渡された外部 CSS ファイルを使用する場合は、CSS ルールの子孫セレクターで `.s7video360viewer` クラスを親クラスとして使用します。 Web ページで埋め込みスタイルを設定する場合は、次のようにコンテナの DOM 要素の ID を使用してこのセレクターを修飾します。

`#<containerId>.s7video360viewer`

## レスポンシブデザイン CSS の構築 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSS で様々なデバイスや埋め込みサイズをターゲットにして、ユーザーのデバイスや特定の Web ページのレイアウトに応じてコンテンツの表示を変えることができます。 この方法には、レイアウト、ユーザーインターフェイス要素のサイズ、アートワークの解像度などがありますが、これらに限定されません。

ビューアでは、レスポンシブデザイン CSS の作成メカニズムが 2 つサポートされています。CSS マーカーと標準の CSS メディアクエリ。 マーカーやクエリは、個別に使用することも、一緒に使用することもできます。

**CSS マーカー**

レスポンシブデザイン CSS を作成するのに役立つように、ビューアでは CSS マーカーがサポートされています。 これらのマーカーは、最上位のビューアのコンテナ要素に動的に割り当てられる特別な CSS クラスです。 実行時のビューアのサイズと、現在のデバイスで使用されている入力タイプに基づきます。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small` の各クラスが含まれます。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 ビューアの領域が一般的なデスクトップモニタのサイズ以上の場合は、 `.s7size_large` が使用されます。領域が共通のタブレットデバイスに近い場合は、`.s7size_medium` が割り当てられます。 携帯電話の画面に似た領域に対しては、`.s7size_small` が設定されます。 これらの CSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 番目のグループには、`.s7mouseinput` と `.s7touchinput` が含まれます。 現在のデバイスにタッチ入力機能がある場合、マーカー `.s7touchinput` が設定されます。それ以外の場合は、`.s7mouseinput` が使用されます。 通常、タッチ入力にはより大きな要素が必要なので、これらのマーカーは、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを主目的としています。 デバイスにマウス入力機能とタッチ機能の両方がある場合、 `.s7touchinput` が設定され、ビューアはタッチ操作に適したユーザーインターフェイスをレンダリングします。

次のサンプル CSS では、再生/一時停止ボタンのサイズを、マウス入力のシステムでは 28 x 28 ピクセルに設定し、タッチデバイスでは 56 x 56 ピクセルに設定します。 また、ビューアのサイズが大幅に縮小されると、ボタンは完全に非表示になります。

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

HTML5 モバイルビューアに適用する場合、4 つの CSS メディアクエリが使用されます。CSS 内では、次の順に定義されます。

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

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイルを設定し、複数の異なる表示状態を持ちます。 良い例は、通常、少なくとも 3 つの異なる状態を持つボタンです。&quot;up&quot;、&quot;over&quot;、&quot;down&quot; 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定アプローチでは、CSS は、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 フルスクリーンボタンのスタイル設定に使用する CSS の例を以下に示します。

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

このアプローチの欠点は、要素が初めてでインタラクションを受けると、エンドユーザーがユーザーインターフェイスの応答がちらつく、または遅れるということです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法では、サーバーへの HTTP 呼び出しの数が増えるので、パフォーマンスに若干悪影響を与える場合があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる別のアプローチです。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSS 内のすべての異なる状態に対して、同じスプライト画像が参照されます。 また、`background-position` プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態で使用されます。 「スプライト」イメージは、適切な方法で構築できます。 通常、ビューアは垂直方向に積み重ねられます。 以下は、前述の「スプライト」ベースの同じフルスクリーンボタンのスタイル設定例です。

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

* CSS 内で指定されている外部アセットへのパスは、ビューアの HTML ページの場所ではなく、CSS の場所を基準に解決されます。 初期設定の CSS を別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタム CSS 内でパスを更新します。
* ビットマップアートワークの推奨される形式は PNG です。
* ビットマップアートワークは、 `background-image` プロパティを使用してユーザインターフェイス要素に割り当てます。
* ユーザーインターフェイス要素の `width` プロパティと `height` プロパティで論理サイズを定義します。 `background-image` に渡されたビットマップのサイズは論理サイズに影響しません。

* Retina のような高解像度画面の高ピクセル密度を使用するには、論理ユーザインターフェイス要素の 2 倍の大きさのビットマップアートワークを指定します。 次に、 `-webkit-background-size:contain` プロパティを適用して、背景を、論理ユーザインターフェイス要素のサイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、その CSS クラスに `display:none` を追加します。
* カラーの値には、CSS でサポートされている様々な形式を使用できます。 透明度が必要な場合は、`rgba(R,G,B,A)` の形式を使用します。 それ以外の場合は、`#RRGGBB` の形式を使用できます。

* CSS を使用してビューアのユーザインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールを使用してビューア要素のスタイルを設定することはできません。 特に、`!IMPORTANT` ルールを使用して、ビューアまたはビューア SDK が提供するデフォルトまたは実行時のスタイル設定を上書きしないでください。 理由は、適切なコンポーネントの動作に影響を与える可能性があるからです。 代わりに、CSS セレクターを適切な特異性で使用して、このリファレンスガイドに記載されている CSS プロパティを設定する必要があります。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオ 360 ビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
