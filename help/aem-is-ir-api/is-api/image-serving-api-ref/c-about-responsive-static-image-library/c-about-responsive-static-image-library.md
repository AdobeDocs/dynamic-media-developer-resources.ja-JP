---
description: レスポンシブ画像ライブラリは、Dynamic Mediaから提供され、レスポンシブWebページに埋め込まれる画像の品質を動的に調整するJavaScriptモジュールです。 また、高密度の画面を持つデバイスの画質も向上します。 ライブラリは、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。
solution: Experience Manager
title: レスポンシブ画像ライブラリについて
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 417fd2540c15762356dfb60aa7eb635ee5f74d13
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 0%

---

# レスポンシブ画像ライブラリについて{#about-responsive-image-library}

レスポンシブ画像ライブラリは、Dynamic Mediaから提供され、レスポンシブWebページに埋め込まれる画像の品質を動的に調整するJavaScriptモジュールです。 また、高密度の画面を持つデバイスの画質も向上します。 ライブラリは、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。

## デモURL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

レスポンシブ画像ライブラリの最も簡単な使用例は、画像の幅のブレークポイント値のリストを定義することです。 このリストは、ユーザーがブラウザーウィンドウのサイズを変更したり、デバイスの向きを変更したりすることでWebページのレイアウトが変化するので、画像がサイズ変更された場合に、適切なレンディションが読み込まれて表示されるようにします。 ライブラリは画面上の画像サイズを継続的に監視し、新しいブレークポイント幅に達するたびにDynamic Mediaから新しい画像レンディションを取得します。

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
   <td colname="col2"> <p>次に、レスポンシブ画像がWebページの幅の50%を占めるコンテナ内にある簡単な例を示します。 ブラウザーウィンドウのサイズが変更されるたびに、コンテナの幅が変更されます。 画像の幅が設定済みのブレークポイントの1つに達すると（例えば、200、400、600、800ピクセルで設定）、新しいレンディションがダウンロードされて表示されます。 目的は、不要な大きな画像を読み込まず、ネットワーク帯域幅を節約することです。 </p> <p>URLをクリックして、Webページを開き、ブラウザーウィンドウのサイズを変更し、ネットワークトラフィックを監視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>次のBootstrapの例は、Webページでの同じ使用例を示しています。 BootstrapのCSSに従い、レスポンシブ画像が追加されるレイアウトセルは、次の幅のいずれかを取ることができます。360、720、940ピクセル。 これらの値は、レスポンシブ画像ライブラリにブレークポイントとして渡される値と同じです。 したがって、Dynamic Mediaは、クライアントのネットワーク帯域幅が有効に使用されるようにします。 また、現在のWebページのレイアウトで必要なサイズで画像が表示され、クライアント側のブラウザーが拡大/縮小される視覚的なアーティファクトは表示されません。 </p> <p>URLをクリックして、Webページを開き、ブラウザーウィンドウのサイズを変更して別のレイアウトのブレークポイントに到達し、ネットワークトラフィックを監視します。 </p> <p>より高度な使用例としては、異なる画像プリセット、画像サービングコマンド、またはその両方を異なるブレークポイント値に関連付ける場合などがあります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>次の例では、異なるブレークポイントサイズに対して異なる画質と形式の画像プリセットが使用されます。 小さなブレークポイントの場合は、低品質のプリセットが適用され、画像サービングは6色に圧縮されたGIF画像のみを返します。 中程度のブレークポイントは、高圧縮のJPEG用に設定された画像プリセットを使用します。 最大のブレークポイントは、可逆PNGを使用して高品質の画像プリセットに関連付けられます。 このような方法では、より大きな画面を持つデバイスの帯域幅と処理能力が大きいと仮定して、高品質の画像をこのようなデバイスに配信できます。 </p> <p>URLをクリックしてWebページを開き、Webブラウザーウィンドウのサイズを大きくして小さくし、画質が低下することに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>画像プリセットに加えて、特定の画像サービングコマンドをブレークポイントに関連付けることができます。 次の例は、画面上の画像サイズが小さくなるにつれて、バナー画像を対象領域に対して徐々に切り抜く方法を示しています。 ここでは、最大のブレークポイントには画像サービングコマンドがまったくないので、バナー画像が完全に表示されます。 中程度のブレークポイントでは、テキスト「実行中」のランナーのみを表示し、適度な切り抜きを適用します。 小さなブレークポイントでは、製品のみが表示されるように、より多くの切り抜きが適用されます。 </p> <p>URLをクリックして、Webページを開き、ブラウザーウィンドウのサイズを変更します。 画像が大きいサイズから小さいサイズに切り抜かれるにつれて、徐々に切り抜かれていく様子に注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>また、画像サービングコマンドと画像サービングテンプレートを使用して、画像サイズに基づいて特定のテンプレートパラメーターを制御することもできます。 次の例では、画像サービングテンプレートを使用し、テキストオーバーレイのフォントサイズが<span class="codeph"> $fontsize </span>パラメーターを使用してパラメーター化されます。 レスポンシブ画像は、テキストが常に読み取り可能な状態を保つために、画像サイズを小さくするために大きいフォントサイズを使用するように設定されています。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 必要システム構成 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**サーバのハードウェアとソフトウェア**

* Dynamic Media Image Serving 6.0.1以降。

**クライアントブラウザーの最小要件**

* Microsoft® Windows® 7以降macOS X 10.8以降。
* Firefox 23、Safari 6、Chrome 29、IE 9以降。
* iOS 6以降。
* iPhone3GS以降およびiPad2以降（ネイティブブラウザーのみ）で認定済み。
* Android™ OS 2.3以降。
* モバイルデバイス上のInternet Explorerは現在サポートされていません。
