---
title: eCatalog 検索ビューアのカスタマイズ
description: e カタログ検索ビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行います。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# eCatalog 検索ビューアのカスタマイズ{#customizing-ecatalog-search-viewer}

e カタログ検索ビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行います。

推奨されるワークフローは、適切なビューアのデフォルトの CSS ファイルを取得し、別の場所にコピーしてカスタマイズし、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

デフォルトの CSS ファイルは、次の場所にあります。

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言を含める必要があります。 クラスの宣言を省略すると、ユーザーインターフェイス要素の組み込みの既定のスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、web ページ上で直接埋め込みスタイルを使用するか、リンクされた外部 CSS ルールの 1 つで埋め込みスタイルを使用する方法があります。

カスタム CSS を作成する場合は、ビューアがコンテナの DOM 要素にクラス `.s7ecatalogsearchviewer` 割り当てることに注意してください。 `style=` コマンドで渡された外部 CSS ファイルを使用している場合は、CSS ルールの descendant セレクターで `.s7ecatalogsearchviewer` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを適用する場合は、次のように、このセレクターをコンテナ DOM 要素の ID で修飾する必要もあります。

`#<containerId>.s7ecatalogsearchviewer`

## レスポンシブデザイン CSS の作成 {#section-c1e74f5114ad418884ca1c95f5ea5b63}

CSS では様々なデバイスや埋め込みサイズをターゲットにすることができ、ユーザーのデバイスや特定の web ページレイアウトに応じて、コンテンツの表示を異なったものにすることができます。 このターゲティングには、web ページレイアウトの違い、ユーザーインターフェイス要素のサイズおよびアートワークの解像度などが含まれますが、これらに限定されません。

ビューアは、レスポンシブデザイン CSS を作成する 2 つの方法（CSS マーカーと標準の CSS メディアクエリ）をサポートしています。 これらのメソッドは、個別に使用することも、同時に使用することもできます。

**CSS マーカー**

レスポンシブデザイン CSS を作成するために、ビューアは CSS マーカーをサポートしています。この CSS クラスは、実行時のビューアサイズと現在のデバイスの入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられます。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`、`.s7size_small` の各クラスが含まれます。 これらは、ビューアコンテナのランタイム領域に基づいて適用されます。 つまり、ビューア領域のサイズが、使用される共通のデスクトップモニターのサイズと同じかそれ以上の場合、`.s7size_large` の領域のサイズが、割り当てられる共通のタブレットデバイスに近い場合 `.s7size_medium` す。 携帯電話画面に類似したエリアの場合。 マーカー `.s7size_small` が設定されます。 これらの CSS マーカーの主な目的は、異なる画面およびビューアのサイズに対して異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 番目のグループには、`.s7mouseinput` と `.s7touchinput` が含まれます。 現在のデバイスにタッチ入力機能がある場合は、マーカー `.s7touchinput` が設定されます。それ以外の場合は、`.s7mouseinput` が使用されます。 これらのマーカーは、通常のタッチ入力にはより大きな要素が必要なので、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。 デバイスがマウス入力とタッチ機能の両方を備えている場合、`.s7touchinput` れが設定され、ビューアはタッチに対応したユーザーインターフェイスをレンダリングします。

次のサンプル CSS では、マウス入力を含んだシステムではズームインボタンサイズを 28 x 28 ピクセルに設定し、タッチデバイスでは 56 x 56 ピクセルに設定しています。 さらに、ビューアのサイズが小さすぎると、ボタンが完全に非表示になります。

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

ピクセル密度の異なるデバイスをターゲットにするには、CSS メディアクエリを使用します。 次のメディアクエリーブロックは、高密度画面に固有の CSS を含んでいます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーの使用は、レスポンシブデザインの CSS を構築するための最も柔軟な方法です。 デバイスの画面サイズだけでなく、実際のビューアのサイズもターゲットにできるので、レスポンシブデザインのページレイアウトに役立ちます。

CSS マーカーアプローチの例として、デフォルトのビューア CSS ファイルを使用します。

**CSS メディアクエリ**

デバイスの検出は、純粋な CSS メディアクエリを使用して実行することもできます。 特定のメディアクエリブロック内に含まれているすべてが、対応するデバイスで実行された場合にのみ適用されます。

モバイルビューアに適用する場合は、4 つの CSS メディアクエリを使用します。CSS では次の順序で定義されます。

1. すべてのタッチデバイスに固有のルールのみが含まれます。

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

## CSS スプライト {#section-9d570f95eb2443aca74c1b02f6e89aff}

多くのビューアのユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイルが設定され、複数の異なる表示状態があります。 良い例は、通常、「上」、「オーバー」、「下」の少なくとも 3 つの異なる状態があるボタンです。 各ステートには、独自のビットマップアートワークが割り当てられている必要があります。

スタイル設定への従来のアプローチでは、CSS は、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 ズームインボタンのスタイル設定に使用する CSS のサンプルを以下に示します。

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

このアプローチの欠点は、要素を初めて操作したときに、エンドユーザーのユーザーインターフェイス応答がちらつきしたり、遅延したりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチでは、サーバーへの HTTP 呼び出し数が増加するので、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる異なるアプローチです。 このような「スプライト」では、特定の要素のすべての視覚状態が順番に配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、CSS 内のすべての異なる状態に対して同じスプライト画像が参照されます。 また、`background-position` プロパティは、各状態に対して使用され、「スプライト」画像の使用部分を指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 ビューアでは通常、画像を垂直方向に積み重ねます。 以下は、「スプライト」ベースの例で、上から同じズームインボタンにスタイルを設定しています。

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

eCatalog 検索ビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを以下に示します。

* [「お気に入りに追加」ボタン](r-html5-ecatsearch-customize-addfavorite.md)
* [「閉じる」ボタン](r-html5-ecatsearch-customize-closebutton.md)
* [ダウンロード](r-html5-ecatsearch-customize-download.md)
* [メール共有](r-html5-ecatsearch-customize-emailshare.md)
* [共有を埋め込む](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook共有](r-html5-ecatsearch-customize-facebookshare.md)
* [お気に入りエフェクト](r-html5-ecatsearch-customize-favoriteseffect.md)
* [お気に入りメニュー](r-html5-ecatsearch-customize-favoritesmenu.md)
* [お気に入り表示](r-html5-ecatsearch-customize-favoritesview.md)
* [最初のページボタン](r-html5-ecatsearch-customize-firstpagebutton.md)
* [フォーカスのハイライト](r-html5-ecatsearch-customize-focushighlight.md)
* [全画面表示ボタン](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [アイコン効果](r-html5-ecatsearch-customize-iconeffect.md)
* [情報パネルポップアップ](r-html5-ecatsearch-customize-infopanelpopup.md)
* [画像マップエフェクト](r-html5-ecatsearch-customize-imagemapeffect.md)
* [大きい次のページのボタン](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [大きい [ 前のページ ] ボタン](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [最後のページボタン](r-html5-ecatsearch-customize-lastpagebutton.md)
* [リンク共有](r-html5-ecatsearch-customize-linkshare.md)
* [メインコントロールバー](r-html5-ecatsearch-customize-maincontrolbar.md)
* [メインビューア領域](r-html5-ecatsearch-customize-mainviewerarea.md)
* [「次のページ」ボタン](r-html5-ecatsearch-customize-nextpagebutton.md)
* [ページインジケーター](r-html5-ecatsearch-customize-pageindicator.md)
* [ページビュー](r-html5-ecatsearch-customize-pageview.md)
* [「前のページ」ボタン](r-html5-ecatsearch-customize-previouspagebutton.md)
* [印刷](r-html5-ecatsearch-customize-print.md)
* [「お気に入りを削除」ボタン](r-html5-ecatsearch-customize-removefavorite.md)
* [「検索」ボタン](r-html5-ecatsearch-customize-searchbutton.md)
* [検索効果](r-html5-ecatsearch-customize-searcheffect.md)
* [検索結果パネル](r-html5-ecatsearch-customize-searchresultspanel.md)
* [セカンダリコントロールバー](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [ソーシャル共有](r-html5-ecatsearch-customize-socialshare.md)
* [目次](r-html5-ecatsearch-customize-tableofcontents.md)
* [サムネール](r-html5-ecatsearch-customize-thumbnails.md)
* [「サムネール」ボタン](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [ツールチップ](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter共有](r-html5-ecatsearch-customize-twittershare.md)
* [「すべてのお気に入りを表示」ボタン](r-html5-ecatsearch-customize-viewallfavorites.md)
* [「ズームイン」ボタン](r-html5-ecatsearch-customize-zoominbutton.md)
* [ズームアウトボタン](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [ズームリセットボタン](r-html5-ecatsearch-customize-zoomresetbutton.md)
