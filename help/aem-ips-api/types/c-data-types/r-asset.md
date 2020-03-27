---
description: フォルダー階層内のオブジェクトまたはコンテナ。
seo-description: フォルダー階層内のオブジェクトまたはコンテナ。
seo-title: アセット
solution: Experience Manager
title: アセット
topic: Scene7 Image Production System API
uuid: 758ac593-98d8-4366-a723-a06435c7fd3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# アセット{#asset}

フォルダー階層内のオブジェクトまたはコンテナ。

構文

## パラメータ {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> animatedGifInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：AnimatedGifInfo</span> </td> 
   <td colname="col3"> アニメーションGIFファイルに関する詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> cabinet <span class="varname"> Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：CabinetInfo</span> </td> 
   <td colname="col3"> キャビネットアセットタイプのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 作成 <span class="varname"> 済</span> み </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> アセットがアップロードされた日時。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットを作成したユーザーの電子メールアドレス。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cssInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：CssInfo</span> </td> 
   <td colname="col3"> CSSファイルに関する詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> cuePointInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">仮想ファイル名を返します。 仮想ファイルの完全なパスは <span class="codeph"> folder</span>+<span class="codeph"> fileNameです</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> フォ <span class="varname"> ルダ</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットを含むフォルダ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットの親フォルダーを処理します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> フォントアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> iccProfileInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：IccProfileInfo</span> </td> 
   <td colname="col3"> ICCプロファイルアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustratorInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ImageInfo</span> </td> 
   <td colname="col3"> 画像アセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットのサムネールビューを表す相対URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：JavaScriptInfo</span> </td> 
   <td colname="col3"> JavaScriptファイルに関する詳細。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 終変更</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> アセットが最後に変更された日時。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットを最後に変更したユーザーの電子メールアドレス。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：LayerViewInfo</span> </td> 
   <td colname="col3"> レイヤービューアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maskInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> masterVideoInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 型：MetadataArray</span> </td> 
   <td colname="col3"> アセットに関連付けられているメタデータ値の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセット名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdfSettingsInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF設定アセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 権 <span class="varname"> 限</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> postScriptInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> powerPointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> プロジ <span class="varname"> ェクト</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> プロジェクト名のリスト。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psdInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> アセットを発行するかどうかを示すフラグを設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> renderSceneInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：RenderSceneInfo</span> </td> 
   <td colname="col3"> レンダリングシーンアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">サブタイプの値(AssetSetなど <span class="codeph"></span>)をサポートする汎用アセットサブタイプ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svgInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：SvgInfo</span> </td> 
   <td colname="col3"> SVGアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：SwcInfo</span> </td> 
   <td colname="col3"> SWCアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> templateInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：TemplateInfo</span> </td> 
   <td colname="col3"> テンプレートアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ごみ <span class="varname"> 箱状</span> 態 </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> アセットがごみ箱内にあるか、ライブにあるかを示します（値については、「ごみ箱の状態」を参照）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">アセットタイプ. 値については <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> 、Asset Types</a> （アセットタイプ）を参照してください。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> videoCaptionInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>ビデオキャプションアセットのプロパティ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> <p>ビデオアセットのプロパティ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerPresetInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ViewerPresetInfo</span> </td> 
   <td colname="col3"> ビューアプリセットアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> viewerSwfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：ViewerSwfInfo</span> </td> 
   <td colname="col3"> ビューアSWfアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> vignetteInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 種類：VignetteInfo</span> </td> 
   <td colname="col3"> ビネットアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> watermarkInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：WatermarkInfo</span> </td> 
   <td colname="col3"> 透かしアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：WindowCoveringInfo</span> </td> 
   <td colname="col3"> アセットをカバーするウィンドウのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：XmlInfo</span> </td> 
   <td colname="col3"> XMLアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xsl Info</span></span> </td> 
   <td colname="col2"> <span class="codeph"> タイプ：XslInfo</span> </td> 
   <td colname="col3"> XSLアセットのプロパティ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

