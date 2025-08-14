---
description: ビネット公開形式設定を更新します。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

ビネット公開形式設定を更新します。

## 許可されているユーザータイプ {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-8c7ba8d2bce14071b21fccb11f44749f}

**入力（updateVignettePublishFormatParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社ハンドル。 |
| vignetteFormatHandle | `xsd:string` | はい | 公開形式ハンドル。 |
| name | `xsd:string` | いいえ | 公開形式名。 |
| targetWidth | `xsd:int` | はい | 生成されるビネットビューのターゲット幅をピクセル単位で指定します。 出力ビネットがプライマリ ビネットと同じサイズになるように、ゼロを使用します。 |
| targetHeight | `xsd:int` | はい | 結果のビネットビューのターゲットの高さをピクセル単位で指定します。 出力ビネットがプライマリ ビネットと同じサイズになるように、ゼロを使用します。 |
| createPyramid | `xsd:boolean` | はい | イメージ レンダリング サーバでズーム用に最適化されたピラミッド ビネットを作成します。 [ ターゲット ビネット サイズ ] フィールドで設定した最大サイズから始めて、1 つのビネット出力ファイルに複数のサイズ ビューを作成します。 その後の各表示サイズは、幅と高さが 128 x 128 ピクセル以内になるまで半分になります。 |
| thumbWidth | `xsd:int` | はい | 生成される各サムネールの幅をピクセル単位で指定します。 この設定はオプションです。 サムネールファイルがない場合は 0 のままにします。 |
| saveAsVersion | `xsd:int` | はい | 公開するビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングと古いバージョンの画像レンダリングサーバーを指定する場合、画像レンダリングサーバーが読み取れるビネットバージョンを指定する必要があります。 新しいバージョンを指定すると、イメージ レンダリング サーバは公開されたビネットを読み取ることができません。 最新バージョンでビネットを公開するには、ゼロに設定します。 |
| sizeSuffixSeparator | `xsd:string` | はい | ビネット名と、その幅を示すサフィックスを区切る文字を指定します。 |
| シャープ | `xsd:int` | いいえ | 各パブリッシュビネットサイズのメイン表示画像にシャープニングを適用します。 シャープにより、ビネットのスケール時のぼかしを補うことができます。 |
| usmAmount | `xsd:double` | はい | デジタルアンシャープマスクは、特にスキャンされた画像のシャープネスを高める柔軟かつ強力な方法です。 これにより、各オーバーシュートの大きさ（エッジの境界の暗さと明るさが増す度合い）が制御されます。 |
| usmRadius | `xsd:double` | はい | 拡張するエッジのサイズやエッジのリムの幅に影響します。半径を小さくすると、詳細のスケールが小さくなります。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かいディテールには、同じサイズの小さなディテールが失われたり、半径よりも小さなディテールが失われたりするため、半径を小さくする必要があります。 |
| usmThreshold | `xsd:int` | はい | シャープにする輝度の変化の最小値や、隣接する階調値の間隔を、フィルターが機能する前に制御します。 この設定を使用すると、より繊細なエッジを残しながら、より多くの発音されたエッジをシャープにすることができます。 しきい値の許容範囲は 0 ～ 255 です。 |

**出力（updateVignettePublishFormatReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | はい | 更新されたビネット公開形式へのハンドル。 |

## 例 {#section-fcba4bf2b7264786a676e315a35dbe43}

このコード例では、ビネット公開形式を更新し、更新された形式へのハンドルを返します。

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
