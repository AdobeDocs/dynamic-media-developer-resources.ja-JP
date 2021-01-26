---
description: ビネット用の新しい公開形式を作成します。
seo-description: ビネット用の新しい公開形式を作成します。
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 14%

---


# createVignettePublishFormat{#createvignettepublishformat}

ビネット用の新しい公開形式を作成します。

ビネット形式は、公開されるビネットとそのサムネールのサイズ、ズームレベル、シャープパラメータ、IPSからImage Rendering Serverに公開されるプライマリビネットから生成されるビネットのファイル形式のバージョンを指定します。

新しいバージョンのImage Rendering Serverでは、ピラミッドビネットをサポートできるので、公開用に特定のビネット形式サイズを定義する必要がありません。

## 認証済みユーザータイプ{#section-f5c563e3695c4dba8df41e2a965aace7}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネットが属する会社のハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット公開形式を識別する名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>生成されるビネット表示のターゲット幅をピクセル単位で指定します。 </p> <p>ゼロを指定すると、出力ビネットはプライマリビネットと同じサイズになります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像レンダリングサーバでのズーム処理に最適なピラミッドビネットを作成します。このオプションでは、1 つのビネット出力ファイルで複数サイズの表示を作成します。ターゲットビネットサイズフィールドで設定された最大サイズから作成を開始します。表示のサイズは、幅と高さが 128x128 ピクセル以内になるまで、1/2 ずつ縮小されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 生成される各サムネールの幅をピクセル単位で指定します。この設定はオプションです。 サムネールファイルを作成しない場合は、ゼロのままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 公開するビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングとそれより古いバージョンの画像レンダリングサーバを指定する場合は、ImageRendering Serverが読み取ることのできるビネットバージョンを指定する必要があります。 より新しいバージョンを指定した場合、Image Rendering Serverは公開されたビネットを読み取れません。 最新バージョンでビネットを公開するには、ゼロに設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名とその幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名とその幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> シャープ</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 各公開ビネットサイズに対してメイン表示画像にシャープを適用します。シャープは、ビネッタを拡大・縮小したときにぼやけを補正できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> デジタルアンシャープマスクは、特にスキャン画像でシャープさを高める柔軟で強力な方法です。 これにより、各オーバーシュートの大きさ（エッジの境界線の暗さと明るさ）が制御されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 拡張するエッジのサイズやエッジの縁の幅に影響を与えるので、半径を小さくすると、より小さなスケールのディテールが向上します。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かいディテールは、同じサイズの小さいまたは半径より小さい細かいディテールが失われるので、小さい半径が必要です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ  </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> シャープを適用する明るさの最小値、またはフィルターが機能する前に隣接する階調値の間隔を制御します。 この設定により、より細かいエッジにシャープを適用し、より細かいエッジに手を加えないようにできます。 しきい値の許容範囲は0 ～ 255です。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(createVignettePublishFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | はい | 作成したビネット形式のハンドル。 |

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

