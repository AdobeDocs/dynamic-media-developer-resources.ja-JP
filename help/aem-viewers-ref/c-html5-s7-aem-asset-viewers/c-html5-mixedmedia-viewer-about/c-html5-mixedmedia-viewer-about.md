---
title: 混在メディア
description: 混在メディアビューアは、メディアビューアです。 画像、見本セット、スピンセット、ビデオおよびアダプティブビデオセットを含むメディアセットをサポートします。
keywords: 応答
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2581'
ht-degree: 0%

---

# 混在メディア{#mixed-media}

混在メディアビューアは、メディアビューアです。 画像、見本セット、スピンセット、ビデオおよびアダプティブビデオセットを含むメディアセットをサポートします。

ビューアの下部にあるサムネールは、各メディアセット要素とそのアセットタイプインジケーターを表します。 スウォッチセット要素が選択されている場合は、スウォッチの 2 行目が表示され、スウォッチセット内のカラーバリエーションを選択できます。 画像およびスウォッチセット要素は、連続モードまたはインラインモードでのズームに対応しており、スピンセットは、ズームとスピンの両方に対応しています。 ビデオおよびアダプティブビデオセットは、すべての基本的な再生コントロールをサポートします（オプションのクローズドキャプションがビデオコンテンツの上に表示されている場合）。 ユーザーは全画面表示ボタンをクリックすることで、いつでも全画面表示に切り替えることができます。 ビューアにはオプションで「閉じる」ボタンがあります。 デスクトップおよびモバイルデバイスで動作するように設計されています。

混在メディアビューアは、基になるシステムでサポートされている場合は常に、デフォルト設定でHLS形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

>[!NOTE]
>
>IR （画像レンダリング）または UGC （ユーザー生成コンテンツ）を使用する画像は、このビューアではサポートされていません。

ビューアのタイプは 505 です。

[ システム要件と前提条件 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## 混在メディアビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

混在メディアビューアは、実行時にビューアによってダウンロードされるメインのJavaScript ファイルと一連のヘルパーファイル（この特定のビューア、アセット、CSS で使用されるすべてのビューア SDK コンポーネントに含まれる 1 つのJavaScript インクルード）を表します。

IS-Viewers に付属の実稼動用HTML ページを使用して、混在メディアビューアをポップアップモードで使用できます。 または、埋め込みモードでビューアを使用し、ドキュメントに記載されている API を使用してターゲット web ページに統合することもできます。

ビューアの設定とスキニングのタスクは、他のビューアと似ています。 すべてのスキニングは、カスタム CSS を使用して行います。

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

## 混在メディアビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

混在メディアビューアでは、他のモバイルアプリケーションに共通するシングルタッチジェスチャとマルチタッチジェスチャをサポートしています。 ビューアがユーザーのスワイプジェスチャーを処理できない場合は、イベントを web ブラウザーに転送して、ネイティブページのスクロールを実行します。 この機能により、ビューアがデバイスの画面領域のほとんどを占めている場合でも、ユーザーはページ内を移動できます。

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
   <td colname="col2"> <p> フライアウト ビューをアクティブにするか、メイン ズーム レベルとサブ ズーム レベルの間を変更します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ダブルタップ </p> </td> 
   <td colname="col2"> <p>連続 <span class="codeph"> ズームモード </span> は、ズームが 1 レベルだけ拡大され、最大倍率に達すると、次のダブルタップジェスチャーが初期状態にリセットされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>タッチ＆ホールド </p> </td> 
   <td colname="col2"> <p> インラインの <span class="codeph"> ズームモード </span> いる場合、はズームされた画像をアクティブにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ピンチ </p> </td> 
   <td colname="col2"> <p>連続ズームモードでは、画像がズームインまたはズームアウトされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>水平スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 現在のアセットがスピンセットで、画像がリセット状態の場合は、スピンセットを水平方向にスピンします。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像がズームインされると、画像は水平方向に移動します。 画像がビューの端に移動されても、その方向にスワイプが行われる場合、ジェスチャーはネイティブページのスクロールを実行します。 </p> <p> スウォッチバーのスウォッチのリストをスクロールします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>垂直スワイプまたはフリック </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態の場合、多次元スピンセットを使用すると垂直視野角が変更されます。 1 次元スピンセットの場合、または多次元スピンセットが最後の軸または最初の軸にあるときに、垂直スワイプによって垂直ビューの角度が変更されないようにする場合、ジェスチャはネイティブページスクロールを実行します。 </p> <p> 現在のアセットがスピンセットまたは画像で、画像がズームインされると、画像が垂直方向に移動します。 画像がビューの端に移動されても、その方向にスワイプが行われる場合、ジェスチャーはネイティブページのスクロールを実行します。 </p> <p> スウォッチ領域内でジェスチャーを行うと、ネイティブページのスクロールが実行されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

また、このビューアは、タッチスクリーンとマウスを備えた Windows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されます。

このビューアは完全にキーボードでアクセス可能です。

詳しくは [ キーボードアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## 混在メディアビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 選択するとビューアが別のブラウザーウィンドウで開くリンクが、web ページに表示される場合があります。 それ以外の場合は、ホスティングページにビューアを直接埋め込む必要があります。 後者の場合、web ページが静的なページレイアウトになっている可能性や、異なるデバイスや異なるブラウザーウィンドウサイズに異なる表示を行うレスポンシブデザインが使用されている可能性があります。 これらのニーズに対応するために、ビューアでは 3 つの主要な操作モード（ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込み）をサポートしています。

## ポップアップモードについて {#section-77d5aa03b8b94566958a179b1a2cd474}

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのサイズが変更された場合や、モバイルデバイスの向きが変更された場合に、ブラウザーウィンドウ領域全体を使用して調整が行われます。

ポップアップモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切なメソッド `A` 使用して、ビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 この場合、[!DNL MixedMediaViewer.html] という名前で、標準の IS-Viewers デプロイメントの [!DNL html5/] サブフォルダー内に配置されます。

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

カスタム CSS を適用すると、視覚的にカスタマイズできます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## 固定サイズおよびレスポンシブデザインの埋め込みについて {#section-ec86b100ba5943d0b16694268520bbde}

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの不動産の一部のみを占有します。

主なユースケースは、デスクトップやタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブデザインページです。

固定サイズの埋め込みは、初回読み込み後にビューアのサイズが変更されない場合に使用されます。 このアクションは、静的なレイアウトの web ページに最適です。

レスポンシブデザインの埋め込みは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

レスポンシブデザインの埋め込みモードでは、web ページのコンテナコンポー `DIV` ントのサイズがどのように調整されるかに応じて、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、アセットが側面にパディングを入れずに、ビューに完全に収まります。 このユースケースは、Bootstrapや Foundation などのレスポンシブデザインレイアウトフレームワークを使用する web ページで最も一般的です。

そうでない場合、web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されていると、ビューアはその領域だけを埋め、web ページレイアウトが提供するサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

## 固定サイズの埋め込み {#section-17d162f76ffa4804b27928f51e7bea1d}

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLのヘッドにスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL MixedMediaViewer.js] を含めてください。 [!DNL MixedMediaViewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリを、コンテキストパス（いわゆる統合SDK `/s7viewers`）から直接参照 `include` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes` をサーバーに保持しません。
>
>
>その結果、ビューアが使用するセカンダリ JavaScript `include` ージをページ上で直接参照すると、今後、新しい製品バージョンがデプロイされた際に、ビューアの機能が損なわれます。

1. コンテナ DIV の定義。

   ビューアを表示するページに、空の DIV 要素を追加します。 DIV 要素には ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるためです。 DIV のサイズは CSS で指定します。

   プレースホルダー DIV が配置済み要素です（つまり、`position` CSS プロパティが `relative` または `absolute` に設定されています）。

   Internet Explorer で全画面表示モードが正しく機能することを確認します。 プレースホルダー DIV よりも重ね順が大きい要素が DOM に他にないことを確認します。

   定義されたプレースホルダー DIV 要素の例を以下に示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. ビューアサイズの設定

   このビューアには、複数項目セットを扱う際のサムネールが表示されます。 デスクトップ システムでは、サムネイルはメイン ビューの下に配置されます。 同時に、ビューアでは API を使用して、実行時にメインアセットを入れ替え `setAsset()` ことができます。 開発者は、新しいアセットに項目が 1 つしかない場合に、ビューアが下部のサムネール領域をどのように管理するかを制御できます。 外側のビューアのサイズはそのままにして、メインビューの高さを上げてサムネール領域を占有することができます。 または、メインビューのサイズを静的に保ち、外側のビューア領域を折りたたんで、web ページのコンテンツを上に移動することもできます。 次に、サムネールから残っている無料ページの不動産を使用します。

   外部ビューアの境界をそのままにするには、最上位の CSS クラス `.s7mixedmediaviewer` サイズを絶対単位で定義します。 CSS でのサイズ設定は、HTML ページまたはカスタムビューア CSS ファイルに直接配置し、後でDynamic Media Classicのビューアプリセットレコードに割り当てたり、style コマンドを使用して明示的に渡したりできます。

   CSS を使用したビューアのスタイル設定について詳しくは、[ 混在メディアビューアのカスタマイズ ](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) を参照してください。

   HTML ページで静的な外部ビューアのサイズを定義する例を次に示します。

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のサンプルページでは、固定の外部ビューア領域での動作を確認できます。 セットを切り替えても、外側のビューアのサイズは変わりません。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   メインビューの寸法を静的にするには、CSS セレクターまたは修飾子を使用して、内部の `Container` SDK コンポーネントのビューアサイズ `.s7mixedmediaviewer .s7container` 絶対単位で定義 `stagesize` ます。

   次に、アセットを切り替えるときにメイン表示領域のサイズが変わらないように、内部の `Container` SDK コンポーネントのビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   次のサンプルページは、固定のメインビューサイズを使用したビューアの動作を示しています。 セットを切り替えると、メインビューは静的なままになり、web ページコンテンツは垂直方向に移動します。

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   `stagesize` 修飾子は、Dynamic Media Classicのビューアプリセットレコードで設定するか、コレクションを使用してビューア初期化コードで明示的に渡 `params` ことができます。 または、このヘルプのコマンドリファレンスの節で説明されているように、API 呼び出しとして、次のように指定します。

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   この例では、CSS ベースのアプローチをお勧めします。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.MixedMediaViewer` そのコンストラクターに渡して、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前を保持する `containerId` フィールドと、ビューアがサポートす `params` 設定パラメーターを含むネストされた JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも、プロパティとして画像サービング URL が渡され、プロパティとしてビデオサーバー URL が渡され、`serverUrl` パラメーターとして初期アセットが渡され `videoserverurl` 必要 `asset` あります。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `init()` タグの直前または body `BODY` イベントで `onload()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   以下に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、`mixedMediaViewer` はビューアインスタンス、`s7viewer` はプレースホルダー `DIV` の名前、[!DNL http://s7d1.scene7.com/is/image/] は画像サービング URL、[!DNL http://s7d1.scene7.com/is/content/] はビデオサーバーの URL、[!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] はアセットであると想定しています。

```html {.line-numbers}
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

次のコードは、混在メディアビューアを固定サイズで埋め込む単純な web ページの完全な例です。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## 高さが制限されないレスポンシブ埋め込み {#section-056cb574713c4d07be6d07cf3c598839}

レスポンシブデザインの埋め込みを使用すると、通常、web ページには、ビューアのコンテナ `DIV` ージの実行時サイズを指定する何らかの柔軟なレイアウトが配置されます。 次の例では、web ページで、ビューアのコンテナ `DIV` が web ブラウザーのウィンドウサイズの 40% を占め、高さは無制限であるとします。 Web ページのHTML コードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズの埋め込みを行う手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ DIV の定義。
1. ビューアの作成と初期化。

上記の手順はすべて、固定サイズの埋め込みと同じです。 コンテナ DIV を既存の `"holder"` DIV に追加します。 次のコードは完全な例です。 ブラウザーのサイズを変更するとビューアのサイズがどのように変化するか、ビューアの縦横比がアセットとどのように一致するかを確認します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

以下の例では、高さが制限されないレスポンシブデザインの埋め込みを使用した実際の使用例を示しています。

[ ライブデモ ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[ 代替デモの場所 ](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## 幅と高さが定義された柔軟なサイズ埋め込み {#section-0a329016f9414d199039776645c693de}

幅と高さが定義されたフレキシブルサイズの埋め込みがある場合、web ページのスタイル設定は異なります。 `"holder"` DIV のサイズとブラウザーウィンドウの中央に配置されるサイズの両方が指定されます。 また、web ページでは、`HTML` と `BODY` 要素のサイズが 100% に設定されます。

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

残りの埋め込み手順は、高さが制限されないレスポンシブデザインの埋め込みに使用される手順と同じです。 結果の例を次に示します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## セッターベースの API を使用した埋め込み {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API コンストラクターを使用すると、パラメーターは取得されず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、別個のJavaScript呼び出しで設定パラメーターが指定されます。

次の例は、setter ベースの API を使用した固定サイズの埋め込みの使用を示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```
