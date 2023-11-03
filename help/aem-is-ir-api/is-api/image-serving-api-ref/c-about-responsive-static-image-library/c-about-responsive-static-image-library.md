---
description: レスポンシブ画像ライブラリは、Dynamic Mediaから提供され、レスポンシブ Web ページに埋め込まれる画像の品質を動的に調整する JavaScript モジュールです。 また、高密度の画面を持つデバイスでの画質も向上します。 また、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。
solution: Experience Manager
title: レスポンシブ画像ライブラリについて
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# レスポンシブ画像ライブラリについて{#about-responsive-image-library}

レスポンシブ画像ライブラリは、Dynamic Mediaから提供され、レスポンシブ Web ページに埋め込まれる画像の品質を動的に調整する JavaScript モジュールです。 また、高密度の画面を持つデバイスでの画質も向上します。 また、スマート切り抜きとスマートスウォッチからの結果を応答的にレンダリングすることもできます。

## デモ URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

レスポンシブ画像ライブラリの最も簡単な使用例は、画像の幅のブレークポイント値のリストを定義することです。 このリストを使用すると、ユーザーがブラウザーウィンドウのサイズを変更したり、デバイスの向きを変更したりして Web ページのレイアウトが変わるので、画像がサイズ変更された場合に、適切なレンディションが読み込まれて表示されます。 ライブラリは画面上の画像サイズを継続的に監視し、新しいブレークポイントの幅に達するたびに、Dynamic Mediaから新しい画像レンディションを取得します。

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>デモ URL </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>次に、レスポンシブ画像が Web ページの幅の 50%を占めるコンテナ内にある簡単な例を示します。 ブラウザーウィンドウのサイズが変更されるたびに、コンテナの幅が変更されます。 画像の幅が、説明のために 200、400、600 および 800 ピクセルで設定された設定済みのブレークポイントのいずれかに達すると、新しいレンディションがダウンロードされて表示されます。 目標は、不要な大きな画像を読み込まず、ネットワーク帯域幅を節約することです。 </p> <p>URL をクリックして、Web ページを開き、ブラウザーウィンドウのサイズを変更し、ネットワークトラフィックを監視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>次のBootstrapの例は、Web ページでの同じ使用例を示しています。 BootstrapCSS に従って、レスポンシブ画像が追加されるレイアウトセルは、幅 360、720、940 ピクセルのいずれかを取ることができます。 これらの値は、レスポンシブ画像ライブラリにブレークポイントとして渡される値とまったく同じです。 したがって、Dynamic Mediaは、クライアントのネットワーク帯域幅が効果的に使用されるようにします。 また、現在の Web ページのレイアウトを考慮すると、画像は必要なサイズで表示され、クライアント側のブラウザーを拡大縮小する視覚的なアーティファクトは一切含まれません。 </p> <p>URL をクリックして、Web ページを開き、ブラウザーウィンドウのサイズを変更して別のレイアウトのブレークポイントに到達し、ネットワークトラフィックを監視できます。 </p> <p>より高度な使用例としては、異なる画像プリセットや画像サービングコマンドの関連付け、またはその両方を異なるブレークポイント値に関連付ける場合などがあります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>次の例では、異なるブレークポイントサイズの異なる画質と形式の画像プリセットが使用されます。 小さなブレークポイントの場合は、低品質のプリセットが適用され、画像サービングは圧縮されたGIF画像を 6 色のみに返すように強制されます。 メディアのブレークポイントは、高圧縮のJPEG用に設定された画像プリセットを使用します。 最大のブレークポイントは、可逆圧縮 PNG を使用した高品質の画像プリセットに関連付けられます。 このような方法では、大きな画面を持つデバイスの帯域幅と処理能力が大きいという前提に基づいて、高品質の画像をこのようなデバイスに配信できます。 </p> <p>URL をクリックして Web ページを開き、Web ブラウザーウィンドウのサイズを大きくして小さくし、画質の低下に注目します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>画像プリセットに加えて、特定の画像サービングコマンドをブレークポイントに関連付けることができます。 次の例は、画面上の画像サイズが小さくなるにつれて、バナー画像を対象領域に対して徐々に切り抜く方法を示しています。 ここでは、最大のブレークポイントには画像サービングコマンドがまったくないので、バナー画像は完全に表示されます。 中程度のブレークポイントでは、中程度の切り抜きが適用され、「実行中」というテキストを含むランナーのみが表示されます。 小さなブレークポイントでは、より多くの切り抜きが適用され、製品のみが表示されます。 </p> <p>URL をクリックして、Web ページを開き、ブラウザーウィンドウのサイズを変更します。 画像が大きいサイズから小さいサイズに切り抜かれるにつれて、徐々に切り抜かれていく様子に注目してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>画像サービングテンプレートと共に画像サービングコマンドを使用して、画像サイズに基づいて特定のテンプレートパラメーターを制御することもできます。 次の例では、画像サービングテンプレートを使用し、テキストオーバーレイのフォントサイズが <span class="codeph"> $fontsize </span> パラメーター。 レスポンシブ画像は、画像サイズを小さくするために大きいフォントサイズを使用するように設定されており、テキストが常に読み取り可能なままになります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 必要システム構成 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**サーバのハードウェアとソフトウェア**

* Dynamic Media Image Serving 6.0.1 以降。

**クライアントブラウザーの最小要件**

* Microsoft® Windows® 7 以降、macOS X 10.8 以降。
* Firefox 23、Safari 6、Chrome 29、IE 9 以降。
* iOS 6 以降。
* iPhone3GS 以降およびiPad2 以降（ネイティブブラウザーのみ）で認定済み。
* Android™ OS 2.3 以降。
* モバイルデバイス上の Internet Explorer は、現在サポートされていません。
