---
description: これらのコマンドは、リクエストのどこに表示されるかに関係なく適用されます。
seo-description: これらのコマンドは、リクエストのどこに表示されるかに関係なく適用されます。
seo-title: 要求コマンド
solution: Experience Manager
title: 要求コマンド
topic: Scene7 Image Serving - Image Rendering API
uuid: 5566bbcd-baf8-4003-b61d-df4e414df781
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 要求コマンド{#request-commands}

これらのコマンドは、リクエストのどこに表示されるかに関係なく適用されます。

<table id="simpletable_3F7C17FB9E374EFDAD01EB24F57EC367"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> キャッシュ</a> </p></td> 
  <td class="stentry"> <p>デフォルトの応答キャッシュ動作を上書きします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2" type="reference" format="dita" scope="local"> defaultImage</a> </p></td> 
  <td class="stentry"> <p>見つからない画像ファイルの代わりに使用する画像を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt</a> </p></td> 
  <td class="stentry"> <p>画像形式を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517" type="reference" format="dita" scope="local"> icc</a> </p></td> 
  <td class="stentry"> <p>出力カラープロファイルを設定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> iccEmbed</a> </p> </td> 
  <td class="stentry"> <p>返信画像にカラープロファイルを埋め込みます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed</a> </p></td> 
  <td class="stentry"> <p>返信画像にPhotoshopのパスデータを埋め込みます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed</a> </p></td> 
  <td class="stentry"> <p>返信画像にXMPメタデータを埋め込みます。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491" type="reference" format="dita" scope="local"> printRes</a> </p> </td> 
  <td class="stentry"> <p>返信画像に埋め込む印刷解像度の値を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt</a> </p></td> 
  <td class="stentry"> <p>JPEGエンコーディング属性を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38" type="reference" format="dita" scope="local"> 量子化する</a> </p> </td> 
  <td class="stentry"> <p>GIF出力のカラー量子化属性を指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req</a> </p></td> 
  <td class="stentry"> <p>リクエストの種類を選択します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md#reference-29a398cc59dc4caf9acd5f69c9ba9715" type="reference" format="dita" scope="local"> resMode</a> </p></td> 
  <td class="stentry"> <p>画像の再サンプリングまたは補間モードを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14" type="reference" format="dita" scope="local"> テンプレート</a> </p> </td> 
  <td class="stentry"> <p>合成テンプレートを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb" type="reference" format="dita" scope="local"> locale</a> </p></td> 
  <td class="stentry"> <p>合成テンプレートを指定します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id</a> </p> </td> 
  <td class="stentry"> <p>画像/メタデータのバージョンID。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3" type="reference" format="dita" scope="local"> imageSet</a> </p> </td> 
  <td class="stentry"> <p>この要求に使用する画像セットを指定します。 </p></td> 
 </tr> 
</table>

