---
title: ビデオビューアのカスタマイズ
description: ビデオビューアのカスタマイズ
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
TQID: 'https://experienceleague.adobe.com/YAER4cAWjtL3KBfYsrS8JOh7tCGvsDKukDtVDT0EocI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 0%

---

# ビデオビューアのカスタマイズ{#customizing-video-viewer}

すべての視覚的なカスタマイズとほとんどの動作のカスタマイズは、カスタム CSSを作成することによって行われます。

推奨されるワークフローは、適切なビューアのデフォルトのCSS ファイルを取得し、別の場所にコピーしてカスタマイズし、`style=` コマンドでカスタマイズしたファイルの場所を指定することです。

デフォルトのCSS ファイルは次の場所にあります。

`<s7_viewers_root>/html5/VideoViewer.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言が含まれている必要があります。 クラス宣言を省略すると、ユーザーインターフェイス要素に組み込みのデフォルトスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、埋め込みスタイルをweb ページまたはリンクされた外部CSS ルールのいずれかに直接使用する方法があります。

カスタム CSSを作成する際は、ビューアがコンテナ DOM要素に`.s7videoviewer` クラスを割り当てていることを忘れないでください。 `style=` コマンドで渡される外部CSS ファイルを使用する場合は、CSS ルールの子孫セレクターで`.s7videoviewer` クラスを親クラスとして使用します。 Web ページにスタイルを埋め込む場合は、このセレクターをコンテナ DOM要素のIDで次のように修飾します。

`#<containerId>.s7videoviewer`

## レスポンシブデザインのCSSを作成する {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

CSSの様々なデバイスをターゲットにして、ユーザーのデバイスに応じてコンテンツの表示を変えることができます。 このターゲティングには、異なるユーザーインターフェイス要素のサイズとアートワークの解像度が含まれますが、これらに限定されません。

ビューアは、レスポンシブデザインのCSSを作成する2つのメカニズム（CSS マーカーと標準のCSS メディアクエリ）をサポートしています。 これらの2つのメカニズムを個別にまたは一緒に使用できます。

**CSS マーカー**

レスポンシブデザインのCSSを作成しやすくするために、ビューアは、トップレベルのビューアコンテナ要素に動的に割り当てられた特殊なCSS クラスであるCSS マーカーをサポートしています。 割り当ては、実行時のビューアサイズと、現在のデバイスで使用されている入力タイプに基づいています。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`および`.s7size_small`個のクラスが含まれています。 ビューアコンテナのランタイム領域に基づいて適用されます。 つまり、ビューア領域が一般的なデスクトップモニター`.s7size_large`のサイズと同じかそれより大きい場合、または共通のタブレットデバイス `.s7size_medium`にサイズが近い場合に割り当てられます。 携帯電話の画面に似た領域には、`.s7size_small`が設定されています。 これらのCSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの2番目のグループには`.s7mouseinput`と`.s7touchinput`が含まれています。 現在のデバイスにタッチ入力機能がある場合は、マーカー`.s7touchinput`が設定されます。それ以外の場合は、`.s7mouseinput`が使用されます。 これらのマーカーは、通常タッチ入力には大きな要素が必要なため、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。 デバイスにマウス入力とタッチ機能の両方がある場合は、`.s7touchinput`が設定され、ビューアはタッチ対応のユーザーインターフェイスをレンダリングします。

次のCSSの例では、再生/一時停止ボタンのサイズを、マウス入力のあるシステムでは28 x 28 ピクセル、タッチデバイスでは56 x 56 ピクセルに設定しています。 さらに、ビューアサイズが小さすぎると、ボタンが完全に非表示になります。

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

異なるピクセル密度のデバイスをターゲットにするには、CSS メディアクエリを使用します。 次のメディアクエリブロックには、高密度スクリーンに固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーを使用することは、レスポンシブデザインのCSSを作成する最も柔軟な方法です。 その理由は、デバイスの画面サイズだけでなく、実際の視聴者サイズもターゲットにできるからです。これは、レスポンシブデザインページのレイアウトに役立つ可能性があります。

CSS マーカーアプローチの例として、デフォルトのビューア CSS ファイルを使用します。

**CSS メディアクエリ**

デバイス検出は、純粋なCSS メディアクエリを使用して実行することもできます。 特定のメディアクエリブロック内に囲まれたすべてが、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、CSSで次の順序で定義された4つのCSS メディアクエリを使用します。

1. すべてのタッチデバイスに固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

CSS メディアクエリ アプローチを使用して、デバイス センシングを使用してCSSを次のように整理します。

* 最初に、「デスクトップ固有」セクションでは、デスクトップ固有またはすべての画面に共通するすべてのプロパティを定義します。
* 次に、4つのメディアクエリは、上記で定義した順序で行い、対応するデバイスタイプに固有のCSS ルールを提供する必要があります。

各メディアクエリでビューア CSS全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSS スプライト {#section-9b6d8d601cb441d08214dada7bb4eddc}

多くのビューアーユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる視覚状態を持ちます。 良い例は、通常は「up」、「over」、「down」の3つの異なる状態を持つボタンです。 各ステートには、割り当てられた独自のビットマップアートワークが必要です。

スタイル設定に対する従来のアプローチでは、CSSはユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 フルスクリーンボタンのスタイルを設定するためのCSSの例を次に示します。

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

このアプローチの欠点は、要素が初めて操作されたときに、エンドユーザーがちらついたり、ユーザーインターフェイスの応答が遅れたりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出し数が増加するため、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべてのエレメント状態の画像アートワークを「スプライト」と呼ばれる1つのPNG ファイルに結合する別のアプローチです。 このような「スプライト」には、特定の要素のすべての視覚状態が次から次へと配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、同じスプライトイメージがCSSのすべての異なるステートに対して参照されます。 また、`background-position` プロパティは各状態に対して使用され、「スプライト」画像のどの部分を使用するかを指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 通常、ビューアは垂直方向に積み重ねられます。 以下は、上から同じフルスクリーンボタンをスタイル設定する「スプライト」ベースの例です。

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

## 一般的なスタイリングノートとアドバイス {#section-097418bd618740bba36352629e4d88e1}

* CSS内の外部アセットへのすべてのパスは、ビューアのHTML ページの場所ではなく、CSSの場所に対して解決されます。 デフォルトのCSSを別の場所にコピーする場合は、このルールを考慮する必要があります。 カスタム CSS内のデフォルトのアセットをコピーするか、パスを更新します。
* ビットマップアートワークにはPNG形式が適しています。
* ビットマップアートワークは、`background-image` プロパティを使用してユーザーインターフェイス要素に割り当てられます。
* ユーザーインターフェイス要素の`width`および`height` プロパティが、その論理サイズを定義します。 `background-image`に渡されたビットマップのサイズは、論理サイズに影響しません。

* Retinaのような高解像度の画面の高いピクセル密度を使用するには、ビットマップアートワークを論理ユーザーインターフェイス要素サイズの2倍のサイズで指定します。 次に、`-webkit-background-size:contain` プロパティを適用して、背景を論理ユーザーインターフェイス要素サイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、そのCSS クラスに`display:none`を追加します。
* CSSがサポートするカラー値には、様々な形式を使用できます。 透明性が必要な場合は、形式`rgba(R,G,B,A)`を使用してください。 それ以外の場合は、形式`#RRGGBB`を使用できます。

* CSSを使用してビューアのユーザーインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールの使用はビューア要素のスタイル設定には対応していません。 特に、`!IMPORTANT` ルールは、ビューアまたはビューア SDKが提供するデフォルトまたは実行時のスタイル設定を上書きするために使用しないでください。 その理由は、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このリファレンスガイドに記載されているCSS プロパティを設定するには、適切な特異性を持つCSS セレクターを使用する必要があります。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

ビデオビューアに適用されるユーザーインターフェイス要素のリファレンスドキュメントを次に示します。
