---
title: Video360
description: HTML5 Video360 Viewer は、H.264 形式でエンコードされたストリーミングおよびプログレッシブ 360 ビデオを再生する 360 度ビデオプレーヤーで、Dynamic Media ClassicまたはAdobe Experience Manager（Dynamic Media）から配信されます。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2561'
ht-degree: 0%

---

# Video360{#video}

HTML5 Video360 Viewer は、H.264 形式でエンコードされたストリーミングおよびプログレッシブ 360 ビデオを再生する 360 度ビデオプレーヤーで、Dynamic Media ClassicまたはAdobe Experience Manager（Dynamic Media）から配信されます。

360 ビデオ（没入型ビデオまたは球形ビデオとも呼ばれます）は、全方向のビューが同時に記録されるビデオ録画で、全方向のカメラまたはカメラのコレクションを使用して撮影されます。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、このビューアは、外部の場所でホストされているプログレッシブビデオおよびHLS ストリームの操作もサポートしています。

360 ビデオの推奨アスペクト比は 2:1 です。 空間サウンドはサポートされていません。 ビューアは 360 ビデオでのみ動作するように設計されています。360 以外のビデオを再生しようとすると、ビデオが歪んで再生されます。

ビューアは、HTML5 ビデオをサポートするデスクトップとモバイルの両方の web ブラウザーで動作するように設計されています。 ビューアは、オプションのソーシャル共有ツールをサポートしています。

Video360 ビューアは、基になるシステムでサポートされている場合は常に、デフォルト設定でHLS形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

ビューアのタイプは 517 です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[ 必要システム構成 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## Video360 ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 ビューアは、実行時にビューアによってダウンロードされた主なJavaScript ファイルと一連のヘルパーファイル（このビューアで使用されるすべてのHTML5 ビューア SDK コンポーネント、アセット、CSS と共に 1 つのJavaScriptに含まれます）を表します。

HTML5 Video360 ビューアは、IS-Viewers に付属の実稼動用HTML ページを使用したポップアップモードと、ドキュメント化された API を使用して Target Web ページに統合する埋め込みモードの両方で使用できます。

設定とスキニングは、このガイドで説明する他のビューアの設定と似ています。 すべてのスキニングは、カスタム（CSS）カスケーディングスタイルシート（CSS）を使用して行います。

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください

360 ビデオコンテンツには、標準の非 360 ビデオよりも高いエンコーディング設定が必要です。 つまり、同じ知覚可能な品質を達成するには、360 コンテンツが非 360 ビデオよりも高解像度である必要があります。 360 ビデオについては、次のアダプティブビデオプリセット設定を検討することをお勧めします。

* 720p、2500 kbps
* 1080p、5000 kbps
* 1440p、6600 kbps

ただし、このような高品質の設定でエンコードされたビデオを提供するには、エンドユーザーのデバイスで高帯域幅接続が必要になることに注意してください。

## Video360 ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 ビューアには、再生/一時停止ボタン、ビデオスクラバーのビデオのタイムバブル、再生時間/合計時間インジケーター、ボリュームコントロール、フルスクリーンボタンなど、ビデオ再生用の一連の標準ユーザーインターフェイスコントロールが用意されています。 これらのコントロールはすべて、ビューアのユーザーインターフェイスの下部にあるコントロールバーにグループ化されます。

タッチデバイスでは、デバイスのハードウェアボタンを使用してのみ音量を制御できるため、音量コントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作する場合、ユーザーインターフェイスで全画面表示ボタンを使用できません。

また、ビューアは、様々なソーシャルメディア共有ツールもサポートしています。 ユーザーインターフェイスでは 1 つのボタンとして使用でき、ユーザーがクリックまたはタップすると、共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、メール共有、埋め込みコード共有、リンク共有など、サポートされている共有チャネルのタイプごとのアイコンが含まれています。 メール共有、埋め込み共有、リンク共有の各ツールがアクティベートされると、ビューアは対応するデータ入力フォームを含むモーダルダイアログボックスを表示します。 Facebook または Twitter が呼び出されると、ビューアはソーシャルメディアサービスから標準の共有ダイアログボックスにユーザーをリダイレクトします。 また、共有ツールがアクティブになると、ビデオの再生は自動的に一時停止します。 Web ブラウザーのセキュリティ制限により、共有ツールは全画面表示モードでは使用できません。

ビューアでは、次の場所での 360 ビデオ再生がサポートされています。

* VR ヘッドセット（Oculus Go やOculus Riftなど）
* VR HMD （ヘッドマウントディスプレイ）マウント（Googleボール紙など）
* VR 非対応デバイス（デスクトップブラウザー、タブレット、携帯電話が VR HMD マウントに接続されていない場合など）

VR ヘッドセットで 360 ビデオコンテンツを表示するために、追加の設定は必要ありません。 視聴者は VR ヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンをオンにすると、ビデオのレンダリングが VR モードに切り替わります。 ビューアでの VR レンダリングは、WebVR をサポートしているブラウザーでのみサポートされています。

VR HMD マウントを使用するには、ビューアの設定で `Video360Player.vrrender` 修飾子を `1` に設定する必要があります。これにより、立体視レンダリングが強制されます。

VR ヘッドセットや VR HMD マウントでは、VR モードでは他の再生制御が提供されるのではなく、ヘッドセットの動きに応じて視点が変化します。

非 VR 対応デバイスで 360 ビデオを視聴する場合、エンドユーザーはマウス、タッチ、キーボードを使用して、ビデオの再生と視点を制御できます。

ビューアは、タッチスクリーンとマウスを使用した Windows デバイスでは、タッチ入力とマウス入力の両方をサポートしていますが、このサポートは、Chrome、Internet Explorer 11、Edgeの web ブラウザーのみに制限されています。

ビューアは完全にキーボードでアクセス可能です。 詳しくは [ キーボードアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## Video360 ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

Web ページによって、ビューアの動作に対するニーズは異なります。 選択すると別のブラウザーウィンドウでビューアが開くリンクが、web ページに表示される場合があります。 それ以外の場合は、ホスティングページにビューアを直接埋め込む必要があります。 後者の場合、web ページが静的なページレイアウトになっている可能性や、異なるデバイスや異なるブラウザーウィンドウサイズに異なる表示を行うレスポンシブデザインが使用されている可能性があります。 これらのニーズに対応するために、ビューアでは 3 つの主要な操作モード（ポップアップ、固定サイズの埋め込み、レスポンシブデザインの埋め込み）をサポートしています。

同じページへの複数のビデオの埋め込みは、タブレットやモバイルデバイスでサポートされています。 通常、一度に再生できるビデオは 1 つだけです。 ユーザーがあるビデオの再生を開始してから、別のビデオを再生しようとすると、最初のビデオは自動的に一時停止されます。 自動一時停止されたビデオは現在の再生時間を記憶しているので、ユーザーはいつでも元に戻って再生を再開できます。 唯一の例外は、ビデオを並行して再生できるAndroid™ 4.x デバイスのChrome ブラウザーです。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の web ブラウザーウィンドウまたはタブで開きます。 ブラウザーのウィンドウ領域全体を使用し、ブラウザーのサイズが変更された場合や、デバイスの向きが変更された場合に備えて調整されます。

このモードは、モバイルデバイスで最も一般的です。 Web ページは、JavaScript呼び出し、HTML要素 `window.open()` の適切な設定、またはその他の適切なメソッド `A` 使用して、ビューアを読み込みます。

ポップアップ操作モードには、標準のHTML ページを使用することをお勧めします。 このフォルダーは [!DNL Video360Viewer.html] と呼ばれ、標準の IS-Viewers デプロイメントの [!DNL html5/] サブフォルダーに配置されています。

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタム CSS を適用すると、視覚的にカスタマイズできます。

次に、新しいウィンドウでビューアを開くHTML コードの例を示します。

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアが既存の web ページに追加されます。これには、ビューアに関連しない顧客コンテンツが既に含まれている場合があります。 閲覧者は通常、Web ページの不動産の一部のみを占有します。

主なユースケースは、デスクトップまたはタブレットデバイス向けの web ページと、デバイスタイプに応じて自動的にレイアウトを調整するレスポンシブデザインのページです。

固定サイズの埋め込みは、初回読み込み後にビューアのサイズが変更されない場合に使用されます。 この方法は、静的なレイアウトを持つ web ページに最適です。

レスポンシブデザインの埋め込みは、コンテナコンポー `DIV` ントのサイズ変更に応じて、実行時にビューアのサイズを変更する必要があることを前提としています。 最も一般的なユースケースは、柔軟なページレイアウトを使用する web ページにビューアを追加する場合です。

レスポンシブデザインの埋め込みモードでは、web ページのコンテナコンポー `DIV` ントのサイズがどのように調整されるかに応じて、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さが制限されない場合、ビューアは、使用されるアセットの縦横比に応じて自動的に高さを選択します。 この機能により、アセットが側面にパディングを入れずに、ビューに完全に収まります。 このユースケースは、Bootstrapや Foundation などのレスポンシブ web デザインレイアウトフレームワークを使用した web ページで最も一般的です。

そうでない場合、web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されていると、ビューアはその領域だけを埋め、web ページレイアウトが提供するサイズに従います。 良い例は、ビューアをモーダルオーバーレイに埋め込む場合です。この場合、オーバーレイは web ブラウザーのウィンドウサイズに応じてサイズが調整されます。

**固定サイズ埋め込み**

Web ページにビューアを追加するには、次の手順を実行します。

1. Web ページへのビューアJavaScript ファイルの追加
1. コンテナ `DIV` を定義します。
1. ビューアサイズの設定。
1. ビューアの作成と初期化。

1. Web ページへのビューアJavaScript ファイルの追加

   ビューアを作成するには、HTMLのヘッドにスクリプトタグを追加する必要があります。 ビューア API を使用する前に、必ず [!DNL Video360Viewer.js] を含めてください。 [!DNL Video360Viewer.js] ファイルは、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

ビューアがAdobe Dynamic Media Classic サーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 そうでない場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classic サーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページ上のメインビューアのJavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性がある web ページコード内の追加のJavaScript ファイルを参照しないでください。 特に、ビューアによって読み込まれるHTML5 SDK `Utils.js` ライブラリを、コンテキストパス（いわゆる統合SDK `/s7viewers`）から直接参照 `include` ないでください。 これは、`Utils.js` や類似のランタイム・ビューア・ライブラリの場所はビューアのロジックによって完全に管理され、ビューア・リリース間で場所が変更されるためです。 Adobeは、古いバージョンのセカンダリビューア `includes` をサーバーに保持しません。
>
>
>その結果、ビューアが使用するセカンダリ JavaScript `include` ージをページ上で直接参照すると、今後、新しい製品バージョンがデプロイされた際に、ビューアの機能が損なわれます。

1. コンテナ `DIV` を定義します。

   ビューアを表示するページに、空の `DIV` 要素を追加します。 `DIV` 要素には ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるためです。 DIV のサイズは CSS で指定します。

   プレースホルダー `DIV` は配置済み要素です。つまり、`position` CSS プロパティは `relative` または `absolute` に設定されています。

   Internet Explorer でフルスクリーン機能を正しく機能させるには、プレースホルダーフ `DIV` ールドよりも重ね順が大きい要素が DOM に他にないことを確認します。

   定義されたプレースホルダー `DIV` 要素の例を以下に示します。

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズは、トップレベル CSS クラスに対して絶対単位で宣言す `.s7video360viewer` か、修飾子を使用して設定 `stagesize` きます。

   サイズ設定は、CSS のHTML ページに直接配置することも、カスタムビューア CSS ファイルに配置することもできます。この CSS ファイルは、後でAdobe Experience Manager Assetsのビューアプリセットレコードにオンデマンドで割り当てられたり、コマンドを使用して明示的に渡され `style` りします。

   CSS を使用したビューアのスタイル設定について詳しくは、[Video360 ビューアのカスタマイズ ](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   HTML ページで静的ビューアサイズを定義する例を以下に示します。

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   `stagesize` 修飾子は、AEM Assetsのビューアプリセットレコードのオンデマンドで設定できます。 または、次のように、コレクションを使用して、またはコマンドリファレンスの節で説明されてい `params` ように、API 呼び出しとしてビューア初期化コードで明示的に渡すこともできます。

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   この例では、CSS ベースのアプローチをお勧めします。

1. ビューアの作成と初期化。

   上記の手順を完了したら、クラスのインスタンスを作成し、すべての設定情報 `s7viewers.Video360Viewer` そのコンストラクターに渡し、ビューアインスタンスのメソッド `init()` 呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトにはビューアコンテナ ID の名前 `containerId` 保持するフィールドと、ビューアでサポートされ `params` 設定パラメーターを含むネストされた JSON オブジェクトが必要です。

   この場合、`params` オブジェクトには、少なくとも画像サービング URL がプロパティとして渡され、初期アセット `serverUrl` パラメーターとして渡されてい `asset` 必要があります。 JSON ベースの初期化 API を使用すると、1 行のコード、プロパティとして渡されたビデオサーバー URL、パラメーターとしての初期アセット、プロパティとして `videoserverurl` ンタラクティブデータで、ビューア `asset` 作成および起動 `interactivedata` きます。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成して開始できます。

   ビューアコードが ID でコンテナ要素を見つけられるように、ビューアコンテナを DOM に追加することが重要です。 一部のブラウザーでは、web ページの最後まで DOM の構築が遅れます。 互換性を最大限に高めるには、終了 `init()` タグの直前または body `BODY` イベントで `onload()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ web ページレイアウトの一部である必要はありません。 例えば、割り当てられたスタイルを使用して非表示 `display:none` する場合があります。 この場合、ビューアは、web ページがコンテナ要素をレイアウトに戻す瞬間まで、初期化プロセスを遅延します。 その際、ビューアの読み込みが自動的に再開されます。

   以下に、ビューアインスタンスを作成し、必要な最小限の設定オプションをコンストラクターに渡して、`init()` メソッドを呼び出す例を示します。 この例では、次のことを前提としています。

   * ビューアインスタンスは `video360Viewer` です。
   * プレースホルダー `DIV` の名前は `s7viewer` です。
   * 画像サービング URL は `https://s7d9.scene7.com/is/image` です。
   * ビデオサーバーの URL は `https://s7d9.scene7.com/is/content` です。
   * アセットは `Viewers/space_station_360-AVS` です。

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   次のコードは、Video360 ビューアを固定サイズで埋め込む単純な web ページの完全な例です。

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**高さが制限されないレスポンシブデザインの埋め込み**

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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**幅と高さが定義されたレスポンシブ埋め込み**

幅と高さが定義されたレスポンシブ埋め込みがある場合、web ページのスタイル設定は異なります。 `"holder"` DIV のサイズとブラウザーウィンドウの中央に合わせたサイズの両方が提供されます。 また、web ページでは、`HTML` と `BODY` 要素のサイズが 100% に設定されます。

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

残りの埋め込みステップは、高さが制限されないレスポンシブ埋め込みに使用されるステップと同じです。 結果の例を次に示します。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Setter ベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、setter ベースの API および no-args コンストラクターを使用することができます。 この API コンストラクターを使用すると、パラメーターは取得されず、`setContainerId()`、`setParam()`、`setAsset()` の API メソッドを使用して、個別のJavaScript呼び出しで設定パラメーターが指定されます。

次の例は、setter ベースの API を使用した固定サイズの埋め込みの使用を示しています。

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
