---
description: レスポンシブ画像ライブラリは、Scene7から提供される画像の品質を動的に調整し、レスポンシブWebページに埋め込むJavaScriptモジュールです。 また、高密度の画面を持つデバイスの画質も向上します。 ライブラリは、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。
seo-description: レスポンシブ画像ライブラリは、Scene7から提供される画像の品質を動的に調整し、レスポンシブWebページに埋め込むJavaScriptモジュールです。 また、高密度の画面を持つデバイスの画質も向上します。 ライブラリは、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。
seo-title: レスポンシブ画像ライブラリについて
solution: Experience Manager
title: レスポンシブ画像ライブラリについて
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# レスポンシブ画像ライブラリについて{#about-responsive-image-library}

レスポンシブ画像ライブラリは、Scene7から提供される画像の品質を動的に調整し、レスポンシブWebページに埋め込むJavaScriptモジュールです。 また、高密度の画面を持つデバイスの画質も向上します。 ライブラリは、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。

## デモURL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

レスポンシブ画像ライブラリの最も簡単な使用例は、画像の幅に対してブレークポイント値のリストを定義することです。 このリストを使用すると、Webページのレイアウトがユーザーによってブラウザーウィンドウのサイズ変更やデバイスの向きの変更を受けて変更されるので、画像のサイズが変更されたときに、適切なレンディションが読み込まれて表示されます。 ライブラリは画面上の画像サイズを継続的に監視し、新しいブレークポイントの幅に達するたびに、Scene7から新しい画像レンディションを取得します。

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>デモURL </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>以下は、レスポンシブ画像がWebページの幅の50%を占めるコンテナ内にある簡単な例です。 ブラウザーウィンドウのサイズが変更されるたびに、コンテナーの幅が変わります。 イメージの幅が、設定されたブレークポイントの1つ（200、400、600、800ピクセルで設定されている）に達すると、新しいレンディションがダウンロードされ、表示されます。 目標は、不要な大きい画像を読み込まないようにし、ネットワークの帯域幅を節約することです。 </p> <p>URLをクリックしてWebページを開き、ブラウザーウィンドウのサイズを変更し、ネットワークトラフィックを監視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>次のBootstrap例は、Webページでの同じ使用例を示しています。 BootstrapCSSに従って、レスポンシブ画像を追加するレイアウトセルは、次のいずれかの幅になります。360、720および940ピクセル。 これらは、レスポンシブ画像ライブラリにブレークポイントとして渡される正確な値です。 そのため、Scene7は、クライアントのネットワーク帯域幅が有効に使用されるようにします。 また、現在のWebページのレイアウトに合わせて、画像が必要なサイズで表示され、クライアント側のブラウザーの拡大/縮小による視覚的な影響を受けません。 </p> <p>URLをクリックしてWebページを開き、ブラウザーウィンドウのサイズを変更して異なるレイアウトブレークポイントに到達し、ネットワークトラフィックを監視します。 </p> <p>より高度な使用例として、異なる画像プリセット、画像サービングコマンド、またはその両方を異なるブレークポイント値に関連付けることがあります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>次の例では、異なるブレークポイントサイズに対して、異なる画質と形式の画像プリセットを使用します。 小さいブレークポイントの場合は、低画質プリセットが適用され、画像サービングから強制的に6色に圧縮されたGIF画像が返されます。 中程度のブレークポイントは、高圧縮のJPEG用に設定された画像プリセットを使用しています。 最大のブレークポイントは、可逆圧縮形式のPNGを使用した高品質画像プリセットに関連付けられます。 この方法により、大きい画面を持つデバイスの帯域幅と処理能力が大きいという前提に基づき、高品質の画像がそのようなデバイスに配信されます。 </p> <p>URLをクリックしてWebページを開き、Webブラウザーウィンドウのサイズを大きくして小さくし、画質が低下するのを確認します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>画像プリセットに加えて、特定の画像サービングコマンドをブレークポイントに関連付けることができます。 次の例は、画面上の画像サイズが小さくなるにつれて、バナー画像を目標領域に合わせて徐々に切り抜く方法を示しています。 ここでは、最大のブレークポイントには画像サービングコマンドがまったくないので、バナーの画像は完全に表示されます。 中程度のブレークポイントでは、中程度の切り抜きが適用され、「実行中」というテキストを持つランナーのみが表示されます。 小さいブレークポイントでは、より多くの切り抜きが適用され、製品のみが表示されます。 </p> <p>URLをクリックしてWebページを開き、ブラウザーウィンドウのサイズを変更します。 大きい方のサイズから小さい方のサイズに移動するに従って、徐々に画像が切り抜かれることに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>また、画像サービングコマンドと画像サービングテンプレートを使用して、画像サイズに基づいて特定のテンプレートパラメータを制御することもできます。 次の例では、テキストオーバーレイのフォントサイズが<span class="codeph"> $fontsize </span>パラメーターを使用してパラメータ化されている場合に、画像サービングテンプレートを使用します。 レスポンシブ画像は、テキストが常に読み取り可能な状態を保つために、小さい画像サイズには大きいフォントサイズを使用するように設定されています。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 必要システム構成 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**サーバのハードウェアとソフトウェア**

* Scene7画像サービング6.0.1以降。

**クライアントブラウザーの最小要件**

* Microsoft® Windows® 7以降Mac OS X 10.8以降。
* Firefox 23、Safari 6、Chrome 29、IE 9以降。
* iOS 6以降。
* iPhone3GS以降およびiPad2以降（ネイティブブラウザーのみ）で認定。
* Android OS 2.3以降。
* モバイルデバイス上のInternet Explorerは、現時点ではサポートされていません。

