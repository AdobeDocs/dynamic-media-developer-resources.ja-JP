---
description: 周辺光量補正の新しい公開形式を作成します。
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
TQID: 'https://experienceleague.adobe.com/7oPPVCLGAntgI4uJXmpUJjKiOIDIKGiVRjdIvXWxVDo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 520
ht-degree: 4%

---

# createVignettePublishFormat{#createvignettepublishformat}

周辺光量補正の新しい公開形式を作成します。

周辺光量補正フォーマットは、公開された周辺光量補正とそのサムネールのサイズ、ズームレベル、シャープニングパラメーター、およびIPSから画像レンダリングサーバーに公開された主要な周辺光量補正から生成された周辺光量補正のファイルフォーマットバージョンを指定します。

新しいバージョンの画像レンダリング サーバーでは、ピラミッドビネットをサポートできるため、公開用に特定のビネット形式サイズを定義する必要がありません。

## 承認済みユーザータイプ {#section-f5c563e3695c4dba8df41e2a965aace7}

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
   <td colname="col4"> ビネットが属する会社に対応します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット公開形式を識別する名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> <p>結果の周辺光量補正ビューのターゲット幅をピクセル単位で指定します。 </p> <p>出力ビネットがプライマリビネットと同じサイズになるように、ゼロを使用します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 画像レンダリングサーバーでのズーム用に最適化されたピラミッドの周辺光量補正を作成します。 「ターゲット周辺光量補正サイズ」フィールドで設定された最大サイズから開始すると、単一の周辺光量出力ファイルに複数のサイズ表示が作成されます。 後続の各ビューサイズは、幅と高さが128 x 128 ピクセル以内になるまで半分になります。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成される各サムネールの幅をピクセル単位で指定します。 この設定はオプションです。 サムネールファイルがない場合は0のままにします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> パブリッシュしたビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングと古いバージョンの画像レンダリングサーバーでは、ImageRendering Serverが読み取れる周辺光量補正バージョンを指定する必要があります。 より高いバージョンを指定した場合、画像レンダリングサーバーは公開されたビネットを読み取ることができません。 最新バージョンでビネットを公開するには、0に設定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名とその幅を示す接尾辞を区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> ビネット名とその幅を示す接尾辞を区切る文字を指定します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> シャープ </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 明るいビネットサイズごとにメインビュー画像にシャープを適用します。シャープを適用すると、ビネッタが拡大・縮小されたときにぼやけを補正できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> デジタルアンシャープマスクは、特にスキャンした画像でシャープを増やすための柔軟で強力な方法です。 これにより、各オーバーシュートの大きさ（エッジの境界線がどれだけ暗く、明るくなるか）が制御されます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 強化するエッジのサイズやエッジ リムの幅に影響を与えるため、小さいラジウムは小さいスケールのディテールを強調します。 半径の値を大きくすると、エッジでハローが発生する可能性があります。 同じサイズの小さいディテールや、半径よりも小さいディテールが失われるので、細かいディテールには半径を小さくする必要があります。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> コードフレーズ </span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> シャープにする最小の明るさの変化や、フィルターを使用する前に隣接する階調値をどの程度離す必要があるかを制御します。 この設定を使用すると、より繊細なエッジを残したまま、より目立つエッジをシャープにすることができます。 しきい値の許容範囲は0 ～ 255です。 </td> 
  </tr> 
 </tbody> 
</table>

**出力（createVignettePublishFormatReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | はい | 作成したビネット形式へのハンドル。 |

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

