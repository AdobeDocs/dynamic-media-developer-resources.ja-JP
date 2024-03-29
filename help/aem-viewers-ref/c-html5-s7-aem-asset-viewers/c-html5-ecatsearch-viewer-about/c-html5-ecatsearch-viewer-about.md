---
description: eCatalog 検索ビューアは、電子パンフレットを見開きまたはページごとに見開きまたはページごとに表示するカタログビューアです。 eCatalog を使用すると、ユーザーは、追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページでズームインして、詳細を確認することもできます。
keywords: レスポンシブ
solution: Experience Manager
title: eCatalog 検索
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2178'
ht-degree: 0%

---

# eCatalog 検索{#ecatalog-search}

eCatalog 検索ビューアは、電子パンフレットを見開きまたはページごとに見開きまたはページごとに表示するカタログビューアです。 eCatalog を使用すると、ユーザーは、追加のユーザーインターフェイス要素または専用のサムネールモードを使用してカタログ内を移動できます。 また、各ページでズームインして、詳細を確認することもできます。

このビューアは eCatalog で機能し、オプションの画像マップとソーシャル共有ツールをサポートします。 このツールには、ズームツール、カタログナビゲーションツール、フルスクリーンサポート、サムネールおよびオプションの閉じるボタンが含まれています。 また、ソーシャル共有ツール、印刷、ダウンロード、およびお気に入りもサポートしています。 デスクトップおよびモバイルデバイスで動作するように設計されています。

また、カタログコンテンツに対してキーワードベースまたはフレーズベースの検索を実行することもできます。

>[!NOTE]
>
>IR（画像レンダリング）または UGC（ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされません。

ビューアタイプ 513

詳しくは、 [必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## eCatalog ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

eCatalog 検索ビューアは、メインの JavaScript ファイルと、ビューアによって実行時にダウンロードされるヘルパーファイルのセット（この特定のビューアで使用されるすべての Viewer SDK コンポーネントを含む単一の JavaScript インクルード）です

IS-Viewers に付属する実稼動に対応したHTMLページまたは埋め込みモードで、ドキュメント化された API を使用して Target Web ページに統合される、ポップアップモードで eCatalog 検索ビューアを使用できます。

設定とスキニングは、他のビューアと同様です。 スキニングはすべて、カスタム CSS を使用して行います。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## eCatalog 検索ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

eCatalog 検索ビューアは、他のモバイルアプリケーションで一般的な以下のタッチジェスチャに対応しています。

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ジェスチャ </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>シングルタップ </p> </td> 
   <td colname="col2"> <p> スウォッチ内の新しいサムネールを選択します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p> 最大の拡大率に達するまで、1 レベルズームインします。 次のダブルタップジェスチャでは、ビューアが初期の表示状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>ズームインまたはズームアウトします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>スライドフレームの切り替えを使用している場合に、カタログページのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直方向のスワイプまたはフリック </p> </td> 
   <td colname="col2"> <p>画像がリセット状態の場合、ネイティブページスクロールを実行します。 </p> <p>サムネールがアクティブな場合、サムネールのリストをスクロールします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

カタログページ間を移動する際の、現実的なページフリップアニメーション効果を有効にすることができます。 その場合、ユーザーはページの隅を長押ししてドラッグし、ページをめくることができます。

このビューアは、タッチスクリーンとマウスを備えた Windows デバイスでも、タッチ入力とマウス入力の両方をサポートします。 ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーにのみ制限されます。

## eCatalog 検索ビューアを使用したソーシャルメディア共有ツール {#section-eb575084a99647c3a9591f439f40b412}

eCatalog 検索ビューアは、ソーシャル共有ツールをサポートしています。 これらは、ユーザーが共有ツールバーをクリックまたはタップしたときに共有ツールバーに展開する、メインコントロールバーのボタンとして使用できます。

共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプに関するアイコンが含まれています。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルサービスの標準の共有ダイアログにリダイレクトされます。 Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアの検索機能は、メインツールバーの見た目の良いガラスのアイコンとして使用できます。 このアイコンをクリックまたはタップすると、入力フィールドを含む検索パネルがアクティブになります。 キーワードまたは語句を入力して Enter キーを押すと、検索結果がパネルにレンダリングされ、メインビューで見つかった単語がハイライトされます。

## eCatalog 検索ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、このリンクを選択すると、ビューアが別のブラウザーウィンドウで開かれる場合があります。 ホスティングページの右側にビューアを埋め込む必要がある場合もあります。 後者の場合は、Web ページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込みの 3 つの主要な操作モードをサポートしています。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズが変更された場合や、モバイルデバイスの向きが変更された場合は調整されます。

ポップアップモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、 `window.open()` JavaScript 呼び出し（適切に設定） `A` HTML要素、またはその他の適切な方法。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 この場合、 [!DNL eCatalogSearchViewer.html] とは、 [!DNL html5/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

カスタム CSS を適用することで、視覚的なカスタマイズを実現できます。

次に、ビューアを新しいウィンドウでHTMLする開封コードの例を示します。

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 これは、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に応じて実行時にビューアのサイズを変更する可能性がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナのサイズ変更の方法によって、ビューアの動作が異なります `DIV`. Web ページでコンテナの幅のみが設定される場合 `DIV`で選択し、高さは無制限のままにし、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Bootstrap、Foundation などのレスポンシブレイアウトフレームワークを使用する Web ページで最も一般的です。

それ以外の場合は、Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域全体を占め、Web ページのレイアウトに従ってサイズが設定されます。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL eCatalogSearchViewer.js]. The [!DNL eCatalogSearchViewer.js] ファイルは、 [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

ビューアがDynamic MediaAdobeの 1 つにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobeDynamic Mediaサーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. コンテナ DIV を定義する。

   ビューアを表示するページに空の DIV 要素を追加します。 DIV 要素の ID は、後でビューア API に渡されるので、定義する必要があります。

   プレースホルダ DIV は配置された要素です。つまり、 `position` CSS プロパティがに設定されている `relative` または `absolute`.

   次に、定義済みのプレースホルダ DIV 要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、次のように宣言します `.s7ecatalogsearchviewer` トップレベルの CSS クラス ( 絶対単位で、または `stagesize` 修飾子

   サイズ調整は、HTMLページ、またはカスタムビューアの CSS ファイルに直接挿入し、その後、Dynamic Media Classicのビューアプリセットレコードに割り当てるか、style コマンドを使用して明示的に渡すことができます。

   詳しくは、 [eCatalog ビューアのカスタマイズ](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   次に、HTMLページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次の設定が可能です。 `stagesize` 修飾子をDynamic Media Classicのビューアプリセットレコードで指定するか、を使用してビューア初期化コードで明示的に渡します。 `params` コレクション、またはコマンドリファレンスの節で説明されている API 呼び出しとして、次のように使用できます。

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. ビューアを初期化します。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.eCatalogSearchViewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID とネストされたコンテナの名前が格納されるフィールド `params` ビューアでサポートされている設定パラメーターを持つ JSON オブジェクト。 この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティとして、最初のアセットを `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるために、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は、まだ Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 この場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次のように仮定します。 `eCatalogSearchViewer` はビューアインスタンスです。 `s7viewer` はプレースホルダーの名前です `DIV`; `https://s7d1.scene7.com/is/image/` は画像サービングの URL で、 `Viewers/Pluralist` はアセットです。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、固定サイズの eCatalog 検索ビューアを埋め込んだ簡単な Web ページの例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されています `DIV`. この例では、Web ページがビューアのコンテナを許可しているとします。 `DIV` を使用すると、web ブラウザーのウィンドウサイズの 40%を占め、高さは無制限のままになります。 生成される Web ページHTMLコードは次のようになります。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

このようなページへのビューアの追加方法は、固定サイズ埋め込みと似ていますが、唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナを追加 `DIV` 既存の「所有者」に対して `DIV`. 次のコードは完全な例です。 ブラウザーのサイズ変更時にビューアのサイズがどのように変化するか、およびビューアの縦横比がアセットとどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下のサンプルページでは、高さ無制限のレスポンシブデザイン埋め込みの、より実際に使用される使用例を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**幅と高さが定義されたフレキシブルサイズ埋め込み**

幅と高さが定義されたフレキシブルサイズ埋め込みの場合、Web ページのスタイル設定は異なります。 つまり、&quot;holder&quot;に両方のサイズを提供します。 `DIV` ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に変更：

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

残りの埋め込み手順は、高さ無制限のレスポンシブデザイン埋め込みと同じです。 結果の例は次のようになります。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API では、コンストラクターにパラメーターは不要で、設定パラメーターは `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、セッターベースの API を使用した固定サイズ埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
