---
description: ビネット用の新しい公開形式を作成します。
seo-description: ビネット用の新しい公開形式を作成します。
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createVignettePublishFormat{#createvignettepublishformat}

ビネット用の新しい公開形式を作成します。

ビネット形式は、公開されたビネットとそのサムネールのサイズ、ズームレベル、シャープのパラメータ、およびIPSから画像レンダリングサーバに公開されたマスタービネットから生成されたビネットのファイル形式のバージョンを指定します。

新しいバージョンのImage Rendering Serverでは、ピラミッドビネットがサポートされるので、パブリッシュ用に特定のビネット形式のサイズを定義する必要がありません。

## 認証されたユーザータイプ {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-3a368186ec1d4005bca056fc9d9bacc7}

**入力(createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネットが属する会社の処理。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット公開形式を識別する名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>ビネットビューのターゲット幅をピクセル単位で指定します。 </p> <p>出力ビネットがマスタービネットと同じサイズになるように、ゼロを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像レンダリングサーバでのズーム処理に最適なピラミッドビネットを作成します。このオプションでは、1 つのビネット出力ファイルで複数サイズの表示を作成します。ターゲットビネットサイズフィールドで設定された最大サイズから作成を開始します。表示のサイズは、幅と高さが 128x128 ピクセル以内になるまで、1/2 ずつ縮小されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ピラミッド <span class="varname"> を作成</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 生成される各サムネールの幅をピクセル単位で指定します。この設定はオプションです。 サムネールファイルを作成しない場合は、ゼロのままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> thumbWidth <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 公開するビネットのファイル形式を指定します。 新しいバージョンのImage Authoringと古いバージョンのImage Rendering Serverを使用する場合は、ImageRendering Serverが読み取ることのできるビネットバージョンを指定する必要があります。 より新しいバージョンを指定した場合、Image Rendering Serverは公開されたビネットを読み取れません。 最新バージョンでビネットを公開するには、0に設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> saveAsVersion <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名と幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> sizeSuffixSeparator <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名と幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> シャ <span class="varname"> ープ</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 各画像ビネットサイズに対してメインビュー画像にシャープを適用します。シャープを適用すると、ビネットを拡大・縮小したときにぼかしが補正されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> デジタルアンシャープマスクは、特にスキャンされた画像のシャープを高める柔軟で強力な方法です。 各オーバーシュートの大きさ（エッジの境界線がどの程度暗く、明るくなるか）を制御します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 拡大するエッジのサイズやエッジの縁の幅に影響を与えるので、小さいラジウムを使用すると、小さいスケールの細部が強調されます。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かいディテールは、同じサイズの小さなディテールまたは半径より小さなディテールが失われるので、小さな半径が必要です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span></span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> シャープを適用する明るさの最小値や、隣接する階調値の間隔を指定してフィルターを機能させるかどうかを制御します。 この設定により、より細かいエッジを残したまま、より回転するエッジにシャープを適用できます。 しきい値の許容範囲は0 ～ 255です。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(createVignettePublishFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | はい | 作成したビネット形式のハンドル。 |

## 例 {#section-0564752d439642b9bb8de2903db6de1e}

このコードは、ビネット公開形式を作成します。 作成リクエストでは、名前、ターゲットの幅と高さ、およびその他の必須の値を指定します。

**リクエスト**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**応答**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

