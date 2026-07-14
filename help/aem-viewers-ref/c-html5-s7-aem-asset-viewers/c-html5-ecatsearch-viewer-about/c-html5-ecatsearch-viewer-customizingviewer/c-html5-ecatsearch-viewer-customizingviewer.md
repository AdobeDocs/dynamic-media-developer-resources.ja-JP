---
title: eCatalog Search Viewerのカスタマイズ
description: eCatalog Search Viewerのビジュアルカスタマイズと動作のカスタマイズは、すべてカスタム CSSを作成して行います。
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
TQID: 'https://experienceleague.adobe.com/8a2nFReDg4jHF9DrvGHuXIMZWrqdDpoUGvqvh4f6CcM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 1414
ht-degree: 0%

---

# eCatalog Search Viewerのカスタマイズ{#customizing-ecatalog-search-viewer}

eCatalog Search Viewerのビジュアルカスタマイズと動作のカスタマイズは、すべてカスタム CSSを作成して行います。

推奨されるワークフローは、適切なビューアのデフォルトのCSS ファイルを取得し、別の場所にコピーしてカスタマイズし、`style=` コマンドでカスタマイズしたファイルの場所を指定することです。

デフォルトのCSS ファイルは次の場所にあります。

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言が含まれている必要があります。 クラス宣言を省略すると、ユーザーインターフェイス要素に組み込みのデフォルトスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、埋め込みスタイルをweb ページまたはリンクされた外部CSS ルールのいずれかに直接使用することもできます。

カスタム CSSを作成する場合、ビューアはコンテナ DOM要素に`.s7ecatalogsearchviewer` クラスを割り当てることに注意してください。 `style=` コマンドで渡された外部CSS ファイルを使用している場合は、CSS ルールの子孫セレクターで`.s7ecatalogsearchviewer` クラスを親クラスとして使用します。 Web ページで埋め込みスタイルを実行する場合は、このセレクターをコンテナ DOM要素のIDで次のように修飾する必要があります。

`#<containerId>.s7ecatalogsearchviewer`

## レスポンシブデザインのCSSを作成する {#section-c1e74f5114ad418884ca1c95f5ea5b63}

ユーザーのデバイスや特定のweb ページレイアウトに応じて、コンテンツの表示を異なるように、さまざまなデバイスやCSSへの埋め込みサイズをターゲットにすることができます。 このターゲティングには、異なるweb ページレイアウト、ユーザーインターフェイス要素のサイズ、アートワークの解像度が含まれますが、これらに限定されません。

ビューアは、レスポンシブデザインのCSSを作成する方法として、CSS マーカーと標準のCSS メディアクエリの2つをサポートしています。 これらの方法は、単独でも一緒でも使用できます。

**CSS マーカー**

レスポンシブデザインのCSSを作成するには、ビューアは、実行時のビューアサイズと現在のデバイス上の入力タイプに基づいて、トップレベルのビューアコンテナ要素に動的に割り当てられた特殊なCSS クラスであるCSS マーカーをサポートします。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`および`.s7size_small`個のクラスが含まれています。 ビューアコンテナのランタイム領域に基づいて適用されます。 つまり、ビューア領域が一般的なデスクトップモニター`.s7size_large`のサイズと同じかそれより大きい場合、または共通のタブレットデバイス `.s7size_medium`にサイズが近い場合に割り当てられます。 モバイルデバイスと類似した領域の場合。 マーカー`.s7size_small`が設定されています。 これらのCSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの2番目のグループには、`.s7mouseinput`と`.s7touchinput`が含まれています。 現在のデバイスにタッチ入力機能がある場合は、マーカー`.s7touchinput`が設定されます。それ以外の場合は、`.s7mouseinput`が使用されます。 これらのマーカーは、通常タッチ入力には大きな要素が必要なため、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。 デバイスにマウス入力とタッチ機能の両方がある場合は、`.s7touchinput`が設定され、ビューアはタッチ対応のユーザーインターフェイスをレンダリングします。

次のCSSの例では、マウスを入力したシステムではズームインボタンのサイズを28 x 28 ピクセル、タッチデバイスでは56 x 56 ピクセルに設定しています。 さらに、ビューアサイズが小さすぎると、ボタンが完全に非表示になります。

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

異なるピクセル密度のデバイスをターゲットにするには、CSS メディアクエリを使用します。 次のメディアクエリブロックには、高密度スクリーンに固有のCSSが含まれます。

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

CSS マーカーを使用することは、レスポンシブデザインのCSSを作成する最も柔軟な方法です。 デバイスの画面サイズだけでなく、実際の視聴者サイズもターゲットにすることができ、レスポンシブデザインのページレイアウトに役立ちます。

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

メディアクエリのアプローチを使用して、デバイスセンシングでCSSを整理する必要があります。

* まず、「デスクトップ固有」セクションでは、デスクトップ固有またはすべてのスクリーンに共通するすべてのプロパティを定義します。
* 2つ目は、4つのメディアクエリが上記で定義された順序で行われ、対応するデバイスタイプに固有のCSS ルールが提供されます。

各メディアクエリでビューア CSS全体を複製する必要はありません。 特定のデバイスに固有のプロパティのみが、メディアクエリ内で再定義されます。

## CSS スプライト {#section-9d570f95eb2443aca74c1b02f6e89aff}

多くのビューアーユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる視覚状態を持ちます。 良い例は、通常は「up」、「over」、「down」の3つの異なる状態を持つボタンです。 各ステートには、割り当てられた独自のビットマップアートワークが必要です。

スタイル設定に対する従来のアプローチでは、CSSはユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 次に、ズームインボタンのスタイル設定に使用するCSSの例を示します。

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

このアプローチの欠点は、要素が初めて操作されたときに、エンドユーザーがちらついたり、ユーザーインターフェイスの応答が遅れたりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出し数が増加するため、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべてのエレメント状態の画像アートワークを「スプライト」と呼ばれる1つのPNG ファイルに結合する別のアプローチです。 このような「スプライト」には、特定の要素のすべての視覚状態が次から次へと配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、同じスプライトイメージがCSSのすべての異なるステートに対して参照されます。 また、`background-position` プロパティは各状態に対して使用され、「スプライト」画像のどの部分を使用するかを指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 通常、ビューアは垂直方向に積み重ねられます。 以下は、上から同じズームインボタンをスタイル設定する「スプライト」ベースの例です。

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

次に、eCatalog Search Viewerに適用されるユーザーインターフェイス要素のリファレンスドキュメントを示します。

* [「お気に入りを追加」ボタン](r-html5-ecatsearch-customize-addfavorite.md)
* [閉じるボタン](r-html5-ecatsearch-customize-closebutton.md)
* [ダウンロード](r-html5-ecatsearch-customize-download.md)
* [メール共有](r-html5-ecatsearch-customize-emailshare.md)
* [共有を埋め込む](r-html5-ecatsearch-customize-embedshare.md)
* [Facebook共有](r-html5-ecatsearch-customize-facebookshare.md)
* [お気に入りエフェクト](r-html5-ecatsearch-customize-favoriteseffect.md)
* [お気に入りメニュー](r-html5-ecatsearch-customize-favoritesmenu.md)
* [お気に入りビュー](r-html5-ecatsearch-customize-favoritesview.md)
* [最初のページのボタン](r-html5-ecatsearch-customize-firstpagebutton.md)
* [フォーカスハイライト](r-html5-ecatsearch-customize-focushighlight.md)
* [フルスクリーンボタン](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [アイコンエフェクト](r-html5-ecatsearch-customize-iconeffect.md)
* [情報パネルのポップアップ](r-html5-ecatsearch-customize-infopanelpopup.md)
* [画像マップエフェクト](r-html5-ecatsearch-customize-imagemapeffect.md)
* [「次のページを大きく」ボタン](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [前のページを大きく表示ボタン](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [「最終ページ」ボタン](r-html5-ecatsearch-customize-lastpagebutton.md)
* [リンク共有](r-html5-ecatsearch-customize-linkshare.md)
* [メインコントロールバー](r-html5-ecatsearch-customize-maincontrolbar.md)
* [メインのビューアエリア](r-html5-ecatsearch-customize-mainviewerarea.md)
* [「次のページ」ボタン](r-html5-ecatsearch-customize-nextpagebutton.md)
* [ページインジケーター](r-html5-ecatsearch-customize-pageindicator.md)
* [ページビュー](r-html5-ecatsearch-customize-pageview.md)
* [前のページのボタン](r-html5-ecatsearch-customize-previouspagebutton.md)
* [印刷](r-html5-ecatsearch-customize-print.md)
* [「お気に入りを削除」ボタン](r-html5-ecatsearch-customize-removefavorite.md)
* [検索ボタン](r-html5-ecatsearch-customize-searchbutton.md)
* [検索効果](r-html5-ecatsearch-customize-searcheffect.md)
* [検索結果パネル](r-html5-ecatsearch-customize-searchresultspanel.md)
* [セカンダリコントロールバー](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [ソーシャル共有](r-html5-ecatsearch-customize-socialshare.md)
* [目次](r-html5-ecatsearch-customize-tableofcontents.md)
* [サムネール](r-html5-ecatsearch-customize-thumbnails.md)
* [「サムネール」ボタン](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [ツールヒント](r-html5-ecatsearch-customize-tooltips.md)
* [Twitter シェア](r-html5-ecatsearch-customize-twittershare.md)
* [「View All Favorites」ボタン](r-html5-ecatsearch-customize-viewallfavorites.md)
* [ズームインボタン](r-html5-ecatsearch-customize-zoominbutton.md)
* [ズームアウトボタン](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [ズームリセットボタン](r-html5-ecatsearch-customize-zoomresetbutton.md)

