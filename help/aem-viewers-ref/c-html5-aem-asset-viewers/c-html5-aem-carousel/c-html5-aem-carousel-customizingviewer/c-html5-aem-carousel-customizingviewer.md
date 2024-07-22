---
title: カルーセルビューアのカスタマイズ
description: カルーセルビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行います。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f392d830-5c75-45dd-bab8-29a38218790d
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# カルーセルビューアのカスタマイズ{#customizing-carousel-viewer}

カルーセルビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行います。

推奨されるワークフローは、適切なビューアのデフォルトの CSS ファイルを取得し、別の場所にコピーしてカスタマイズし、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

デフォルトの CSS ファイルは、次の場所にあります。

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

ビューアには、数値とドットのセットインジケーター用の 4 つの標準 CSS ファイルが用意されており、それぞれが「明」と「暗」のカラースキームになっています。 「点光源」バージョンはデフォルトで使用されますが、別の標準 CSS を使用して `SetIndicator.mode` パラメーターを設定することで、別のバージョンに簡単に切り替えることができます。 その他の標準の CSS は次の場所にあります。

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言を含める必要があります。 クラスの宣言を省略すると、ユーザーインターフェイス要素の組み込みの既定のスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、web ページ上で直接埋め込みスタイルを使用するか、リンクされた外部 CSS ルールの 1 つで埋め込みスタイルを使用する方法があります。

カスタム CSS を作成する場合は、ビューアがコンテナの DOM 要素にクラス `.s7carouselviewer` 割り当てることに注意してください。 `style=` コマンドで渡された外部 CSS ファイルを使用している場合は、CSS ルールの descendant セレクターで `.s7carouselviewer` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを追加する場合は、次のように、このセレクターをコンテナ DOM 要素の ID で修飾します。

`#<containerId>.s7carouselviewer`

## レスポンシブデザイン CSS の作成 {#section-0bb49aca42d242d9b01879d5ba59d33b}

CSS では様々なデバイスや埋め込みサイズをターゲットにすることができ、ユーザーのデバイスや特定の web ページレイアウトに応じて、コンテンツの表示を異なったものにすることができます。 この手法には、レイアウトの違い、ユーザーインターフェイス要素のサイズ、アートワークの解像度などが含まれますが、これらに限定されません。

このビューアは、レスポンシブに設計された CSS を作成する、CSS マーカーと標準の CSS メディアクエリの 2 つのメカニズムをサポートしています。 これら 2 つのメカニズムは、個別に使用することも、同時に使用することもできます。

**CSS マーカー**

レスポンシブデザイン CSS の作成に役立つように、ビューアでは CSS マーカーをサポートしています。 これらのマーカーは、最上位のビューアコンテナ要素に動的に割り当てられる特別な CSS クラスです。 これらは、ランタイムビューアのサイズと、現在のデバイスで使用されている入力タイプに基づいています。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium` および `.s7size_small` の各クラスが含まれます。 これらは、ビューアコンテナのランタイム領域に基づいて適用されます。 例えば、ビューア領域が一般的なデスクトップモニターのサイズと同じかそれ以上の場合は、`.s7size_large` を使用します。 領域が共通のタブレットデバイスに近い場合は、`.s7size_medium` を割り当てます。 携帯電話画面に類似した領域の場合は、`.s7size_small` を使用します。 これらの CSS マーカーの主な目的は、異なる画面およびビューアのサイズに対して異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 番目のグループには、`.s7mouseinput` と `.s7touchinput` が含まれます。 現在のデバイスがタッチ入力の場合、CSS マーカー `.s7touchinput` が設定されます。 それ以外の場合は、`.s7mouseinput` が使用されます。 通常のタッチ入力にはより大きな要素が必要なため、これらのマーカーは主に、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。

次のサンプル CSS では、マウス入力システムではズームインボタンサイズを 28 x 28 ピクセルに設定し、タッチ入力デバイスでは 56 x 56 ピクセルに設定します。 ビューアのサイズがさらに小さい場合は、20 x 20 ピクセルに設定されます。

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
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

多くのビューアのユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイルが設定され、複数の異なる表示状態があります。 良い例は、通常、`up`、`over`、`down` の少なくとも 3 つの異なる状態があるボタンです。 各ステートには、独自のビットマップアートワークが割り当てられている必要があります。

スタイル設定への従来のアプローチでは、CSS は、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 ズームインボタンのスタイル設定に使用する CSS のサンプルを以下に示します。

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

このアプローチの欠点は、要素を初めて操作したときに、エンドユーザーのユーザーインターフェイス応答がちらつきしたり、遅延したりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチでは、サーバーへの HTTP 呼び出し数が増加するので、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる異なるアプローチです。 このような「スプライト」では、特定の要素のすべての視覚状態が順番に配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、CSS 内のすべての異なる状態に対して同じスプライト画像が参照されます。 また、`background-position` プロパティは、各状態に対して使用され、「スプライト」画像の使用部分を指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 ビューアでは通常、画像を垂直方向に積み重ねます。

以下は、同じホットスポットアイコンのスタイルを「スプライト」ベースの例です。

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## 一般的なスタイル設定のメモとアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS を使用してビューアユーザーインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールを使用してビューア要素のスタイルを設定することはできません。 特に、ビューア `!IMPORTANT` たはビューア SDK から提供されるデフォルトまたはランタイムのスタイル設定を上書きする場合は、このルールを使用しないでください。 その理由は、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、適切な特異性を持つ CSS セレクターを使用して、このビューアリファレンスガイドに記載されている CSS プロパティを設定する必要があります。
* CSS 内の外部アセットへのすべてのパスは、ビューアHTMLページの場所ではなく CSS の場所に対して解決されます。 デフォルトの CSS を別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタム CSS 内のすべてのパスを更新します。
* ビットマップアートワークの形式は PNG が推奨されます。
* ビットマップアートワークは、`background-image` プロパティを使用してユーザーインターフェイス要素に割り当てられます。
* ユーザーインターフェイス要素の `width` プロパティと `height` プロパティは、その論理サイズを定義します。 `background-image` に渡されるビットマップのサイズは、その論理サイズに影響しません。
* Retina のような高解像度の画面で高いピクセル密度を使用するには、ビットマップアートワークを論理ユーザーインターフェイス要素のサイズの 2 倍の大きさに指定します。 次に、`-webkit-background-size:contain` プロパティを適用して、背景を論理ユーザーインターフェイス要素サイズに縮小します。
* ユーザーインターフェイスからボタンを削除するには、CSS クラスに `display:none` を追加します。
* CSS がサポートするカラー値に対して様々な形式を使用できます。 透明度が必要な場合は、形式 `rgba(R,G,B,A)` を使用します。 それ以外の場合は、`#RRGGBB` 形式を使用できます。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下は、ビデオ画像ビューアに適用されるユーザーインターフェイス要素のリファレンスドキュメントです。
