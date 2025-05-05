---
description: レスポンシブ画像ライブラリは、JavaScriptから提供され、レスポンシブ web ページに埋め込まれる画像の品質を動的に調整するDynamic Media モジュールです。 また、高密度画面を使用するデバイスの画質も向上します。 このライブラリは、スマート切り抜きとスマートスウォッチから結果をレスポンシブにレンダリングすることもできます。
solution: Experience Manager
title: レスポンシブ画像ライブラリについて
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# レスポンシブ画像ライブラリについて{#about-responsive-image-library}

レスポンシブ画像ライブラリは、JavaScriptから提供され、レスポンシブ web ページに埋め込まれる画像の品質を動的に調整するDynamic Media モジュールです。 また、高密度画面を使用するデバイスの画質も向上します。 このライブラリは、スマート切り抜きとスマートスウォッチから結果をレスポンシブにレンダリングすることもできます。

## デモ URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

レスポンシブ画像ライブラリの最も簡単なユースケースは、画像の幅のブレークポイント値のリストを定義することです。 このリストにより、ブラウザーウィンドウのサイズを変更したユーザーやデバイスの向きを変更したユーザーの web ページのレイアウト変更が原因で画像のサイズが変更された場合、適切なレンディションが読み込まれて表示されるようになります。 ライブラリは画面上の画像サイズを継続的にモニタリングし、新しいブレークポイントの幅に達するたびに、Dynamic Mediaから新しい画像レンディションを取得します。

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
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=ja" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=ja </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>次に、レスポンシブ画像が、web ページ幅の 50% を占めるコンテナ内にある簡単な例を示します。 ブラウザーウィンドウのサイズが変更されるたびに、コンテナの幅が変化します。 画像の幅が設定されたブレークポイントの 1 つに達すると（例として、200、400、600、800 ピクセルに設定されている）、新しいレンディションがダウンロードされ、表示されます。 目標は、不要な大きな画像の読み込みを回避し、ネットワーク帯域幅を節約することです。 </p> <p>URL をクリックして web ページを開き、ブラウザーウィンドウのサイズを変更し、ネットワークトラフィックを監視します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=ja" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=ja </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>次のBootstrapの例は、web ページにおける同じユースケースを示しています。 BootstrapCSS によれば、レスポンシブ画像が追加されるレイアウトセルは、360、720、940 ピクセルのいずれかの幅を取ります。 これらの値は、まさに、ブレークポイントとしてレスポンシブ画像ライブラリに渡される値です。 そのため、Dynamic Mediaでは、クライアントのネットワーク帯域幅が効果的に使用されます。 また、クライアントサイドのブラウザーの拡大縮小による視覚的なアーティファクトを生じさせることなく、現在の web ページのレイアウトで必要とされる正確なサイズで画像が表示されます。 </p> <p>URL をクリックして web ページを開き、異なるレイアウトブレークポイントに合わせてブラウザーウィンドウのサイズを変更し、ネットワークトラフィックを監視します。 </p> <p>より高度な事例としては、異なる画像プリセット、画像サービングコマンドまたはその両方を、異なるブレークポイント値に関連付ける場合などがあります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=ja" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=ja</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>次の例では、異なるブレークポイントサイズに対して、異なる画質と形式の画像プリセットを使用します。 小さなブレークポイントには、画質の低いプリセットが適用され、画像サービングで、GIFの画像が 6 色のみに圧縮されて返されます。 中程度のブレークポイントは、高圧縮でJPEGするように設定された画像プリセットを使用しています。 最大のブレークポイントは、可逆圧縮 PNG を使用した高品質の画像プリセットに関連付けられます。 このような方法では、画面が大きいデバイスほど帯域幅と処理能力が大きいという前提に基づいて、高品質の画像がそのようなデバイスに配信されます。 </p> <p>URL をクリックして web ページを開き、web ブラウザーウィンドウのサイズを大きくから小さくし、画質の低下に注意します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=ja" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=ja </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>画像プリセットに加えて、特定の画像サービングコマンドをブレークポイントに関連付けることができます。 次の例では、画面の画像サイズが小さくなるにつれて、バナー画像を対象の領域まで徐々に切り抜く方法を示しています。 ここで、最大のブレークポイントには画像サービングコマンドがまったく含まれていないので、バナー画像が完全に表示されます。 中程度のブレークポイントでは、中程度の切り抜きが適用され、「実行中」というテキストを含むランナーのみが表示されます。 小さなブレークポイントでは、製品のみが表示されるように、より多くの切り抜きが適用されます。 </p> <p>URL をクリックして web ページを開き、ブラウザーウィンドウのサイズを変更します。 大きいサイズから小さいサイズに変更するにつれて、画像が徐々にトリミングされていることに注意してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=ja" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=ja </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>また、画像サービングコマンドを画像サービングテンプレートと共に使用して、画像サイズに基づいて特定のテンプレートパラメーターを制御することもできます。 次の例では、画像サービングテンプレートを使用し、$fontsize </span> パラメーターを使用してテキストオーバーレイのフォントサイズ <span class="codeph"> パラメーター化します。 レスポンシブ画像は、テキストが常に読みやすくなるように、小さい画像サイズに対して大きいフォントサイズを使用するように設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 必要システム構成 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**サーバのハードウェアとソフトウェア**

* Dynamic Media画像サービング 6.0.1 以降。

**クライアントブラウザーの最小要件**

* Microsoft® Windows® 7 以降、macOS X 10.8 以降。
* Firefox 23、Safari 6、Chrome 29、IE 9 以降。
* iOS 6 以降。
* iPhone3GS 以降およびiPad2 以降（ネイティブブラウザーのみ）で認定済み。
* Android™ OS 2.3 以降。
* モバイル デバイスの Internet Explorer は現在サポートされていません。
