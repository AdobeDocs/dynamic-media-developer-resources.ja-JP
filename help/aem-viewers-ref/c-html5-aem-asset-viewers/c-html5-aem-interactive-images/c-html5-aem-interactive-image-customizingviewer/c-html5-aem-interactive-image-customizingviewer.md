---
title: インタラクティブ画像ビューアのカスタマイズ
description: インタラクティブ画像ビューアのビジュアルのカスタマイズと動作のカスタマイズは、すべてカスタム CSSを作成して行います。
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: bb3cfe4a-ec60-4c10-82fe-9e4f8f7c586f
TQID: 'https://experienceleague.adobe.com/B63pgKihnG7F-AVm81OYRN828iHHDhw9XAFK5-LPWYg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1298
ht-degree: 0%

---

# インタラクティブ画像ビューアのカスタマイズ{#customizing-interactive-image-viewer}

インタラクティブ画像ビューアのビジュアルのカスタマイズと動作のカスタマイズは、すべてカスタム CSSを作成して行います。

推奨されるワークフローは、適切なビューアのデフォルトのCSS ファイルを取得し、別の場所にコピーしてカスタマイズし、`style=` コマンドでカスタマイズしたファイルの場所を指定することです。

デフォルトのCSS ファイルは次の場所にあります。

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言が含まれている必要があります。 クラス宣言を省略すると、ユーザーインターフェイス要素に組み込みのデフォルトスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供する別の方法として、埋め込みスタイルをweb ページ上またはリンクされた外部CSS ルールの1つで直接使用することもできます。

カスタム CSSを作成する場合、ビューアはコンテナ DOM要素に`.s7interactiveimage` クラスを割り当てることに注意してください。 `style=` コマンドで渡された外部CSS ファイルを使用している場合は、CSS ルールの子孫セレクターで`.s7interactiveimage` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを追加する場合は、このセレクターをコンテナ DOM要素のIDで次のように修飾します。

`#<containerId>.s7interactiveimage`

## レスポンシブデザインのCSSを作成する {#section-0bb49aca42d242d9b01879d5ba59d33b}

ユーザーのデバイスや特定のweb ページレイアウトに応じて、コンテンツの表示を異なるように、さまざまなデバイスやCSSへの埋め込みサイズをターゲットにすることができます。 このテクニックには、様々なレイアウト、ユーザーインターフェイス要素のサイズ、アートワークの解像度などが含まれますが、これらに限定されません。

ビューアは、レスポンシブデザインのCSSを作成する2つのメカニズム（CSS マーカーと標準のCSS メディアクエリ）をサポートしています。 これらのマーカーやクエリは、個別に使用することも、一緒に使用することもできます。

**CSS マーカー**

レスポンシブデザインのCSSの作成に役立つように、ビューアはCSS マーカーをサポートしています。 これらのマーカーは、トップレベルのビューアコンテナ要素に動的に割り当てられる特殊なCSS クラスです。 ランタイムビューアサイズと、現在のデバイスで使用されている入力タイプに基づいています。

CSS マーカーの最初のグループには、`.s7size_large`、`.s7size_medium`および`.s7size_small`個のクラスが含まれています。 ビューアコンテナのランタイム領域に基づいて適用されます。 例えば、ビューア領域が一般的なデスクトップモニターのサイズと同じかそれより大きい場合は、`.s7size_large`を使用します。 領域が共通のタブレットデバイスに近い場合は、`.s7size_medium`を割り当てます。 携帯電話の画面に類似した領域については、`.s7size_small`を使用してください。 これらのCSS マーカーの主な目的は、画面やビューアサイズごとに異なるユーザーインターフェイスレイアウトを作成することです。

CSS マーカーの2番目のグループに`.s7mouseinput`と`.s7touchinput`が含まれています。 現在のデバイスにタッチ入力がある場合は、CSS マーカー`.s7touchinput`が設定されます。 それ以外の場合は、`.s7mouseinput`が使用されます。 これらのマーカーは主に、通常タッチ入力には大きな要素が必要なため、異なる入力タイプに対して異なる画面サイズのユーザーインターフェイス入力要素を作成することを目的としています。

次のCSSの例では、マウス入力付きシステムではズームインボタンのサイズを28 x 28 ピクセルに、タッチ入力デバイスでは56 x 56 ピクセルに設定しています。 ビューアのサイズがさらに小さい場合は、20 x 20 ピクセルに設定されます。

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
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

多くのビューアーユーザーインターフェイス要素は、ビットマップアートワークを使用してスタイル設定され、複数の異なる視覚状態を持ちます。 良い例は、通常、少なくとも3つの異なる状態を持つボタンです：`up`、`over`、`down`。 各ステートには、割り当てられた独自のビットマップアートワークが必要です。

スタイル設定に対する従来のアプローチでは、CSSはユーザーインターフェイス要素の状態ごとに、サーバー上の個々の画像ファイルへの個別の参照を持ちます。 次に、ズームインボタンのスタイル設定に使用するCSSの例を示します。

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

このアプローチの欠点は、要素が初めて操作されたときに、エンドユーザーがちらついたり、ユーザーインターフェイスの応答が遅れたりすることです。 このアクションは、新しいエレメント状態の画像アートワークがまだダウンロードされていないために発生します。 また、このアプローチは、サーバーへのHTTP呼び出し数が増加するため、パフォーマンスにわずかな悪影響を及ぼす可能性があります。

CSS スプライトは、すべてのエレメント状態の画像アートワークを「スプライト」と呼ばれる1つのPNG ファイルに結合する別のアプローチです。 このような「スプライト」には、特定の要素のすべての視覚状態が次から次へと配置されます。 スプライトを使用してユーザーインターフェイス要素のスタイルを設定する場合、同じスプライトイメージがCSSのすべての異なるステートに対して参照されます。 また、`background-position` プロパティは各状態に対して使用され、「スプライト」画像のどの部分を使用するかを指定します。 「スプライト」画像は、任意の適切な方法で構成できます。 通常、ビューアは垂直方向に積み重ねられます。

以下は、先ほど同じズームインボタンをスタイル設定した「スプライト」ベースの例です。

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## 一般的なスタイリングノートとアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSSを使用してビューアのユーザーインターフェイスをカスタマイズする場合、`!IMPORTANT` ルールの使用はビューア要素のスタイル設定には対応していません。 特に、`!IMPORTANT` ルールは、ビューアまたはビューア SDKが提供するデフォルトまたはランタイムのスタイル設定を上書きするために使用しないでください。 その理由は、適切なコンポーネントの動作に影響を与える可能性があるためです。 代わりに、このビューアリファレンスガイドに記載されているCSS プロパティを設定するには、適切な特異性を持つCSS セレクターを使用する必要があります。
* CSS内の外部アセットへのすべてのパスは、ビューアのHTML ページの場所ではなく、CSSの場所に対して解決されます。 デフォルトのCSSを別の場所にコピーする場合は、このルールに注意してください。 デフォルトのアセットもコピーするか、カスタム CSS内のすべてのパスを更新します。
* ビットマップアートワークにはPNG形式が適しています。
* ビットマップアートワークは、`background-image` プロパティを使用してユーザーインターフェイス要素に割り当てられます。
* ユーザーインターフェイス要素の`width`および`height` プロパティが、その論理サイズを定義します。 `background-image`に渡されたビットマップのサイズは、その論理サイズに影響しません。
* Retinaのような高解像度の画面の高いピクセル密度を使用するには、ビットマップアートワークを論理ユーザーインターフェイス要素サイズの2倍のサイズで指定します。 次に、`-webkit-background-size:contain` プロパティを適用して、背景を論理ユーザーインターフェイス要素サイズまで縮小します。
* ユーザーインターフェイスからボタンを削除するには、そのCSS クラスに`display:none`を追加します。
* CSSがサポートするカラー値には、様々な形式を使用できます。 透明性が必要な場合は、形式`rgba(R,G,B,A)`を使用してください。 それ以外の場合は、形式`#RRGGBB`を使用できます。

## 共通のユーザーインターフェイス要素 {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

以下は、ビデオ画像ビューアに適用されるユーザーインターフェイス要素のリファレンスドキュメントです。
