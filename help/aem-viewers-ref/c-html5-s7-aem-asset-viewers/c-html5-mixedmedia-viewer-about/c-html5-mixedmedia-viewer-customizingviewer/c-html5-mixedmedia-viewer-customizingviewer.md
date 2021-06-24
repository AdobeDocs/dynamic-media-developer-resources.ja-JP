---
description: 混在メディアビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
keywords: レスポンシブ
solution: Experience Manager
title: 混在メディアビューアのカスタマイズ
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 3bea8efb-faf8-4909-b51a-0b9964fcd735
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 0%

---

# 混在メディアビューアのカスタマイズ{#customizing-mixed-media-viewer}

混在メディアビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を`style=`コマンドで指定することです。

初期設定のCSSファイルは次の場所にあります。

`<s7_viewers_root>/html5/MixedMediaViewer_light.css`

このビューアには、「ライト」と「ダーク」カラースキームの2つのCSSファイルが標準で用意されています。 デフォルトでは「ライト」バージョンが使用されますが、次の標準CSSを使用して「ダーク」バージョンに切り替えることができます。

`<s7_viewers_root>/html5/MixedMediaViewer_dark.css`

カスタムのCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素に`.s7mixedmediaviewer`クラスを割り当てることに注意してください。 `style=`コマンドで渡された外部CSSファイルを使用する場合は、CSSルールの子孫セレクターで`.s7mixedmediaviewer`クラスを親クラスとして使用します。 Webページで埋め込みスタイルを使用する場合は、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7mixedmediaviewer`

## レスポンシブデザインCSSの構築 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSSで様々なデバイスおよび埋め込みサイズをターゲットにして、ユーザーのデバイスや特定のWebページのレイアウトに応じて、コンテンツの表示を変えることができます。 これには、Webページのレイアウト、ユーザーインターフェイス要素のサイズ、アートワークの解像度などが該当しますが、これらに限定されません。

ビューアでは、レスポンシブデザインCSSの作成方法が2通りサポートされています。CSSマーカーと標準のCSSメディアクエリ。 これらの方法は、個別に、または一緒に使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成を支援するために、ビューアでは、実行時のビューアサイズと現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられる特別なCSSクラスのCSSマーカーがサポートされています。

CSSマーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small`の各クラスが含まれます。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 つまり、ビューアの領域が一般的なデスクトップモニター`.s7size_large`と同じかそれ以上の場合に、領域のサイズが一般的なタブレットデバイス`.s7size_medium`に近い場合に割り当てられます。 携帯電話の画面`.s7size_small`に類似する領域が設定されます。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、`.s7mouseinput`と`.s7touchinput`が含まれます。 `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合 `.s7mouseinput` は、が使用されます。通常、タッチ入力にはより大きな要素が必要なので、これらのマーカーは、入力タイプごとに異なる画面サイズを持つユーザーインターフェイス入力要素を作成することを目的としています。 デバイスにマウス入力機能とタッチ機能の両方がある場合、 `.s7touchinput`が設定され、ビューアはタッチ操作に適したユーザーインターフェイスをレンダリングします。

以下のサンプルCSSでは、ズームインボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに設定し、タッチデバイスでは56 x 56ピクセルに設定します。 また、ビューアのサイズが非常に小さくなると、ボタンは完全に非表示になります。

```
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7mixedmediaviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7mixedmediaviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

ピクセル密度が異なるデバイスをターゲットにするには、CSSメディアクエリを使用します。 次のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

レスポンシブデザインCSSを構築する最も柔軟な方法は、CSSマーカーを使用することです。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにでき、レスポンシブデザインページのレイアウトに役立ちます。

初期設定のビューアCSSファイルを、CSSマーカーアプローチの例として使用します。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用しておこなうこともできます。 特定のメディアクエリブロック内に含まれるすべての要素は、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、4つのCSSメディアクエリを使用します。これらはCSSで次の順序で定義されます。

1. すべてのタッチデバイスに固有のルールのみを含む。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. 高解像度の画面を持つタブレットに固有のルールのみを含めます。

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

メディアクエリアプローチを使用する場合、デバイス検出を行うCSSを次のように整理する必要があります。

* まず、デスクトップ固有のセクションで、デスクトップに固有またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4つのメディアクエリを上で定義した順に実行し、対応するデバイスタイプに固有のCSSルールを指定します。

各メディアクエリでビューアのCSS全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSSスプライト {#section-209a43dfbddf4fc589e79cddaf233f50}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイルを設定し、複数の異なる視覚状態を持ちます。 良い例は、通常、少なくとも3つの異なる状態を持つボタンです。「up」、「over」、「down」の3つの値を指定します。 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定アプローチでは、CSSは、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 次に、ズームインボタンのスタイル設定用のCSSの例を示します。

```
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

このアプローチの欠点は、要素が初めてで操作されると、エンドユーザーがユーザーインターフェイスの応答がちらつく、または遅れるということです。 このアクションは、新しい要素の状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出しの数が増えるので、パフォーマンスに若干悪影響を与える可能性があります。

CSSスプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに組み合わせる別のアプローチです。 このような「スプライト」は、指定された要素のすべての視覚的状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSS内のすべての異なる状態で同じスプライト画像が参照されます。 また、`background-position`プロパティは、「スプライト」イメージのどの部分を使用するかを指定するために各状態に対して使用されます。 「スプライト」イメージは、適切な方法で構築できます。 通常、ビューアは垂直に積み重ねられます。 以下は、上記と同じズームインボタンのスタイル設定に関する「スプライト」ベースの例です。

```
.s7mixedmediaviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## スタイルに関する一般的な注意事項とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS内で指定されている外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタムCSS内でパスを更新します。
* ビットマップアートワークの推奨される形式はPNGです。
* ビットマップアートワークは、 `background-image`プロパティを使用してユーザインターフェイス要素に割り当てます。
* ユーザーインターフェイス要素の`width`プロパティと`height`プロパティで、論理サイズを定義します。 `background-image`に渡されるビットマップのサイズは論理サイズに影響しません。

* Retinaのような高解像度画面の高ピクセル密度を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、 `-webkit-background-size:contain`プロパティを適用して、背景を論理ユーザインターフェイス要素のサイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、CSSクラスに`display:none`を追加します。
* カラーの値には、CSSでサポートされている様々な形式を使用できます。 透明度が必要な場合は、`rgba(R,G,B,A)`の形式を使用します。 それ以外の場合は、`#RRGGBB`の形式を使用できます。

* CSSを使用してビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のスタイル設定に`!IMPORTANT`ルールを使用することはサポートされていません。 特に、ビューアまたはビューアSDKが提供するデフォルトまたは実行時のスタイル設定を上書きする場合は、`!IMPORTANT`ルールを使用しないでください。 理由は、適切なコンポーネントの動作に影響を与える可能性があるからです。 代わりに、CSSセレクターを適切な特異性で使用して、このリファレンスガイドに記載されているCSSプロパティを設定する必要があります。

## 共通のユーザインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

混在メディアビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。
