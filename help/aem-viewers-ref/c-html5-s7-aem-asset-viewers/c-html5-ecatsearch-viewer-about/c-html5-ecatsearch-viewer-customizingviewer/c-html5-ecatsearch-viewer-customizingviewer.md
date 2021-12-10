---
title: eCatalog 検索ビューアのカスタマイズ
description: eCatalog 検索ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# eCatalog 検索ビューアのカスタマイズ{#customizing-ecatalog-search-viewer}

eCatalog 検索ビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定の CSS ファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を `style=` コマンドを使用します。

初期設定の CSS ファイルは次の場所にあります。

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

カスタムの CSS ファイルには、デフォルトの CSS ファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていないからです。

カスタムの CSS ルールを指定する別の方法は、Web ページ上またはリンクされた外部 CSS ルールの 1 つで、埋め込みスタイルを直接使用することです。

カスタム CSS を作成する場合、ビューアに `.s7ecatalogsearchviewer` クラスをコンテナの DOM 要素に追加します。 外部 CSS ファイルを使用し、 `style=` コマンド、使用 `.s7ecatalogsearchviewer` クラスを親クラスとして、CSS ルールの子孫セレクターに含めます。 Web ページで埋め込みスタイルを使用している場合は、次のようにコンテナの DOM 要素の ID でこのセレクターを修飾する必要があります。

`#<containerId>.s7ecatalogsearchviewer`

## レスポンシブデザイン CSS の構築 {#section-c1e74f5114ad418884ca1c95f5ea5b63}

CSS で様々なデバイスおよび埋め込みサイズをターゲットにして、ユーザーのデバイスや特定の Web ページのレイアウトに応じて、コンテンツの表示を異なる方法でおこなうことができます。 このターゲット設定では、Web ページのレイアウト、ユーザーインターフェイス要素のサイズ、アートワークの解像度などを指定できますが、これらに限定されません。

ビューアでは、レスポンシブデザイン CSS の作成に 2 つの方法がサポートされています。CSS マーカーと標準の CSS メディアクエリ。 これらの方法は、個別に、または一緒に使用できます。

**CSS マーカー**

レスポンシブデザイン CSS を作成するために、ビューアでは、実行時のビューアサイズと現在のデバイスの入力タイプに基づいて、最上位のビューアコンテナ要素に動的に割り当てられる特別な CSS クラスを持つ CSS マーカーがサポートされています。

CSS マーカーの最初のグループには、以下が含まれます。 `.s7size_large`, `.s7size_medium`、および `.s7size_small` クラス。 これらは、ビューアコンテナの実行時領域に基づいて適用されます。 つまり、ビューアの領域が一般的なデスクトップモニターのサイズ以上の場合 `.s7size_large` が使用されます。領域のサイズが一般的なタブレットデバイスに近い場合 `.s7size_medium` が割り当てられます。 携帯電話の画面に似た領域の場合。 マーカー `.s7size_small` が設定されている。 これらの CSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの 2 つ目のグループには、以下が含まれます。 `.s7mouseinput` および `.s7touchinput`. マーカー `.s7touchinput` は、現在のデバイスにタッチ入力機能がある場合に設定されます。それ以外の場合は `.s7mouseinput` が使用されます。 これらのマーカーは、入力タイプごとに異なる画面サイズでユーザインターフェイス入力要素を作成することを目的としています。通常、タッチ入力にはより大きな要素が必要になるからです。 デバイスにマウス入力機能とタッチ機能の両方がある場合、 `.s7touchinput` が設定され、ビューアによってタッチ操作に適したユーザーインターフェイスがレンダリングされます。

以下のサンプル CSS では、ズームインボタンのサイズを、マウス入力のシステムでは 28 x 28 ピクセルに設定し、タッチデバイスでは 56 x 56 ピクセルに設定します。 また、ビューアのサイズが小さすぎると、ボタンは完全に非表示になります。

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

ピクセル密度が異なるデバイスをターゲットにするには、CSS メディアクエリを使用します。 次のメディアクエリブロックには、高密度の画面に固有の CSS が含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーを使用すると、レスポンシブデザイン CSS を柔軟に作成できます。 デバイスの画面サイズだけでなく、実際のビューアサイズもターゲットにでき、レスポンシブデザインのページレイアウトに役立ちます。

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

メディアクエリアプローチを使用する場合、デバイス検出を含む CSS を次のように整理する必要があります。

* まず、デスクトップ固有のセクションで、デスクトップに固有の、またはすべての画面に共通のすべてのプロパティを定義します。
* 次に、4 つのメディアクエリを上で定義した順序に従って、対応するデバイスタイプに固有の CSS ルールを指定します。

各メディアクエリでビューアの CSS 全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSS スプライト {#section-9d570f95eb2443aca74c1b02f6e89aff}

多くのビューアユーザインターフェイス要素は、ビットマップアートワークを使用してスタイルを設定し、複数の異なる視覚状態を持ちます。 良い例として、通常は少なくとも 3 つの異なる状態を持つボタンがあります。&quot;up&quot;、&quot;over&quot;、&quot;down&quot; 各ステートには、独自のビットマップアートワークを割り当てる必要があります。

従来のスタイル設定アプローチでは、CSS には、ユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照が含まれていました。 次に、ズームインボタンのスタイル設定用の CSS の例を示します。

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

このアプローチの欠点は、要素が初めてで操作されると、エンドユーザーがユーザーインターフェイスの応答がちらつく、または遅延することです。 このアクションは、新しい要素の状態の画像アートワークがまだダウンロードされていないために発生します。 また、この方法では、サーバーへの HTTP 呼び出しの数が増えるので、パフォーマンスに若干の悪影響が及ぶ場合があります。

CSS スプライトは、すべての要素状態の画像アートワークを「スプライト」と呼ばれる単一の PNG ファイルに組み合わせる場合とは異なるアプローチです。 このような「スプライト」は、指定された要素のすべての視覚状態を次々に配置します。 スプライトを使用してユーザインターフェイス要素をスタイル設定する場合、CSS 内のすべての異なる状態で同じスプライト画像が参照されます。 また、 `background-position` プロパティは、「sprite」イメージのどの部分を使用するかを指定するために各状態に対して使用されます。 「スプライト」イメージを適切な方法で構築できます。 通常、ビューアは垂直方向に積み重ねられます。 以下は、上記と同じズームインボタンのスタイルを「スプライト」ベースに設定した例です。

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

## スタイルに関する一般的な注意事項とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS を使用してビューアのユーザインターフェイスをカスタマイズする場合、 `!IMPORTANT` ルールは、ビューア要素のスタイル設定に対してサポートされていません。 特に `!IMPORTANT` ルールを使用して、ビューアまたは Viewer SDK が提供するデフォルトのスタイルや実行時のスタイルを上書きしないでください。 これは、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このリファレンスガイドに記載されている CSS プロパティを設定するには、適切な特異性を持つ CSS セレクターを使用する必要があります。
* CSS 内で指定されている外部アセットへのパスは、ビューアのパスページの場所ではなく、CSS の場所を基準にHTMLされます。 デフォルトの CSS を別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタム CSS 内でパスを更新します。
* ビットマップアートワークの推奨される形式は PNG です。
* ビットマップアートワークは、 `background-image` プロパティ。
* この `width` および `height` 論理サイズを定義するユーザーインターフェイス要素のプロパティ。 に渡すビットマップのサイズ `background-image` は論理サイズに影響しません。
* Retina のような高解像度画面の高ピクセル密度を使用するには、論理ユーザインターフェイス要素の 2 倍の大きさのビットマップアートワークを指定します。 次に、 `-webkit-background-size:contain` プロパティを使用して、背景を論理ユーザーインターフェイス要素のサイズまで縮小できます。
* ユーザーインターフェイスからボタンを削除するには、 `display:none` を CSS クラスに追加する。
* カラー値には、CSS でサポートされる様々な形式を使用できます。 透明度が必要な場合は、次の形式を使用します。 `rgba(R,G,B,A)`. それ以外の場合は、 `#RRGGBB`.

## 共通のユーザインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

eCatalog 検索ビューアに適用されるユーザーインターフェイス要素リファレンスドキュメントを次に示します。

* [お気に入りを追加ボタン](r-html5-ecatsearch-customize-addfavorite.md)
* [閉じるボタン](r-html5-ecatsearch-customize-closebutton.md)
* [ダウンロード](r-html5-ecatsearch-customize-download.md)
* [メール共有](r-html5-ecatsearch-customize-emailshare.md)
* [埋め込み共有](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook共有](r-html5-ecatsearch-customize-facebookshare.md)
* [お気に入りエフェクト](r-html5-ecatsearch-customize-favoriteseffect.md)
* [お気に入りメニュー](r-html5-ecatsearch-customize-favoritesmenu.md)
* [お気に入り表示](r-html5-ecatsearch-customize-favoritesview.md)
* [最初のページボタン](r-html5-ecatsearch-customize-firstpagebutton.md)
* [フォーカスのハイライト](r-html5-ecatsearch-customize-focushighlight.md)
* [全画面表示ボタン](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [アイコンエフェクト](r-html5-ecatsearch-customize-iconeffect.md)
* [情報パネルポップアップ](r-html5-ecatsearch-customize-infopanelpopup.md)
* [画像マップ効果](r-html5-ecatsearch-customize-imagemapeffect.md)
* [次の大きいページボタン](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [前のページの大きいボタン](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [最後のページボタン](r-html5-ecatsearch-customize-lastpagebutton.md)
* [リンク共有](r-html5-ecatsearch-customize-linkshare.md)
* [メインコントロールバー](r-html5-ecatsearch-customize-maincontrolbar.md)
* [メインビューア領域](r-html5-ecatsearch-customize-mainviewerarea.md)
* [次のページボタン](r-html5-ecatsearch-customize-nextpagebutton.md)
* [ページインジケーター](r-html5-ecatsearch-customize-pageindicator.md)
* [ページビュー](r-html5-ecatsearch-customize-pageview.md)
* [「前のページ」ボタン](r-html5-ecatsearch-customize-previouspagebutton.md)
* [印刷](r-html5-ecatsearch-customize-print.md)
* [お気に入りを削除ボタン](r-html5-ecatsearch-customize-removefavorite.md)
* [検索ボタン](r-html5-ecatsearch-customize-searchbutton.md)
* [検索効果](r-html5-ecatsearch-customize-searcheffect.md)
* [検索結果パネル](r-html5-ecatsearch-customize-searchresultspanel.md)
* [セカンダリコントロールバー](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [ソーシャル共有](r-html5-ecatsearch-customize-socialshare.md)
* [目次](r-html5-ecatsearch-customize-tableofcontents.md)
* [サムネール](r-html5-ecatsearch-customize-thumbnails.md)
* [サムネールボタン](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [ツールチップ](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter共有](r-html5-ecatsearch-customize-twittershare.md)
* [[ すべてのお気に入りを表示 ] ボタン](r-html5-ecatsearch-customize-viewallfavorites.md)
* [ズームインボタン](r-html5-ecatsearch-customize-zoominbutton.md)
* [ズームアウトボタン](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [ズームのリセットボタン](r-html5-ecatsearch-customize-zoomresetbutton.md)
