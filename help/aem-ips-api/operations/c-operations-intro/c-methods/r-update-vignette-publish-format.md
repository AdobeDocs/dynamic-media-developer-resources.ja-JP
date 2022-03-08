---
description: ビネット公開形式の設定を更新します。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 20%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

ビネット公開形式の設定を更新します。

## 認証済みユーザータイプ {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-8c7ba8d2bce14071b21fccb11f44749f}

**入力 (updateVignetPublishFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| vignetFormatHandle | `xsd:string` | はい | 公開形式ハンドル。 |
| name | `xsd:string` | いいえ | 公開形式名。 |
| targetWidth | `xsd:int` | はい | 生成されるビネット表示のターゲット幅をピクセル単位で指定します。 出力ビネットのサイズがプライマリビネットと同じになるように、ゼロを使用します。 |
| targetHeight | `xsd:int` | はい | 生成されるビネット表示のターゲットの高さをピクセル単位で指定します。 出力ビネットのサイズがプライマリビネットと同じになるように、ゼロを使用します。 |
| createPyramid | `xsd:boolean` | はい | 画像レンダリングサーバでのズーム処理に最適なピラミッドビネットを作成します。このオプションでは、1 つのビネット出力ファイルで複数サイズの表示を作成します。ターゲットビネットサイズフィールドで設定された最大サイズから作成を開始します。表示のサイズは、幅と高さが 128x128 ピクセル以内になるまで、1/2 ずつ縮小されます。 |
| thumbWidth | `xsd:int` | はい | 生成される各サムネールの幅をピクセル単位で指定します。この設定はオプションです。 サムネールファイルを使用しない場合はゼロのままにします。 |
| saveAsVersion | `xsd:int` | はい | 公開したビネットのファイル形式を指定します。 Image Authoring の新しいバージョンと Image Rendering Server の古いバージョンを指定する場合は、ImageRendering Server が読み取ることのできるビネットバージョンを指定する必要があります。 より高いバージョンを指定した場合、画像レンダリングサーバは公開済みビネットを読み取れません。 最新バージョンのビネットを公開するには、0 に設定します。 |
| sizeSuffixSeparator | `xsd:string` | はい | ビネット名と幅を示すサフィックスを区切る文字を指定します。 |
| 鋭くする | `xsd:int` | いいえ | 各公開ビネットサイズのメイン表示画像にシャープを適用します。シャープにより、ビネットを拡大・縮小したときにぼかしを補正できます。 |
| usmAmount | `xsd:double` | はい | デジタルアンシャープマスクは、特にスキャンされた画像でシャープネスを高める柔軟で強力な方法です。 これは、各オーバーシュートの大きさ（エッジ境界がどれだけ暗く、より明るくなるか）を制御します。 |
| usmRadius | `xsd:double` | はい | 拡大するエッジのサイズやエッジリムの幅に影響を与えるので、半径を小さくすると、より小さいスケールの詳細が向上します。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かい詳細は、同じサイズの小さな詳細と同じか、半径より小さい細かい詳細が失われるので、小さい半径を必要とします。 |
| usmThreshold | `xsd:int` | はい | シャープにする最小の明るさの変化、または隣接する階調値の間隔を、フィルターが機能する前にどの程度制御します。 この設定により、より回転するエッジをよりシャープにし、より繊細なエッジは手を付けずに残すことができます。 しきい値の許容範囲は 0～255 です。 |

**出力 (updateVignettePublishFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetFormatHandle | `xsd:string` | はい | 更新されたビネット公開形式を処理します。 |

## 例 {#section-fcba4bf2b7264786a676e315a35dbe43}

このコードサンプルは、ビネット公開形式を更新し、ハンドルを更新された形式に返します。

**リクエスト**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**応答**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
