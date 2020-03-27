---
description: eCatalog検索ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
keywords: responsive
seo-description: eCatalog検索ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。
seo-title: eCatalog検索ビューアのカスタマイズ
solution: Experience Manager
title: eCatalog検索ビューアのカスタマイズ
topic: Dynamic media
uuid: a715399b-7b02-4656-8257-4c390c6f629c
translation-type: tm+mt
source-git-commit: 8d7fdab78c5d23d0e541effa9b9c470921bd144b

---


# eCatalog検索ビューアのカスタマイズ{#customizing-ecatalog-search-viewer}

eCatalog検索ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタムCSSを作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定のCSSファイルを別の場所にコピーし、カスタマイズして、コマンドでカスタマイズしたファイルの場所を指定すること `style=` です。

初期設定のCSSファイルは、次の場所にあります。

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

カスタムCSSファイルには、初期設定のCSSファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていません。

カスタムCSSルールを指定する別の方法は、Webページ上またはリンクされたいずれかの外部CSSルール内で、埋め込みスタイルを直接使用することです。

カスタムCSSを作成する場合、ビューアはコンテナのDOM要素にク `.s7ecatalogsearchviewer` ラスを割り当てることに注意してください。 コマンドで渡された外部CSSファイルを使用する場合は、CSS `style=` ルールの子孫セレ `.s7ecatalogsearchviewer` クターでクラスを親クラスとして使用します。 Webページ上で埋め込みスタイルを使用する場合は、このセレクターを次のようにコンテナのDOM要素のIDで修飾します。

`#<containerId>.s7ecatalogsearchviewer`

## レスポンシブデザインCSSの構築 {#section-c1e74f5114ad418884ca1c95f5ea5b63}

CSSで様々なデバイスや埋め込みサイズをターゲットにして、ユーザーのデバイスや特定のWebページのレイアウトに応じてコンテンツの表示を変えることができます。 これには、Webページのレイアウト、ユーザインターフェイス要素のサイズ、アートワークの解像度が含まれますが、これらに限定されません。

ビューアでは、レスポンシブデザインCSSを作成する方法が2つサポートされています。CSSマーカーと標準のCSSメディアクエリ。 これらの方法は、個別に、または一緒に使用できます。

**CSSマーカー**

レスポンシブデザインCSSの作成を支援するため、ビューアでは、実行時のビューアサイズと現在のデバイスで使用されている入力タイプに基づいて、特別なCSSクラスを最上位のビューアコンテナ要素に動的に割り当てるCSSマーカーがサポートされています。

CSSマーカーの最初のグループには、、、 `.s7size_large`および `.s7size_medium`クラスが含ま `.s7size_small` れます。 これらは、ビューアコンテナの実行時の領域に基づいて適用されます。 つまり、ビューアの領域が一般的なデスクトップモニターと同じかそれ以上のサイズである場合、次のよう `.s7size_large` になります。領域のサイズが一般的なタブレットデバイスに近い場合は、こ `.s7size_medium` の値が割り当てられます。 携帯電話の画面に似た領域が設定さ `.s7size_small` れている。 これらのCSSマーカーの主な目的は、画面やビューアサイズごとに異なるユーザインターフェイスレイアウトを作成することです。

CSSマーカーの2番目のグループには、とが含ま `.s7mouseinput` れま `.s7touchinput`す。 `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合は、 `.s7mouseinput` が使用されます。 これらのマーカーは、入力タイプごとに画面サイズが異なるユーザーインターフェイス入力要素を作成することを目的としています。通常、タッチ入力にはより大きな要素が必要なためです。 デバイスにマウス入力とタッチの両方の機能がある場合は、が設定され、 `.s7touchinput` ビューアによってタッチ操作に適したユーザインターフェイスがレンダリングされます。

以下のサンプルCSSでは、ズームインボタンのサイズを、マウス入力のシステムでは28 x 28ピクセルに、タッチデバイスでは56 x 56ピクセルに設定します。 また、ビューアのサイズが非常に小さくなると、ボタンは完全に非表示になります。

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

ピクセル密度が異なるデバイスをターゲットにするには、CSSメディアクエリを使用します。 次のメディアクエリブロックには、高密度画面に固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSSマーカーの使用は、レスポンシブデザインCSSを構築する最も柔軟な方法です。デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにできるので、これはレスポンシブデザインページレイアウトに便利です。

初期設定のビューアのCSSファイルを、CSSマーカーアプローチの例として使用します。

**CSSメディアクエリ**

デバイスの検出は、純粋なCSSメディアクエリを使用して行うこともできます。 特定のメディアクエリブロック内に含まれるすべての要素は、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、4つのCSSメディアクエリを使用します。このクエリは、CSS内で次の順序で定義されます。

1. すべてのタッチデバイスに固有のルールのみを含みます。

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

1. 高解像度画面の携帯電話に固有のルールのみを含めます。

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

メディアクエリアプローチを使用する場合は、次のようにデバイス検出を行うCSSを整理する必要があります。

* まず、デスクトップ固有のセクションで、デスクトップ固有またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4つのメディアクエリを上記の定義の順に記述し、対応するデバイスタイプに固有のCSSルールを指定します。

各メディアクエリでビューアのCSS全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみがメディアクエリ内で再定義されます。

## CSSスプライト {#section-9d570f95eb2443aca74c1b02f6e89aff}

多くのビューアのユーザインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる表示状態を持ちます。 良い例は、通常は少なくとも3つの異なる状態を持つボタンです。「up」、「over」および「down」 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定手法では、CSSは、ユーザインターフェイス要素の状態ごとに、サーバ上の個々の画像ファイルを個別に参照します。 以下は、ズームインボタンのスタイル設定に使用するCSSの例です。

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

このアプローチの欠点は、エンドユーザーが、要素が初めて操作されたときに、ちらつきや遅延が発生することです。 このアクションは、新しい要素状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法は、サーバーへのHTTP呼び出しの数が増えたため、パフォーマンスに若干悪影響を与える可能性があります。

CSSスプライトは、すべての要素の状態の画像アートワークを「スプライト」と呼ばれる単一のPNGファイルに結合する別の方法です。 このような「スプライト」は、指定された要素のすべての視覚的な状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSSのすべての異なる状態に対して同じスプライト画像が参照されます。 また、このプロ `background-position` パティは、「スプライト」画像のどの部分を使用するかを指定するために各状態に使用されます。 「スプライト」画像は、適切な方法で構成できます。 通常、ビューアは縦に積み重ねられます。 以下に、上から同じズームインボタンをスタイル設定する「スプライト」ベースの例を示します。

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## スタイルに関する一般的な注意とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSSでビューアのユーザインターフェイスをカスタマイズする場合、ビューア要素のス `!IMPORTANT` タイル設定に対するルールの使用はサポートされていません。 特に、ビューアま `!IMPORTANT` たはビューアSDKが提供するデフォルトのスタイルや実行時のスタイルを上書きする際には、ルールを使用しないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このリファレンスガイドに記載されているCSSプロパティを設定するには、CSSセレクターを適切な仕様で使用する必要があります。
* CSS内の外部アセットへのパスは、ビューアのHTMLページの場所ではなく、CSSの場所を基準に解決されます。 初期設定のCSSを別の場所にコピーする場合は、このルールに注意してください。 初期設定のアセットもコピーするか、カスタムCSS内のパスを更新します。
* ビットマップアートワークに推奨される形式はPNGです。
* ビットマップアートワークは、このプロパティを使用してユーザインターフェイス要素に割り当 `background-image` てられます。
* ユーザイン `width` ターフ `height` ェイス要素の論理サイズは、およびプロパティで定義します。 に渡されるビットマップのサイズは、論 `background-image` 理サイズに影響しません。
* Retinaなどの高ピクセル密度の高解像度画面を使用するには、論理ユーザインターフェイス要素の2倍の大きさのビットマップアートワークを指定します。 次に、このプロパティを適 `-webkit-background-size:contain` 用して、背景を論理ユーザインターフェイス要素のサイズに合わせて縮小します。
* ユーザーインターフェイスからボタンを削除するには、CSSク `display:none` ラスにを追加します。
* カラー値には、CSSでサポートされる様々な形式を使用できます。 透明度が必要な場合は、形式を使用しま `rgba(R,G,B,A)`す。 それ以外の場合は、形式を使用できま `#RRGGBB`す。

## 共通のユーザインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

eCatalog検索ビューアに適用されるユーザインターフェイス要素リファレンスドキュメントを次に示します。

* [お気に入りを追加ボタン](r-html5-ecatsearch-customize-addfavorite.md)
* [閉じるボタン](r-html5-ecatsearch-customize-closebutton.md)
* [ダウンロード:](r-html5-ecatsearch-customize-download.md)
* [電子メール共有](r-html5-ecatsearch-customize-emailshare.md)
* [埋め込み共有](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook共有](r-html5-ecatsearch-customize-facebookshare.md)
* [お気に入りエフェクト](r-html5-ecatsearch-customize-favoriteseffect.md)
* [お気に入りメニュー](r-html5-ecatsearch-customize-favoritesmenu.md)
* [お気に入りビュー](r-html5-ecatsearch-customize-favoritesview.md)
* [最初のページボタン](r-html5-ecatsearch-customize-firstpagebutton.md)
* [フォーカスハイライト](r-html5-ecatsearch-customize-focushighlight.md)
* [フルスクリーンボタン](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [アイコンエフェクト](r-html5-ecatsearch-customize-iconeffect.md)
* [情報パネルポップアップ](r-html5-ecatsearch-customize-infopanelpopup.md)
* [画像マップ効果](r-html5-ecatsearch-customize-imagemapeffect.md)
* [次の大きいページボタン](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [1つ前の大きいページボタン](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [最後のページボタン](r-html5-ecatsearch-customize-lastpagebutton.md)
* [リンク共有](r-html5-ecatsearch-customize-linkshare.md)
* [メインコントロールバー](r-html5-ecatsearch-customize-maincontrolbar.md)
* [メインビューア領域](r-html5-ecatsearch-customize-mainviewerarea.md)
* [次のページボタン](r-html5-ecatsearch-customize-nextpagebutton.md)
* [ページインジケーター](r-html5-ecatsearch-customize-pageindicator.md)
* [ページビュー](r-html5-ecatsearch-customize-pageview.md)
* [前のページボタン](r-html5-ecatsearch-customize-previouspagebutton.md)
* [印刷](r-html5-ecatalog-viewer-20-customize-print.md)
* [お気に入りを削除ボタン](r-html5-ecatsearch-customize-removefavorite.md)
* [検索ボタン](r-html5-ecatsearch-customize-searchbutton.md)
* [検索効果](r-html5-ecatsearch-customize-searcheffect.md)
* [検索結果パネル](r-html5-ecatsearch-customize-searchresultspanel.md)
* [セカンダリコントロールバー](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [ソーシャルシェア](r-html5-ecatsearch-customize-socialshare.md)
* [目次](r-html5-ecatsearch-customize-tableofcontents.md)
* [サムネール](r-html5-ecatsearch-customize-thumbnails.md)
* [サムネールボタン](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [ツールチップ](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter共有](r-html5-ecatsearch-customize-twittershare.md)
* [すべてのお気に入りを表示ボタン](r-html5-ecatsearch-customize-viewallfavorites.md)
* [ズームインボタン](r-html5-ecatsearch-customize-zoominbutton.md)
* [ズームアウトボタン](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [ズームリセットボタン](r-html5-ecatsearch-customize-zoomresetbutton.md)

