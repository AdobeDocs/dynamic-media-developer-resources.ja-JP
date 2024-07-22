---
title: ズームビューアのカスタマイズ
description: ズームビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS の作成によって行われます。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 336bf68c-6110-4ce8-85b4-28d7397044c2
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 0%

---

# ズームビューアのカスタマイズ{#customizing-zoom-viewer}

ズームビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS の作成によって行われます。

推奨されるワークフローは、適切なビューアのデフォルトの CSS ファイルを取得し、別の場所にコピーしてカスタマイズし、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

デフォルトの CSS ファイルは、次の場所にあります。

`<s7_viewers_root>/html5/ZoomViewer_light.css`

ビューアには、「明」と「暗」のカラースキーム用の 2 つの標準 CSS ファイルが用意されています。 デフォルトでは「light」バージョンが使用されますが、次の標準 CSS を使用して「dark」バージョンに切り替えることができます。

`<s7_viewers_root>/html5/ZoomViewer_dark.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言を含める必要があります。 クラスの宣言を省略すると、ユーザーインターフェイス要素の組み込みの既定のスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供するもう 1 つの方法は、web ページ上で直接埋め込みスタイルを使用するか、リンクされた外部 CSS ルールの 1 つで埋め込みスタイルを使用することです。

カスタム CSS を作成する場合は、ビューアがコンテナの DOM 要素にクラス `.s7zoomviewer` 割り当てることに注意してください。 コマンドで渡された外部 CSS ファイルを使用してい `style=` 場合は、CSS ルールの descendant セレクターで `.s7zoomviewer` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを適用する場合は、次のように、このセレクターをコンテナ DOM 要素の ID で修飾します。

`#<containerId>.s7zoomviewer`

## レスポンシブデザイン CSS の作成 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSS では様々なデバイスや埋め込みサイズをターゲットにすることができ、ユーザーのデバイスや特定の web ページレイアウトに応じて、コンテンツの表示を異なったものにすることができます。 ターゲット設定には、レイアウトの違い、ユーザーインターフェイスの要素のサイズ、アートワークの解像度などが含まれますが、これらに限定されません。

このビューアは、レスポンシブに設計された CSS を作成する、CSS マーカーと標準の CSS メディアクエリの 2 つのメカニズムをサポートしています。 これらのメカニズムは、個別に使用することも、同時に使用することもできます。

**CSS マーカー**

レスポンシブデザイン CSS の作成に役立つように、ビューアでは CSS マーカーをサポートしています。 これらのマーカーは特別な CSS クラスです。 これらのクラスは、実行時ビューアのサイズと、現在のデバイスで使用されている入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられます。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small` の各クラスが含まれます。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 ビューア領域が一般的なデスクトップモニターのサイズと同じか、それよりも大きい場合は、`.s7size_large` が使用されます。ビューア領域が一般的なタブレットデバイスに近い場合は、`.s7size_medium` が割り当てられます。 携帯電話画面に類似した領域の場合、`.s7size_small` が設定されます。 これらの CSS マーカーの主な目的は、異なる画面およびビューアのサイズに対して異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 番目のグループには、`.s7mouseinput` と `.s7touchinput` が含まれます。 現在のデバイスにタッチ入力機能がある場合は、マーカー `.s7touchinput` が設定されます。それ以外の場合は、`.s7mouseinput` が使用されます。 通常のタッチ入力にはより大きな要素が必要なため、これらのマーカーは主に、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。 デバイスがマウス入力とタッチ機能の両方を備えている場合、`.s7touchinput` れが設定され、ビューアはタッチに対応したユーザーインターフェイスをレンダリングします。

次のサンプル CSS では、マウス入力を含んだシステムではズームインボタンサイズを 28 x 28 ピクセルに設定し、タッチデバイスでは 56 x 56 ピクセルに設定しています。 さらに、ビューアのサイズが小さすぎると、ボタンが完全に非表示になります。

```
.s7zoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7zoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7zoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
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

スタイル設定への従来のアプローチでは、CSS は、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 ズームインボタンのスタイル設定に使用する CSS のサンプルを以下に示します。

```
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

このアプローチの欠点は、要素を初めて操作したときに、エンドユーザーのユーザーインターフェイス応答がちらつきしたり、遅延したりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチでは、サーバーへの HTTP 呼び出し数が増加するので、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる異なるアプローチです。 このような「スプライト」では、特定の要素のすべての視覚状態が順番に配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、CSS 内のすべての異なる状態に対して同じスプライト画像が参照されます。 また、`background-position` プロパティは、各状態に対して使用され、「スプライト」画像の使用部分を指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 ビューアでは通常、画像を垂直方向に積み重ねます。 以下は、「スプライト」ベースの例で、上から同じズームインボタンにスタイルを設定しています。

```
.s7zoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
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

以下は、ビデオビューアに適用されるユーザーインターフェイス要素のリファレンスドキュメントです。
