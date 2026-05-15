---
description: ビネットのパブリッシュ形式設定を更新します。
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
TQID: 'https://experienceleague.adobe.com/sarJBoGNUo5Prxa4NQyxwhYp-PEAIZ5VNUvcEAQrpG0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 5%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

ビネットのパブリッシュ形式設定を更新します。

## 承認済みユーザータイプ {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-8c7ba8d2bce14071b21fccb11f44749f}

**入力（updateVignettePublishFormatParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| vignetteFormatHandle | `xsd:string` | はい | 形式ハンドルを公開します。 |
| name | `xsd:string` | いいえ | 書式名を公開します。 |
| targetWidth | `xsd:int` | はい | 結果の周辺光量補正ビューのターゲット幅をピクセル単位で指定します。 出力ビネットがプライマリビネットと同じサイズになるように、ゼロを使用します。 |
| targetHeight | `xsd:int` | はい | 結果の周辺光量補正ビューの目標高さをピクセル単位で指定します。 出力ビネットがプライマリビネットと同じサイズになるように、ゼロを使用します。 |
| createPyramid | `xsd:boolean` | はい | 画像レンダリングサーバーでのズーム用に最適化されたピラミッドの周辺光量補正を作成します。 「ターゲット周辺光量補正サイズ」フィールドで設定された最大サイズから開始すると、単一の周辺光量出力ファイルに複数のサイズ表示が作成されます。 後続の各ビューサイズは、幅と高さが128 x 128 ピクセル以内になるまで半分になります。 |
| thumbWidth | `xsd:int` | はい | 作成される各サムネールの幅をピクセル単位で指定します。 この設定はオプションです。 サムネールファイルがない場合は0のままにします。 |
| saveAsVersion | `xsd:int` | はい | パブリッシュしたビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングと古いバージョンの画像レンダリングサーバーでは、ImageRendering Serverが読み取れる周辺光量補正バージョンを指定する必要があります。 より高いバージョンを指定した場合、画像レンダリングサーバーは公開されたビネットを読み取ることができません。 最新バージョンでビネットを公開するには、0に設定します。 |
| sizeSuffixSeparator | `xsd:string` | はい | ビネット名とその幅を示す接尾辞を区切る文字を指定します。 |
| シャープ | `xsd:int` | いいえ | パブリッシュ ビネット サイズごとに、メイン ビューの画像にシャープを適用します。 シャープを適用すると、周辺光量補正を行うことで、周辺光量補正を行うことができます。 |
| usmAmount | `xsd:double` | はい | デジタルアンシャープマスクは、特にスキャンした画像でシャープを増やすための柔軟で強力な方法です。 これにより、各オーバーシュートの大きさ（エッジの境界線がどれだけ暗く、明るくなるか）が制御されます。 |
| usmRadius | `xsd:double` | はい | 強化するエッジのサイズやエッジ リムの幅に影響を与えるので、半径を小さくするとスケールのディテールが小さくなります。 半径の値を大きくすると、エッジでハローが発生する可能性があります。 同じサイズの小さいディテールや、半径よりも小さいディテールが失われるので、細かいディテールには半径を小さくする必要があります。 |
| usmThreshold | `xsd:int` | はい | シャープにする最小の明るさの変化や、フィルターを使用する前に隣接する階調値をどの程度離す必要があるかを制御します。 この設定を使用すると、より繊細なエッジを残したまま、より目立つエッジをシャープにすることができます。 しきい値の許容範囲は0 ～ 255です。 |

**出力（updateVignettePublishFormatReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| vignetteFormatHandle | `xsd:string` | はい | 更新されたビネットのパブリッシュ形式に対応します。 |

## 例 {#section-fcba4bf2b7264786a676e315a35dbe43}

このコードサンプルは、ビネットのパブリッシュ形式を更新し、更新された形式にハンドルを返します。

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
