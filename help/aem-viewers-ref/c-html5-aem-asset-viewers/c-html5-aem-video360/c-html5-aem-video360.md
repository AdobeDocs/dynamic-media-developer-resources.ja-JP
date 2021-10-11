---
title: ビデオ 360
description: HTML5 Video360 ビューアは、Dynamic Media ClassicまたはDynamic Media、Adobe Experience Managerから配信され、H.264 形式でエンコードされたストリーミングおよびプログレッシブ 360 ビデオを再生する 360 度ビデオプレーヤーです。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# ビデオ 360{#video}

HTML5 Video360 ビューアは、Dynamic Media ClassicまたはDynamic Media、Adobe Experience Managerから配信され、H.264 形式でエンコードされたストリーミングおよびプログレッシブ 360 ビデオを再生する 360 度ビデオプレーヤーです。

360 度ビデオ（イマーシブビデオや球形ビデオとも呼ばれる）は、全方位カメラやカメラのコレクションを使用して、全方向のビューを同時に記録するビデオ録画です。 単一のビデオとアダプティブビデオセットの両方がサポートされています。 また、外部の場所でホストされるプログレッシブビデオおよび HLS ストリームの操作もサポートしています。

360 ビデオの推奨縦横比は 2:1 です。 空間音はサポートされていません。 このビューアは 360 ビデオでのみ機能するように設計されています。360 ビデオ以外のビデオを再生しようとすると、ビデオの再生がゆがむ。

このビューアは、デスクトップとモバイルの両方で動作し、HTML5 ビデオをサポートしている Web ブラウザーで動作するように設計されています。 ビューアでは、オプションのソーシャル共有ツールがサポートされています。

Video360 ビューアは、基になるシステムが HLS 形式をサポートしている場合は常に、デフォルト設定で HLS 形式のHTML5 ストリーミングビデオ再生を使用します。 HTML5 ストリーミングをサポートしていないシステムでは、ビューアはHTML5 プログレッシブビデオ配信にフォールバックされます。

ビューアタイプは 517 です。

## デモ URL {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## システム要件 {#section-b7270cc4290043399681dc504f043609}

[ 必要システム構成 ](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842) を参照してください。

## Video360 ビューアの使用 {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 ビューアは、メインの JavaScript ファイルと、ヘルパーファイルのセット ( このビューアで使用されるすべてのHTML5 Viewer SDK コンポーネントを含む単一の JavaScript インクルード、アセット、CSS) で、ビューアによって実行時にダウンロードされます。

HTML5 Video360 ビューアは、IS ビューアに付属の実稼動用HTMLページを使用するポップアップモードと、API を使用してターゲット Web ページに統合される埋め込みモードの両方で使用できます。

設定とスキン表示は、このガイドで説明する他のビューアと同様です。 スキン表示はすべて、カスタム (CSS) カスケーディングスタイルシートを使用して行います。

[ すべてのビューアに共通のコマンドリファレンス — 設定属性 ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) および [ すべてのビューアに共通のコマンドリファレンス — URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください。

360 ビデオコンテンツは、標準の 360 以外のビデオよりも高いエンコーディング設定が必要です。 つまり、同じ知覚可能な画質を実現するには、360 コンテンツが 360 ビデオ以外のビデオよりも高い解像度になる必要があります。 360 ビデオに対する次のアダプティブビデオプリセット設定を検討することをお勧めします。

* 720p、2500 kbps
* 1,080p、5,000 kbps
* 1440p、6600 kbps

ただし、このような高品質の設定でエンコードされたビデオを提供するには、エンドユーザーのデバイスで高帯域幅の接続が必要になります。

## Video360 ビューアの操作 {#section-642e66ca38cd4032992840ec6c0b0cd2}

HTML5 Video360 ビューアは、再生/一時停止ボタン、ビデオスクラバビデオの時間の吹き出し、再生時間/合計時間のインジケータ、ボリュームコントロール、フルスクリーンボタンなど、ビデオ再生用の一連の標準的なユーザインターフェイスコントロールを提供します。 これらのコントロールはすべて、ビューアのユーザインターフェイスの下部にあるコントロールバーにまとめられます。

タッチデバイスでは、デバイスのハードウェアボタンを使用してのみボリュームを制御できるので、ボリュームコントロールはユーザーインターフェイスに表示されません。

ビューアがポップアップモードで動作している場合、ユーザーインターフェイスでフルスクリーンボタンは使用できません。

このビューアは、様々なソーシャルメディア共有ツールもサポートしています。 これらは、ユーザーインターフェイスの単一のボタンとして使用でき、ユーザーがクリックまたはタップすると共有ツールバーに展開されます。 共有ツールバーには、Facebook、Twitter、電子メール共有、埋め込みコード共有、リンク共有など、サポートされる共有チャネルの各タイプ用のアイコンが表示されます。 電子メール共有、埋め込み共有、リンク共有の各ツールをアクティブにすると、ビューアにモーダルダイアログボックスが表示され、対応するデータ入力フォームが表示されます。 facebookまたはTwitterを呼び出すと、ソーシャルメディアサービスの標準の共有ダイアログボックスにリダイレクトされます。 また、共有ツールが有効になると、ビデオ再生は自動的に一時停止します。 Web ブラウザーのセキュリティ上の制限により、共有ツールはフルスクリーンモードでは使用できません。

ビューアでは、次の場合の 360 ビデオ再生がサポートされます。

* VR ヘッドセット (Oculus Go やOculus Riftなど )
* VR HMD（ヘッドマウントディスプレイ）マウント (Google Dalboold など )
* VR 非対応のデバイス（VR HMD マウントに接続されていないデスクトップブラウザー、タブレット、携帯電話など）

VR ヘッドセットで 360 ビデオコンテンツを表示する場合、追加の設定は必要ありません。 ビューアは VR ヘッドセットの存在を自動的に検出し、ビデオコンテンツの上に「VR」ボタンを表示します。 この「VR」ボタンをオンにすると、ビデオレンダリングが VR モードに切り替わります。 ビューアは、WebVR がサポートされているブラウザーでのみ VR レンダリングをサポートします。

VR HMD をマウントするには、ビューアの設定で `Video360Player.vrrender` 修飾子を `1` に設定し、立体的なレンダリングを強制する必要があります。

VR ヘッドセットおよび VR HMD マウントでは、VR モードで他の再生制御が提供されるのではなく、ヘッドセットの動きに応じて視点の変更が行われます。

VR 非対応デバイスで 360 ビデオを視聴する場合、エンドユーザーはマウス、タッチ、キーボードを使用して、ビデオの再生と視点を制御できます。

ビューアは、タッチスクリーンとマウスを備えた Windows デバイスでのタッチ入力とマウス入力の両方をサポートします。ただし、このサポートは、Chrome、Internet Explorer 11 および Edge Web ブラウザーに限られます。

ビューアが完全にキーボードでアクセス可能。 [ キーボードのアクセシビリティとナビゲーション ](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861) を参照してください。

## Video360 ビューアの埋め込み {#section-6bb5d3c502544ad18a58eafe12a13435}

ビューアの動作に対するニーズは、Web ページごとに異なります。 Web ページにリンクが表示され、このリンクをクリックすると別のブラウザーウィンドウでビューアが開く場合があります。 ホストページに直接ビューアを埋め込む必要がある場合もあります。 後者の場合は、Web ページが静的ページレイアウトである場合や、デバイスごと、ブラウザーウィンドウのサイズごとに表示方法が変わるレスポンシブデザインを使用する場合があります。 これらのニーズに対応するため、ビューアでは次の 3 つの主要な操作モードをサポートしています。ポップアップ、固定サイズ埋め込み、レスポンシブデザイン埋め込み。

同じページへの複数のビデオの埋め込みは、タブレットおよびモバイルデバイスでサポートされています。 通常、一度に再生できるビデオは 1 つだけです。 ユーザーが 1 つのビデオの再生を開始し、別のビデオの再生を試みると、最初のビデオが自動的に一時停止します。 自動一時停止になったビデオは現在の再生時間を記憶するので、ユーザーはいつでもビデオに戻って再生を再開できます。 ただし、Android™ 4.x デバイスの Chrome ブラウザーでは、ビデオを並行して再生できます。

**ポップアップモードについて**

ポップアップモードでは、ビューアは別の Web ブラウザーウィンドウまたはタブに開きます。 ブラウザーウィンドウの全領域を占め、ブラウザーのサイズやデバイスの向きが変更された場合は調整されます。

このモードは、モバイルデバイスで最も一般的なモードです。 Web ページでは、`window.open()` JavaScript 呼び出し、適切に設定された `A`HTML要素、またはその他の適切な方法を使用してビューアを読み込みます。

ポップアップ操作モードには、標準搭載のHTMLページを使用することをお勧めします。 このページは [!DNL Video360Viewer.html] と呼ばれ、標準の IS-Viewers デプロイメントの [!DNL html5/] サブフォルダーにあります。

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

カスタム CSS を適用することで、視覚的なカスタマイズを実現できます。

以下は、ビューアを新しいHTMLで開くウィンドウコードの例です。

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**固定サイズ埋め込みモードとレスポンシブデザイン埋め込みモードについて**

埋め込みモードでは、ビューアは既存の Web ページに追加されます。既に、ビューアに関連しない顧客コンテンツが含まれている場合があります。 ビューアは通常、Web ページの一部の領域のみを占めます。

主な使用例は、デスクトップやタブレットデバイス向けの Web ページ、およびデバイスの種類に応じてレイアウトを自動的に調整するレスポンシブデザインページです。

固定サイズ埋め込みは、初回の読み込み後にビューアのサイズが変更されない場合に使用します。 この方法は、静的レイアウトの Web ページに最適です。

レスポンシブデザイン埋め込みは、コンテナ `DIV` のサイズ変更に対応して実行時にビューアのサイズを変更する必要がある場合を想定しています。 最も一般的な使用例は、柔軟なページレイアウトを使用する Web ページにビューアを追加する場合です。

レスポンシブデザイン埋め込みモードでは、Web ページによるコンテナ `DIV` のサイズ変更の方法によって、ビューアの動作が異なります。 Web ページでコンテナ `DIV` の幅のみが設定され、高さは無制限のままの場合、ビューアでは、使用するアセットの縦横比に従って高さが自動的に選択されます。 この機能により、両側のパディングなしで、アセットが表示にぴったりと収まります。 この使用例は、Bootstrapや基盤などのレスポンシブ Web デザインレイアウトフレームワークを使用する Web ページで最も一般的です。

また、Web ページでビューアのコンテナ `DIV` の幅と高さの両方が設定されている場合、ビューアはその領域を占め、Web ページのレイアウトで指定されているサイズに従います。 良い例として、ビューアをモーダルオーバーレイに埋め込み、オーバーレイが Web ブラウザーのウィンドウサイズに従ってサイズ設定される場合があります。

**固定サイズ埋め込み**

ビューアを Web ページに追加するには、次の手順を実行します。

1. ビューアの JavaScript ファイルを Web ページに追加します。
1. コンテナ `DIV` を定義します。
1. ビューアのサイズを設定します。
1. ビューアを作成して初期化する

1. ビューアの JavaScript ファイルを Web ページに追加します。

   ビューアを作成するには、スクリプトタグをHTMLhead に追加する必要があります。 ビューアの API を使用する前に、必ず [!DNL Video360Viewer.js] を含めてください。 [!DNL Video360Viewer.js] ファイルは、次に示すように、標準の IS-Viewers デプロイメントの [!DNL html5/js/] サブフォルダーにあります。

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

ビューアがAdobe Dynamic Media Classicサーバーの 1 つにデプロイされ、同じドメインから提供される場合は、相対パスを使用できます。 それ以外の場合は、IS ビューアがインストールされているAdobe Dynamic Media Classicサーバーの 1 つへのフルパスを指定します。

相対パスは次のようになります。

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>ページでは、メインビューアの JavaScript `include` ファイルのみを参照します。 実行時にビューアのロジックによってダウンロードされる可能性のある Web ページコード内の追加の JavaScript ファイルは参照しないでください。 特に、`/s7viewers` コンテキストパス（いわゆる統合 SDK `include`）からビューアによって読み込まれたHTML5 SDK `Utils.js` ライブラリを直接参照しないでください。 この理由は、`Utils.js` や類似のランタイムビューアライブラリの場所がビューアのロジックによって完全に管理され、ビューアのリリース間で位置が変わるからです。 Adobeは、古いバージョンのセカンダリビューア `includes` をサーバ上に保持しません。
>
>
>その結果、新しい製品バージョンがデプロイされると、ビューアが使用するセカンダリ JavaScript `include` への直接参照をページに配置すると、将来ビューア機能が壊れます。

1. コンテナ `DIV` を定義します。

   ビューアを表示するページに空の `DIV` 要素を追加します。 `DIV` 要素の ID は、後でビューアの API に渡されるので、定義する必要があります。 DIV のサイズは CSS で指定します。

   プレースホルダー `DIV` は配置する要素です。つまり、CSS の `position` プロパティを `relative` または `absolute` に設定します。

   Internet Explorer でフルスクリーン機能を正しく機能させるには、DOM 内にプレースホルダー `DIV` よりも重ね順の高い要素が存在しないことを確認します。

   次に、定義済みのプレースホルダー `DIV` 要素の例を示します。

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. ビューアサイズの設定

   ビューアの静的サイズを設定するには、最上位 CSS クラスに対して絶対単位で宣言するか、`.s7video360viewer` 修飾子を使用します。`stagesize`

   サイズ調整は、CSS で直接HTMLページまたはカスタムビューアの CSS ファイルに配置できます。この CSS ファイルは、後でAdobe Experience Manager Assets - On-demand のビューアプリセットレコードに割り当てられるか、`style` コマンドを使用して明示的に渡されます。

   CSS でのビューアのスタイル設定について詳しくは、[ ビデオ 360 ビューアのカスタマイズ ](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) を参照してください。

   以下は、静的ビューアサイズを定義する例です。HTMLページ

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   AEM Assets — オンデマンドのビューアプリセットレコードで `stagesize` 修飾子を設定できます。 または、次のように、 `params` コレクションを使用してビューア初期化コードを明示的に渡すことも、コマンドリファレンスの節で説明するように API 呼び出しとして渡すこともできます。

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   CSS ベースのアプローチを推奨し、この例で使用します。

1. ビューアを作成して初期化する

   上記の手順を完了したら、`s7viewers.Video360Viewer` クラスのインスタンスを作成し、すべての設定情報をコンストラクターに渡して、ビューアインスタンスで `init()` メソッドを呼び出します。 設定情報は、JSON オブジェクトとしてコンストラクターに渡されます。 最低でも、このオブジェクトには `containerId` フィールドが必要です。このフィールドには、ビューアのコンテナ ID の名前と、ビューアでサポートされている設定パラメーターを含むネストされた `params` JSON オブジェクトが含まれています。

   この場合、 `params` オブジェクトには、少なくとも `serverUrl` プロパティとして渡された画像サービング URL が含まれ、最初のアセットが `asset` パラメーターとして含まれている必要があります。 JSON ベースの初期化 API を使用すると、1 行のコード、`videoserverurl` プロパティとして渡されたビデオサーバの URL、`asset` パラメーターとしての最初のアセット、`interactivedata` プロパティとしてのインタラクティブデータを使用して、ビューアを作成して起動できます。 JSON ベースの初期化 API を使用すると、1 行のコードでビューアを作成し、起動できます。

   ビューアのコンテナを DOM に追加して、ビューアのコードが ID でコンテナ要素を見つけられるようにすることが重要です。 一部のブラウザーでは、Web ページの末尾まで DOM の構築が遅れます。 互換性を最大にするには、 `BODY` 終了タグの直前、または本文の `onload()` イベントで `init()` メソッドを呼び出します。

   同時に、コンテナ要素は、まだ Web ページレイアウトの一部ではない必要があります。 例えば、`display:none` スタイルを割り当てて非表示にすることができます。 この場合、Web ページでコンテナ要素がレイアウトに戻るまで、ビューアは初期化プロセスを遅延します。 その場合、ビューアの読み込みが自動的に再開されます。

   次の例では、ビューアインスタンスを作成し、最低限必要な設定オプションをコンストラクターに渡して `init()` メソッドを呼び出します。 この例では、次の点が前提となります。

   * ビューアインスタンスは `video360Viewer` です。
   * プレースホルダ `DIV` の名前は `s7viewer` です。
   * 画像サービングの URL は `https://s7d9.scene7.com/is/image` です。
   * ビデオサーバーの URL は `https://s7d9.scene7.com/is/content` です。
   * アセットは `Viewers/space_station_360-AVS` です。

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

レスポンシブデザイン埋め込みでは、Web ページには通常、ビューアのコンテナ `DIV` の実行時のサイズを指示する柔軟なレイアウトが指定されています。 次の例では、Web ページでビューアのコンテナ `DIV` が Web ブラウザーのウィンドウサイズの 40%を占めることを許可し、高さは無制限のままにするとします。 Web ページのHTMLコードは次のようになります。

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

このようなページにビューアを追加する手順は、固定サイズ埋め込みの手順と似ています。 唯一の違いは、ビューアのサイズを明示的に定義する必要がないことです。

1. ビューアの JavaScript ファイルを Web ページに追加します。
1. コンテナ DIV を定義する。
1. ビューアを作成して初期化する

上記の手順は、固定サイズ埋め込みの場合と同じです。 コンテナ DIV を既存の `"holder"` DIV に追加します。 次のコードは完全な例です。 ブラウザーのサイズが変更されたときにビューアのサイズが変化し、ビューアの縦横比がアセットと一致することに注意してください。

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

幅と高さが定義されたレスポンシブ埋め込みがある場合、Web ページのスタイル設定は異なります。 `"holder"` DIV に両方のサイズを提供し、ブラウザーウィンドウの中央に配置します。 また、Web ページでは、`HTML` 要素と `BODY` 要素のサイズを 100%に設定します。

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

残りの埋め込み手順は、高さ無制限のレスポンシブ埋め込みに使用した手順と同じです。 結果の例を次に示します。

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

JSON ベースの初期化を使用する代わりに、セッターベースの API と no-args コンストラクターを使用できます。 この API を使用する場合は、コンストラクターにパラメーターは不要です。設定パラメーターは、 `setContainerId()` 、 `setParam()` および `setAsset()` の各 API メソッドを別々の JavaScript 呼び出しで使用して指定します。

次の例は、固定サイズ埋め込みをセッターベースの API と共に使用する方法を示しています。

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
