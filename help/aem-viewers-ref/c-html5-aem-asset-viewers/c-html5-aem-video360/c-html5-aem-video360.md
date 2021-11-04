---
title: ビデオ 360
description: HTML5 Video360 ビューアは、Dynamic Media ClassicまたはDynamic MediaのAdobe Experience Managerから配信される、H.264 形式でエンコードされたストリーミングビデオとプログレッシブ 360 ビデオを再生する 360 度ビデオプレーヤーです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# ビデオ 360{#video}

HTML5 Video360 ビューアは、Dynamic Media ClassicまたはDynamic MediaのAdobe Experience Managerから配信される、H.264 形式でエンコードされたストリーミングビデオとプログレッシブ 360 ビデオを再生する 360 度ビデオプレーヤーです。

360 度ビデオ（没入型ビデオや球形ビデオとも呼ばれます）は、全方位カメラやカメラのコレクションを使用して撮影し、あらゆる方向のビューを同時に記録するビデオ録画です。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、外部でホストされるプログレッシブビデオおよび HLS ストリームの操作もサポートしています。

360 ビデオの推奨縦横比は 2:1 です。 空間サウンドはサポートされていません。 このビューアは 360 ビデオでのみ機能するように設計されています。360 ビデオ以外の再生を試みると、ビデオがゆがんで再生される。

このビューアは、デスクトップとモバイル Web ブラウザーの両方で動作し、HTML5 ビデオをサポートしています。 ビューアは、オプションのソーシャル共有ツールをサポートしています。

Video360 ビューアは、基になるシステムが HLS 形式をサポートしている場合は常に、デフォルト設定で HLS 形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックします。

ビューアのタイプは 517 です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

詳しくは、 [必要システム構成](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Video360 ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 ビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット ( このビューア、アセット、CSS で使用されるすべてのHTML5 Viewer SDK コンポーネントが含まれる 1 つの JavaScript インクルード ) です。

HTML5 Video360 ビューアは、IS-Viewers に付属する実稼動用HTMLページを使用するポップアップモードと、API を使用してターゲット Web ページに統合される埋め込みモードの両方で使用できます。

設定とスキニングは、このガイドで説明する他のビューアと同様です。 スキニングは、すべてカスタム (CSS) カスケーディングスタイルシートを使用して行います。

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

360 ビデオコンテンツは、360 以外の標準のビデオよりも高いエンコーディング設定が必要です。 つまり、同じ知覚可能な品質を実現するには、360 コンテンツが 360 ビデオ以外のビデオよりも高い解像度で表示される必要があります。 360 ビデオに対しては、次のアダプティブビデオプリセット設定を考慮することをお勧めします。

* 720p、2500 kbps
* 1080p、5000 kbps
* 1440p、6600 kbps

ただし、このような高品質の設定でエンコードされたビデオを配信する場合は、エンドユーザーのデバイスで高帯域幅の接続が必要になります。

## Video360 ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 ビューアは、再生/一時停止ボタン、ビデオスクラバービデオの時間の吹き出し、再生時間/合計時間のインジケーター、ボリューム制御、フルスクリーンボタンなど、ビデオ再生に関する一連の標準的なユーザーインターフェイスコントロールを提供します。 これらのコントロールはすべて、ビューアのユーザインターフェイスの下部にあるコントロールバーにグループ化されています。

タッチデバイスでは、デバイスのハードウェアボタンを使用してのみボリュームを制御できるので、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでフルスクリーンボタンを使用することはできません。

ビューアは、様々なソーシャルメディア共有ツールもサポートしています。 これらは、ユーザーインターフェイスで 1 つのボタンとして使用でき、ユーザーがクリックまたはタップすると、共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプ用のアイコンが表示されます。 電子メール共有、埋め込み共有またはリンク共有のツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールが有効になると、ビデオ再生が自動的に一時停止します。 Web ブラウザーのセキュリティ制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアでは、次の場合の 360 ビデオ再生がサポートされています。

* VR ヘッドセット (Oculus Go やOculus Riftなど )
* VR HMD（ヘッドマウントディスプレイ）マウント (Google Dalbald など )
* 非 VR 対応デバイス（デスクトップブラウザー、タブレット、VR HMD マウントに接続されていない携帯電話など）

VR ヘッドセットで 360 ビデオコンテンツを表示する場合、追加の設定は必要ありません。 ビューアは VR ヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンをオンにすると、ビデオレンダリングが VR モードに切り替わります。 ビューアは、WebVR がサポートされているブラウザーでのみ、VR レンダリングをサポートします。

VR HMD を使用するには、 `Video360Player.vrrender` 修飾子は次の値に設定する必要があります： `1` を設定します。

VR ヘッドセットと VR HMD マウントでは、ヘッドセットの移動に応じて視点の変化が起こり、VR モードでは他の再生制御が提供されません。

VR が有効でないデバイスで 360 ビデオを視聴する場合、エンドユーザーはマウス、タッチまたはキーボードを使用して、ビデオの再生と視点を制御できます。

ビューアは、タッチスクリーンとマウスを備えた Windows デバイスで、タッチ入力とマウス入力の両方をサポートしています。ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーに限られます。

ビューアが完全にキーボードでアクセス可能になる。 詳しくは、 [キーボードのアクセシビリティとナビゲーション](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Video360 ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、このリンクを選択すると、別のブラウザーウィンドウでビューアが開く場合があります。 ホスティングページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Web ページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するために、ビューアでは次の 3 つの主要な操作モードがサポートされています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

同じページへの複数のビデオの埋め込みは、タブレットとモバイルデバイスでサポートされています。 通常、一度に 1 つのビデオのみ再生できます。 ユーザーが 1 つのビデオの再生を開始し、別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止されたビデオは現在の再生時間を記憶するので、ユーザーはいつでも元に戻って再生を再開できます。 ただし、Android™ 4.x デバイスの Chrome ブラウザーでは、ビデオを並行して再生できます。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブで開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、 `window.open()` JavaScript 呼び出し（適切に設定） `A` HTML要素、またはその他の適切な方法。

ポップアップ操作モードには、標準のHTMLページを使用することをお勧めします。 これは、と呼ばれます。 [!DNL Video360Viewer.html] そしてそれは以下の場所にある [!DNL html5/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタム CSS を適用することで、視覚的なカスタマイズを実現できます。

以下は、ビューアを新しいウィンドウでHTMLする開封コードの例です。

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。ビューアに関連しない顧客コンテンツが既に存在する場合があります。 ビューアは、通常、Web ページの一部の領域のみを占有します。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページと、デバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この方法は、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナのサイズ変更に応じて実行時にビューアのサイズを変更する必要がある場合を想定しています `DIV`. 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナのサイズ変更の方法によって、ビューアの動作が異なります `DIV`. Web ページでコンテナの幅のみが設定される場合 `DIV`で選択し、高さは無制限のままにし、使用するアセットの縦横比に従って、ビューアによって高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットが表示に完全に収まります。 この使用例は、Web や Foundation などのレスポンシブ Web デザインレイアウトフレームワークを使用する Web ページで最も一般的です。

それ以外の場合は、Web ページでビューアのコンテナの幅と高さの両方が設定されている場合 `DIV`を指定した場合、ビューアはその領域全体を占め、Web ページのレイアウトに従ってサイズが設定されます。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ変更される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナの定義 `DIV`.
1. ビューアのサイズを設定します。
1. ビューアを作成および初期化する。

1. ビューアの JavaScript ファイルを Web ページに追加する。

   ビューアを作成するには、HTMLhead にスクリプトタグを追加する必要があります。 ビューア API を使用する前に、 [!DNL Video360Viewer.js]. この [!DNL Video360Viewer.js] ファイルは [!DNL html5/js/] 標準の IS-Viewers デプロイメントのサブフォルダー

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

ビューアがいずれかのAdobe Dynamic Media Classicサーバーにデプロイされ、同じドメインから提供されている場合は、相対パスを使用できます。 それ以外の場合は、IS-Viewers がインストールされているAdobe Dynamic Media Classicのいずれかのサーバーへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>メインビューアの JavaScript のみを参照します。 `include` ファイルをページに貼り付けます。 実行時にビューアのロジックによってダウンロードされる可能性のある、Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、HTML5 SDK を直接参照しないでください `Utils.js` からビューアによって読み込まれたライブラリ `/s7viewers` コンテキストパス（いわゆる統合 SDK） `include`) をクリックします。 理由は、 `Utils.js` または同様のランタイムビューアライブラリは、ビューアのロジックによって完全に管理され、ビューアのリリースによって位置が変わります。 Adobeは古いバージョンのセカンダリビューアを保持しません `includes` をサーバー上に置きます。
>
>
>その結果、セカンダリ JavaScript への直接参照を配置する `include` ページ上でビューアが使用すると、新しい製品バージョンがデプロイされると、将来ビューア機能が機能しなくなります。

1. コンテナの定義 `DIV`.

   空の `DIV` 要素を追加します。 この `DIV` 要素は、その ID が定義されている必要があります。これは、この ID が後でビューア API に渡されるからです。 DIV のサイズは CSS で指定されます。

   プレースホルダー `DIV` は位置固定された要素で、 `position` CSS プロパティがに設定されている `relative` または `absolute`.

   フルスクリーン機能を Internet Explorer で正しく機能させるには、DOM 内に、プレースホルダーよりも重ね順の高い要素が存在しないことを確認します。 `DIV`.

   次に、定義済みのプレースホルダーの例を示します `DIV` 要素：

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、次のように宣言します `.s7video360viewer` 最上位の CSS クラス ( 絶対単位で、または `stagesize` 修飾子。

   サイズ調整は、HTMLーページ上で直接 CSS に配置することも、カスタムビューアの CSS ファイル内に配置することもできます。このファイルは、後でAdobe Experience Manager Assets（オンデマンド）のビューアプリセットレコードに割り当てられます。または、 `style` コマンドを使用します。

   詳しくは、 [Video360 ビューアのカスタマイズ](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   以下は、HTMLページで静的ビューアサイズを定義する例です。

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   次の設定が可能です。 `stagesize` 修飾子がAEM Assetsのビューアプリセットレコード — オンデマンド または、を使用して、ビューア初期化コードで明示的に渡すこともできます。 `params` コレクション、またはコマンドリファレンスの節で説明されている API 呼び出しとして、次のように指定します。

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSS ベースのアプローチを推奨します。この例では、を使用します。

1. ビューアを作成および初期化する。

   上記の手順を完了したら、のインスタンスを作成します。 `s7viewers.Video360Viewer` クラス、すべての設定情報をコンストラクタに渡し、を呼び出します。 `init()` メソッドを使用して、ビューアインスタンス上に配置できます。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 少なくとも、このオブジェクトには `containerId` ビューアのコンテナ ID とネストされたコンテナの名前が格納されるフィールド `params` ビューアでサポートされている設定パラメーターを持つ JSON オブジェクト。

   この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティとして、最初のアセットを `asset` パラメーター。 JSON ベースの初期化 API を使用すると、1 行のコードと、として渡されるビデオサーバ URL を使用して、ビューアを作成し、開始できます。 `videoserverurl` プロパティ、初期アセット `asset` パラメーターとしてのインタラクティブデータ `interactivedata` プロパティ。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの終わりまで DOM の構築が遅れます。 互換性を最大限に高めるには、 `init()` 終了直前の方法 `BODY` タグ、または本文 `onload()` イベント。

   同時に、コンテナ要素は、必ずしも Web ページレイアウトに含まれているとは限りません。 例えば、 `display:none` スタイルが割り当てられています。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 その場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して、 `init()` メソッド。 この例では、次のように想定しています。

   * ビューアインスタンスは `video360Viewer`.
   * プレースホルダーの名前 `DIV` が `s7viewer`.
   * 画像サービング URL は `https://s7d9.scene7.com/is/image`.
   * ビデオサーバーの URL は `https://s7d9.scene7.com/is/content`.
   * アセットは `Viewers/space_station_360-AVS`.

   ```
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

   次のコードは、固定サイズの Video360 ビューアを埋め込んだ簡単な Web ページの例です。

   ```
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

**高さ無制限のレスポンシブデザイン埋め込み**

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナの実行時のサイズを指示する柔軟なレイアウトが指定されています `DIV`. 次の例では、Web ページがビューアのコンテナを許可しているとします `DIV` を使用すると、web ブラウザーのウィンドウサイズの 40%を占め、高さは無制限のままになります。 Web ページのHTMLコードは次のようになります。

```
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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がない点です。

1. ビューアの JavaScript ファイルを Web ページに追加する。
1. コンテナ DIV を定義する。
1. ビューアを作成および初期化する。

上記の手順はすべて、固定サイズ埋め込みの場合と同じです。 コンテナ DIV を既存の `"holder"` DIV. 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化すること、およびビューアの縦横比がアセットと一致することに注意してください。

```
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

幅と高さが定義されたレスポンシブ埋め込みがある場合、Web ページのスタイル設定は異なります。 次の両方のサイズを `"holder"` DIV を指定し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは `HTML` および `BODY` 要素を 100%に設定します。

```
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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みに使用した手順と同じです。 結果の例は次のようになります。

```
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

**セッターベースの API を使用した埋め込み**

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API コンストラクターを使用する場合は、パラメーターは必要ありません。設定パラメーターは、 `setContainerId()`, `setParam()`、および `setAsset()` API メソッドを個別の JavaScript 呼び出しで使用できます。

次の例は、固定サイズ埋め込みをセッターベースの API で使用する方法を示しています。

```
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
