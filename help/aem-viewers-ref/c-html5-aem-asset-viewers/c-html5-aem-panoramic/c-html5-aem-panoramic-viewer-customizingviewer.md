---
title: パノラマビューアのカスタマイズ
description: パノラマビューアの視覚的なカスタマイズや動作のカスタマイズはすべて、カスタム CSS を作成して行われます。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Video360 ビューアのカスタマイズ{#customizing-video-viewer}

すべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行われます。

推奨されるワークフローは、適切なビューアのデフォルトの CSS ファイルを取得し、別の場所にコピーしてカスタマイズし、カスタマイズしたファイルの場所を `style=` コマンドで指定することです。

デフォルトの CSS ファイルは、次の場所にあります。

`<s7viewers_root>/html5/PanoramicViewer.css`

カスタム CSS ファイルには、デフォルトのクラス宣言と同じクラス宣言を含める必要があります。 クラスの宣言を省略すると、ユーザーインターフェイス要素の組み込みの既定のスタイルが提供されないため、ビューアが正しく機能しません。

カスタム CSS ルールを提供するもう 1 つの方法は、web ページ上で直接埋め込みスタイルを使用するか、リンクされた外部 CSS ルールの 1 つで埋め込みスタイルを使用することです。

カスタム CSS を作成する場合は、ビューアがコンテナ DOM 要素 `.s7panoramicviewer` クラスを割り当てることに注意してください。 コマンドで渡された外部 CSS ファイルを使用してい `style=` 場合は、CSS ルールの descendant セレクターで `.s7panoramicviewer` クラスを親クラスとして使用します。 Web ページに埋め込みスタイルを適用する場合は、さらに、次のように、このセレクターをコンテナ DOM 要素の ID で修飾します。

`#<containerId>.s7panoramicviewer.`


## 一般的なスタイル設定のメモとアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS 内の外部アセットへのすべてのパスは、ビューアのHTML ページの場所ではなく、CSS の場所に対して解決されます。 デフォルトの CSS を別の場所にコピーする場合は、このことを考慮に入れます。場合によっては、デフォルトのアセットもコピーするか、カスタム CSS 内のパスを更新する必要があります。
* CSS でサポートされているカラー値には、様々な形式を使用できます。 透明度が必要な場合は、形式 `rgba(R,G,B,A)` 提案されます。 そうでない場合は、透明度は必要なく `#RRGGBB` 使用できます。

CSS を使用してビューア UI をカスタマイズする場合、ビューア要素のスタイル `!IMPORTANT` 設定するためにルールを使用することはできません。 特に、ビューア `!IMPORTANT` たはビューアSDKで提供されるデフォルトまたは実行時のスタイル設定を上書きする場合は、コンポーネントの適切な動作に影響を与える可能性があるので、このルールを使用しないでください。 代わりに、適切な特異性を持つ CSS セレクターを使用して、このリファレンスガイドに記載されている CSS プロパティを設定する必要があります。

## パノラマビューア CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**メインビューア領域**
メインビュー領域は、パノラマ画像が占める領域です。  通常、サイズが指定されていない場合は、デバイスの使用可能な画面に合わせて設定されます。

表示領域の外観は、CSS クラスセレクターで制御します。
`.s7panoramicviewer`

適用可能な CSS プロパティは次のとおりです。

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 幅 </span> </p> </td> 
   <td colname="col2"> <p> ビューアの幅を <span class="codeph"> します。</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高さ </span> </p> </td> 
   <td colname="col2"> <p> ビューアの高さを <span class="codeph"> します。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

例：
サイズ 1024 x 512 ピクセルのビューアを設定するには：

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**パノラマビュー**
メインビューはパノラマ画像で構成されています。

メインビューの外観は、CSS クラスセレクターで制御します。
`.s7panoramicviewer .s7panoramicview`

適用可能な CSS プロパティは次のとおりです。
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> の背景色の </span> </p> </td> 
   <td colname="col2"> <p> メインビューの背景色を <span class="codeph"> します。</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

例：
メイン ビューを透明にするには：

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
