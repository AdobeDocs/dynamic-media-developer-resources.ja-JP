---
title: パノラマビューアのカスタマイズ
description: パノラマビューアのすべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。
keywords: レスポンシブ
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Video360 ビューアのカスタマイズ{#customizing-video-viewer}

すべての視覚的なカスタマイズと、ほとんどの動作のカスタマイズは、カスタム CSS を作成することで行います。

推奨されるワークフローは、適切なビューアの初期設定の CSS ファイルを別の場所にコピーし、カスタマイズして、カスタマイズしたファイルの場所を `style=` コマンドを使用します。

初期設定の CSS ファイルは次の場所にあります。

`<s7viewers_root>/html5/PanoramicViewer.css`

カスタム CSS ファイルには、デフォルトの CSS ファイルと同じクラス宣言が含まれている必要があります。 クラス宣言を省略した場合、ビューアは正しく機能しません。ビューアには、ユーザインターフェイス要素の初期設定のスタイルが組み込まれていないからです。

カスタム CSS ルールを指定する別の方法は、Web ページ上またはリンクされた外部 CSS ルールの 1 つで、埋め込みスタイルを直接使用することです。

カスタム CSS を作成する場合、ビューアは `.s7panoramicviewer` クラスをコンテナの DOM 要素に追加します。 で渡された外部 CSS ファイルを使用する場合 `style=` コマンド、使用 `.s7panoramicviewer` クラスを親クラスとして、CSS ルールの子孫セレクターに含めます。 Web ページで埋め込みスタイルを使用している場合は、このセレクターを次のようにコンテナの DOM 要素の ID で修飾します。

`#<containerId>.s7panoramicviewer.`


## スタイルに関する一般的な注意事項とアドバイス {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS 内で指定されている外部アセットへのパスは、ビューアのパスページの場所ではなく、CSS の場所を基準にHTMLされます。 デフォルトの CSS を別の場所にコピーする場合は、次の点を考慮します。場合によっては、デフォルトのアセットもコピーするか、カスタム CSS 内でパスを更新する必要があります。
* カラー値には、CSS でサポートされている様々な形式を使用できます。 透明度が必要な場合は、 `rgba(R,G,B,A)` 形式が推奨されます。 それ以外の場合、透明度は不要です `#RRGGBB` を使用できます。

CSS でビューア UI をカスタマイズする場合は、 `!IMPORTANT` ルールは、ビューア要素のスタイル設定に対してサポートされていません。 特に `!IMPORTANT` ルールは、適切なコンポーネント動作に影響を与える可能性があるので、ビューアまたは Viewer SDK が提供するデフォルトのスタイル設定または実行時のスタイル設定を上書きする場合には使用しないでください。 代わりに、適切な特異性を持つ CSS セレクターを使用して、このリファレンスガイドで説明する CSS プロパティを設定する必要があります。

## パノラマビューア CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**メインビューア領域**
メインビュー領域は、パノラマ画像が表示される領域です。  通常、サイズが指定されていない場合は、使用可能なデバイス画面に収まるようにが設定されます。

表示領域の外観は、CSS クラスセレクターを使用して制御します。
`.s7panoramicviewer`

適用可能な CSS プロパティは次のとおりです。

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ビューアの幅 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 閲覧者の高さ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

例：サイズが 1024 x 512 ピクセルのビューアを設定するには、次のように記述します。

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**パノラマ表示**
メインビューは、パノラマ画像で構成されます。

メインビューの外観は、CSS クラスセレクターを使用して制御します。
`.s7panoramicviewer .s7panoramicview`

適用可能な CSS プロパティは次のとおりです。
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> メインビューの背景色 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

例：メインビューを透明にするには：

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
