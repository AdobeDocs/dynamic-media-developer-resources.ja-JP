---
description: ビネットの新しい公開形式を作成します。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 4%

---

# createVignettePublishFormat{#createvignettepublishformat}

ビネットの新しい公開形式を作成します。

ビネット形式は、公開するビネットとそのサムネールのサイズ、ズームレベル、シャープニングパラメーター、IPS から画像レンダリングサーバーに公開したプライマリビネットから生成されるビネットのファイルフォーマットバージョンを指定します。

新しいバージョンの Image Rendering Server では、ピラミッド ビネットをサポートできるため、公開用に特定のビネット形式サイズを定義する必要がなくなります。

## 許可されているユーザータイプ {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-3a368186ec1d4005bca056fc9d9bacc7}

**入力（createVignettePublishFormatParam）**

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
   <td colname="col4"> ビネットが所属する会社のハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> の名前 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット公開形式を識別する名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>生成されるビネットビューのターゲット幅をピクセル単位で指定します。 </p> <p>出力ビネットがプライマリ ビネットと同じサイズになるように、ゼロを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> イメージ レンダリング サーバでズーム用に最適化されたピラミッド ビネットを作成します。 [ ターゲット ビネット サイズ ] フィールドで設定した最大サイズから始めて、1 つのビネット出力ファイルに複数のサイズ ビューを作成します。 その後の各表示サイズは、幅と高さが 128 x 128 ピクセル以内になるまで半分になります。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 生成される各サムネールの幅をピクセル単位で指定します。 この設定はオプションです。 サムネールファイルがない場合は 0 のままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 公開するビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングと古いバージョンの画像レンダリングサーバーを指定する場合、ImageRendering サーバーが読み取れるビネットバージョンを指定する必要があります。 新しいバージョンを指定すると、イメージ レンダリング サーバは公開されたビネットを読み取ることができません。 最新バージョンでビネットを公開するには、ゼロに設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名と、その幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名と、その幅を示すサフィックスを区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sharpen</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 各パブリッシュビネットサイズのメインビュー画像にシャープニングを適用しますシャープニングは、ビネットサイズの拡大時のぼかしを補うことができます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> デジタルアンシャープマスクは、特にスキャンされた画像のシャープネスを高める柔軟かつ強力な方法です。 これは、各オーバーシュートの大きさ（エッジの境界が暗くなり、明るくなるほど）を制御します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 拡張するエッジのサイズやエッジのリムの幅に影響を与えるため、ラジウムを小さくすると、スケールの小さいディテールが強調されます。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かいディテールには、同じサイズの小さなディテールが失われたり、半径よりも小さなディテールが失われたりするため、半径を小さくする必要があります。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> のコードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> シャープにする輝度の変化の最小値や、隣接する階調値の間隔を、フィルターが機能する前に制御します。 この設定を使用すると、より繊細なエッジを残しながら、より多くの発音されたエッジをシャープにすることができます。 しきい値の許容範囲は 0 ～ 255 です。 </td> 
  </tr> 
 </tbody> 
</table>

**出力（createVignettePublishFormatReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | はい | 作成されたビネット形式へのハンドル。 |

## 例 {#section-0564752d439642b9bb8de2903db6de1e}

このコードは、ビネット公開形式を作成します。 作成リクエストでは、名前、ターゲットの幅と高さ、およびその他の必要な値を指定します。

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
