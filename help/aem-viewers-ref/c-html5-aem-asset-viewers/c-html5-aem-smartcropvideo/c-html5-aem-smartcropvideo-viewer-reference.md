---
title: スマート切り抜きビデオビューア
description: スマート切り抜きビデオビューアは、スマート切り抜きサポートの追加により、H.264形式でエンコードされたストリーミングおよびプログレッシブビデオを再生します。 Dynamic Media機能を備えたDynamic Media ClassicまたはAdobe Experience Managerから配信されます。
keywords: responsive
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
TQID: 'https://experienceleague.adobe.com/GqkOR2872dgwk3CxxGctC3axCktGC0-iYkh8przgBjo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 2427
ht-degree: 0%

---

# スマート切り抜きビデオ{#smart-crop-video}

スマート切り抜きビデオビューアは、スマート切り抜きサポートの追加により、H.264形式でエンコードされたストリーミングおよびプログレッシブビデオを再生します。 Dynamic Media機能を備えたDynamic Media ClassicまたはExperience Managerから配信されます。

[必要システム構成と前提条件](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842)を参照してください。

シングルビデオとアダプティブビデオセットの両方がサポートされています。 また、ビューアは、外部の場所でホストされているプログレッシブビデオストリームとHLS ストリームの操作をサポートしています。 HTML5 ビデオをサポートするデスクトップとモバイルの両方のWeb ブラウザーで動作するように設計されています。 このビューアは、ビデオコンテンツ、ビデオチャプターのナビゲーション、ソーシャルメディア共有ツールの上に表示されるオプションのクローズドキャプションもサポートしています。

スマート切り抜きビデオビューアは、基になるシステムがサポートしている場合は常に、デフォルト設定でHLS形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

ビューアータイプ 518。


## デモ URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)


## スマート切り抜きビデオビューアの使用 {#section-f21ac23d3f6449ad9765588d69584772}

スマート切り抜きビデオビューアは、メインのJavaScript ファイルと一連のヘルパーファイルを表します。1つのJavaScriptには、この特定のビューアで使用されるすべてのビューア SDK コンポーネント、アセット、および実行時にビューアがダウンロードしたCSSが含まれます。

IS-Viewersに付属の実稼動対応のHTML ページを使用して、スマート切り抜きビデオビューアをポップアップモードで使用できます。 または、ドキュメント化されたAPIを使用してターゲット web ページに統合する埋め込みモードでビューアを使用することもできます。

ビューアの設定とスキン処理の作業は、他のビューアと同様です。 すべてのスキニングは、カスタム CSSを使用して実行できます。

すべてのビューアに共通する[&#x200B; コマンド参照 – 構成属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通するコマンド参照 – URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください

## スマート切り抜きビデオビューアの操作 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

スマート切り抜きビデオビューアは、ビデオの再生に対して次のような一連の標準ユーザーインターフェイスコントロールを提供します。

* 「再生/一時停止」ボタン。
* ビデオスクラムビデオタイムバブル。
* 再生時間/合計時間インジケーター。
* ボリュームコントロール：
* フルスクリーンボタン：
* クローズドキャプションの切り替え。

これらのコントロールはすべて、ビューアユーザーインターフェイスの下部にあるコントロールバーにグループ化されます。

タッチデバイスでは、ボリュームコントロールはハードウェアボタンを使用してボリュームを制御することしかできないため、ユーザーインターフェイスから非表示になります。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでは全画面ボタンを使用できません。

ビデオチャプターがアクティブ化されると、ビデオのコンテンツを素早くナビゲートできます。 ビデオチャプターは、ビデオスクラブラートラックにマーカーとして表示され、マウスロールオーバーまたはタッチシステムをタップするだけで、チャプターのタイトルと関連する説明が表示されます。 ユーザーは、章マーカーを選択するか、章説明バブルを選択することで、特定の章を検索できます。

ビューアは、タッチスクリーンとマウスを備えたWindows デバイスでのタッチ入力とマウス入力の両方をサポートしています。 ただし、このサポートは、Chrome、Internet Explorer 11、およびEdgeのweb ブラウザーのみに限定されます。

このビューアにはキーボードから完全にアクセス可能です。

[&#x200B; キーボードのアクセシビリティとナビゲーション &#x200B;](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)を参照してください。

## スマート切り抜きビデオビューアを備えたソーシャルメディア共有ツール {#section-907d316fe1da4b87abb9775f02464704}

スマート切り抜きビデオビューアは、ソーシャルメディア共有ツールをサポートしています。 ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーが共有ツールバーをクリックまたはタップすると、共有ツールバーに展開されます。

共有ツールバーには、Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など、サポートされている共有チャネルのタイプごとにアイコンが含まれています。 メール共有、埋め込み共有またはリンク共有ツールがアクティブ化されると、対応するデータ入力フォームを含むモーダルダイアログボックスがビューアに表示されます。 FacebookまたはTwitterが呼び出されると、ビューアはソーシャルメディアサービスから標準の共有ダイアログボックスにユーザーをリダイレクトします。 また、共有ツールが有効になっている場合、ビデオの再生は自動的に一時停止されます。

Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは利用できません。

## スマート切り抜きビデオビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

web ページごとに、閲覧者の行動に対するニーズは異なります。 Web ページでリンクが提供される場合があります。このリンクを選択すると、別のブラウザーウィンドウでビューアが開きます。 それ以外の場合は、ホスティングページに直接ビューアを埋め込む必要があります。 後者の場合、web ページは静的なページレイアウトを使用するか、異なるデバイスまたは異なるブラウザーウィンドウのサイズに対して異なる表示を行うレスポンシブデザインを使用します。 これらのニーズに対応するために、ビューアでは、ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込みという3つの主要な操作モードをサポートしています。

同じページに複数のビデオを埋め込むことは、タブレットおよびモバイルデバイスでサポートされています。 通常、一度に再生できるビデオは1つだけです。 ユーザーが1つのビデオの再生を開始してから別のビデオの再生を試みると、最初のビデオは自動的に一時停止します。 自動一時停止されたビデオは現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 このルールの唯一の例外は、ビデオを並行して再生できるAndroid™ 4.x デバイスのChrome ブラウザーです。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別のweb ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズ変更やデバイスの向きの変更に応じて調整します。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、`window.open()` JavaScript呼び出し、`A` HTML要素の適切な設定、またはその他の適切なメソッドを使用してビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 [!DNL SmartCropVideoViewer.html]と呼ばれ、標準のIS-Viewers デプロイメントの[!DNL html5/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

カスタム CSSを適用すると、視覚的なカスタマイズを実現できます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブ埋め込みモードについて**

埋め込みモードでは、ビューアが既存のweb ページに追加されます。このweb ページには、ビューアに関連しない顧客コンテンツが既に含まれている可能性があります。 通常、閲覧者はweb ページの不動産の一部しか占めていません。

主なユースケースは、デスクトップ PCやタブレットデバイス向けのweb ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

初期読み込み後にビューアのサイズが変更されない場合は、固定サイズ埋め込みが使用されます。 このオプションは、静的ページレイアウトを持つweb ページに最適です。

レスポンシブデザインの埋め込みは、コンテナ `DIV`のサイズ変更に応じて、ビューアを実行時にサイズ変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟性の高いページレイアウトを使用するweb ページにビューアを追加することです。

レスポンシブデザイン埋め込みモードでは、web ページのサイズとコンテナ `DIV`のサイズによって、ビューアの動作が異なります。 Web ページがコンテナ `DIV`の幅のみを設定し、高さを制限しない場合、ビューアは使用されるアセットの縦横比に応じて自動的に高さを選択します。 この方法により、側面にパディングすることなく、アセットをビューに完全に収めることができます。 このユースケースは、BootstrapやFoundationなどのレスポンシブデザインレイアウトフレームワークを使用するweb ページで最も一般的です。

それ以外の場合、web ページがビューアのコンテナ `DIV`の幅と高さの両方を設定すると、ビューアはその領域だけを塗りつぶし、web ページレイアウトで提供されるサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込むことです。このオーバーレイは、web ブラウザーウィンドウのサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

次の操作を実行して、ビューアをweb ページに追加します。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ `DIV`を定義しています。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. ビューアのJavaScript ファイルをweb ページに追加します。

   ビューアを作成するには、HTML ヘッドにスクリプトタグを追加する必要があります。 ビューアーAPIを使用する前に、[!DNL SmartCropVideoViewer.js]を含めることを確認してください。 [!DNL SmartCropVideoViewer.js] ファイルは、標準のIS-Viewers デプロイメントの[!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

ビューアがAdobe Dynamic Media Classic サーバーのいずれかにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-ViewersがインストールされているAdobe Dynamic Media Classic サーバーの1つにフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメイン ビューア JavaScript `include` ファイルのみを参照してください。 実行時にビューアのロジックによってダウンロードされる可能性があるweb ページコード内の他のJavaScript ファイルを参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 その理由は、`Utils.js`または類似のランタイムビューアーライブラリの場所が、ビューアーのロジックによって完全に管理され、ビューアーリリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes`をサーバー上に保持しません。
>
>
>その結果、ビューアがページ上で使用するセカンダリ JavaScript `include`を直接参照すると、新しい製品バージョンがデプロイされる際に、将来的にビューア機能が破損します。

1. コンテナ DIVの定義。

   ビューアを表示するページに、空のDIV エレメントを追加します。 このIDは後でビューア APIに渡されるので、DIV要素にはIDが定義されている必要があります。 DIVのサイズはCSSで指定します。

   プレースホルダーDIVは配置された要素です。`position` CSS プロパティが`relative`または`absolute`に設定されていることを意味します。

   Internet Explorerでフルスクリーン機能が正しく機能することを確認します。 プレースホルダーDIVよりも高い重ね順を持つ要素がDOMにないことを確認します。

   次に、定義済みのプレースホルダーDIV要素の例を示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、`.s7videoviewer` トップレベル CSS クラスを絶対単位で宣言するか、修飾子`stagesize`を使用することで設定できます。

   HTML ページのCSSまたはカスタムビューア CSS ファイルにサイズを設定できます。 その後、Dynamic Media Classicのビューアプリセットレコードに割り当てられるか、スタイルコマンドを使用して明示的に渡されます。

   CSSを使用したビューアのスタイル設定について詳しくは、[&#x200B; スマート切り抜きビデオビューアのカスタマイズ &#x200B;](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e)を参照してください。

   次に、HTML ページで静的ビューアサイズを定義する例を示します。

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Dynamic Media Classicのビューアプリセットレコードで`stagesize`修飾子を設定するか、`params` コレクションを使用してビューアの初期化コードで明示的に渡すことができます。 または、コマンドリファレンスセクションで説明されているように、次のようにAPI呼び出しとして使用します。

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアの作成と初期化。

   上記の手順を完了したら、`s7viewers.SmartCropVideoViewer` クラスのインスタンスを作成し、すべての構成情報をそのコンストラクターに渡し、ビューアーインスタンスで`init()` メソッドを呼び出します。 構成情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには、ビューアコンテナ IDの名前を保持する`containerId` フィールドと、ビューアでサポートされている設定パラメーターを含むネストされた`params` JSON オブジェクトが必要です。 この場合、`params` オブジェクトには、少なくとも`serverUrl` プロパティとして渡された画像サービング URL、`videoserverurl` プロパティとして渡されたビデオサーバーURL、および最初のアセットを`asset` パラメーターとして含める必要があります。 JSON ベースの初期化APIを使用すると、1行のコードでビューアを作成して開始できます。

   ビューアコードがIDでコンテナ要素を見つけられるように、ビューアコンテナをDOMに追加することが重要です。 一部のブラウザーは、Web ページの最後までDOMの構築を遅らせます。 互換性を最大限に高めるには、終了`BODY` タグの直前または本文`onload()` イベントで`init()` メソッドを呼び出します。

   同時に、コンテナ要素は必ずしもweb ページレイアウトの一部であってはなりません。 例えば、割り当てられた`display:none` スタイルを使用して非表示にすることができます。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで初期化プロセスを遅らせます。 このアクションが発生すると、ビューアの読み込みが自動的に再開されます。

   次に、ビューアーインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡し、`init()` メソッドを呼び出す例を示します。 この例では、`smartCropVideoViewer`がビューアーインスタンスで、`s7viewer`がプレースホルダー`DIV`の名前、[!DNL http://s7d1.scene7.com/is/image/]が画像サービス URL、[!DNL http://s7d1.scene7.com/is/content/]がビデオサーバーURL、[!DNL html5automation/frisbee-AVS]がアセットであると仮定します。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   次のコードは、スマート切り抜きビデオビューアを固定サイズで埋め込む面倒なweb ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**高さの制限のないレスポンシブデザイン埋め込み**

レスポンシブデザインの埋め込みにより、web ページには通常、ビューアのコンテナ `DIV`の実行時サイズを決定する、ある種の柔軟なレイアウトが配置されています。 この例では、web ページでビューアのコンテナ `DIV`がweb ブラウザーのウィンドウ サイズの40%を使用でき、高さは制限されないと仮定します。 Web ページのHTML コードは次のようになります。

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

このようなページへのビューアの追加は、固定サイズの埋め込みと似ています。唯一の違いは、ビューアサイズを明示的に定義する必要がないことです。

1. ビューアのJavaScript ファイルをweb ページに追加します。
1. コンテナ DIVの定義。
1. ビューアの作成と初期化。

上記のすべての手順は、固定サイズの埋め込みと同じです。 コンテナ `DIV`を既存の「ホルダー」 `DIV`に追加します。 次のコードは、完全な例です。 ブラウザーのサイズを変更するとビューアサイズがどのように変化するか、およびビューアの縦横比がアセットとどのように一致するかを確認できます。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

次のサンプルページでは、高さの制限のないレスポンシブデザイン埋め込みをより実際に使用する方法を示します。

[ライブデモ](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=ja)

-->

**幅と高さが定義されたレスポンシブデザイン埋め込み**

幅と高さが定義されたレスポンシブデザインの埋め込みがある場合、web ページのスタイルは異なります。「ホルダー」 `DIV`に両方のサイズを提供し、ブラウザーウィンドウに中央に配置します。 また、web ページでは、`HTML`要素と`BODY`要素のサイズを100%に設定しています。

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

残りの埋め込み手順は、高さの制限のないレスポンシブデザイン埋め込みと同じです。 結果として得られる例は次のとおりです。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Setter ベースのAPIを使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースのAPIとno-args コンストラクターを使用できます。 このAPIでは、コンストラクターはパラメーターを受け取らず、設定パラメーターは`setContainerId()`、`setParam()`、および`setAsset()`のAPI メソッドを使用して指定され、別々のJavaScript呼び出しが行われます。

次の例は、セッターベースのAPIを使用した固定サイズの埋め込みを示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
