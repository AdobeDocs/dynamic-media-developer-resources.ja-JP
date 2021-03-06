---
description: ビネット用の新しい公開形式を作成します。
solution: Experience Manager
title: createVignetPublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 14%

---

# createVignetPublishFormat{#createvignettepublishformat}

ビネット用の新しい公開形式を作成します。

ビネット形式は、公開済みビネットとそのサムネールのサイズ、ズームレベル、シャープパラメータ、IPS から Image Rendering Server に公開されたプライマリビネットから作成されたビネットのファイル形式バージョンを指定します。

新しい Image Rendering Server バージョンでは、ピラミッドビネットをサポートできるので、公開用に特定のビネット形式のサイズを定義する必要がなくなりました。

## 認証済みユーザータイプ {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-3a368186ec1d4005bca056fc9d9bacc7}

**入力 (createVignettePublishFormatParam)**

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
   <td colname="col4"> ビネットが属する会社を処理します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名前</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット公開形式を識別する名前です。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>生成されるビネット表示のターゲット幅をピクセル単位で指定します。 </p> <p>出力ビネットのサイズがプライマリビネットと同じになるように、ゼロを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像レンダリングサーバでのズーム処理に最適なピラミッドビネットを作成します。このオプションでは、1 つのビネット出力ファイルで複数サイズの表示を作成します。ターゲットビネットサイズフィールドで設定された最大サイズから作成を開始します。表示のサイズは、幅と高さが 128x128 ピクセル以内になるまで、1/2 ずつ縮小されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 生成される各サムネールの幅をピクセル単位で指定します。この設定はオプションです。 サムネールファイルを使用しない場合はゼロのままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 公開したビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングと古いバージョンの画像レンダリングサーバーを指定する場合、ImageRendering Server が読み取ることのできるビネットバージョンを指定する必要があります。 より高いバージョンを指定した場合、画像レンダリングサーバは公開済みビネットを読み取れません。 最新バージョンのビネットを公開するには、0 に設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名と幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名と幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 鋭くする</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> メイン表示画像に対してシャープを適用し、各画像サイズに対してシャープを適用します。シャープを適用すると、ビネッターを拡大・縮小したときにぼかしを補正できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> デジタルアンシャープマスクは、特にスキャンされた画像でシャープネスを高める柔軟で強力な方法です。 これは、各オーバーシュートの大きさ（エッジ境界がどれだけ暗く、ライトになるか）を制御します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 拡張するエッジのサイズやエッジリムの幅に影響を与えます。したがって、小さいラジウムは小さいスケールの詳細を高めます。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かい詳細は、同じサイズの小さな詳細と同じか、半径より小さい細かい詳細が失われるので、小さい半径を必要とします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> シャープにする最小の明るさの変化、または隣接する階調値の間隔を、フィルターが機能する前にどの程度制御します。 この設定により、より回転するエッジをよりシャープにし、より繊細なエッジは手を付けずに残すことができます。 しきい値の許容範囲は 0～255 です。 </td> 
  </tr> 
 </tbody> 
</table>

**出力 (createVignettePublishFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetFormatHandle | `xsd:string` | はい | 作成したビネット形式のハンドル。 |

## 例 {#section-0564752d439642b9bb8de2903db6de1e}

このコードはビネット公開形式を作成します。 作成リクエストでは、名前、ターゲットの幅と高さ、およびその他の必須値を指定します。

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
