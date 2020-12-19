---
description: ビネット公開形式の設定を更新します。
seo-description: ビネット公開形式の設定を更新します。
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 20%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

ビネット公開形式の設定を更新します。

## 認証済みユーザータイプ{#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-8c7ba8d2bce14071b21fccb11f44749f}

**入力(updateVignettePublishFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| ` *`vignetteFormatHandle`*` | `xsd:string` | はい | 発行形式ハンドル |
| ` *`name`*` | `xsd:string` | いいえ | 発行形式名。 |
| ` *`targetWidth`*` | `xsd:int` | はい | 生成されるビネット表示のターゲット幅をピクセル単位で指定します。 ゼロを指定すると、出力ビネットはプライマリビネットと同じサイズになります。 |
| ` *`targetHeight`*` | `xsd:int` | はい | 生成されるビネット表示のターゲットの高さをピクセル単位で指定します。 ゼロを指定すると、出力ビネットはプライマリビネットと同じサイズになります。 |
| ` *`createPyramid`*` | `xsd:boolean` | はい | 画像レンダリングサーバでのズーム処理に最適なピラミッドビネットを作成します。このオプションでは、1 つのビネット出力ファイルで複数サイズの表示を作成します。ターゲットビネットサイズフィールドで設定された最大サイズから作成を開始します。表示のサイズは、幅と高さが 128x128 ピクセル以内になるまで、1/2 ずつ縮小されます。 |
| ` *`thumbWidth`*` | `xsd:int` | はい | 生成される各サムネールの幅をピクセル単位で指定します。この設定はオプションです。 サムネールファイルを作成しない場合は、ゼロのままにします。 |
| ` *`saveAsVersion`*` | `xsd:int` | はい | 公開するビネットのファイル形式を指定します。 新しいバージョンの画像オーサリングと古いバージョンの画像レンダリングサーバを使用する場合は、ImageRendering Serverが読み取ることのできるビネットバージョンを指定する必要があります。 より新しいバージョンを指定した場合、Image Rendering Serverは公開されたビネットを読み取れません。 最新バージョンでビネットを公開するには、ゼロに設定します。 |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | はい | ビネット名と幅を示すサフィックスを区切る文字を指定します。 |
| ` *`シャープ`*` | `xsd:int` | いいえ | 各公開ビネットサイズに対して、メイン表示画像にシャープを適用します。シャープを適用すると、ビネットを拡大・縮小したときにぼかしを補正できます。 |
| ` *`usmAmount`*` | `xsd:double` | はい | デジタルアンシャープマスクは、特にスキャン画像でシャープさを高める柔軟で強力な方法です。 これにより、各オーバーシュートの大きさ（エッジの境界線の暗さと明るさ）が制御されます。 |
| ` *`usmRadius`*` | `xsd:double` | はい | 拡大するエッジのサイズやエッジの縁の幅に影響を与えるので、半径を小さくすると、より小さなスケールのディテールが強調されます。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かいディテールは、同じサイズの小さいまたは半径より小さい細かいディテールが失われるので、小さい半径が必要です。 |
| ` *`usmThreshold`*` | `xsd:int` | はい | シャープを適用する明るさの最小値、またはフィルターが機能する前に隣接する階調値の間隔を制御します。 この設定により、より細かいエッジにシャープを適用し、より細かいエッジに手を加えないようにできます。 許容範囲のしきい値は0 ～ 255です。 |

**出力(updateVignettePublishFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | はい | 更新されたビネット公開形式に対する処理。 |

## 例 {#section-fcba4bf2b7264786a676e315a35dbe43}

次のコードのサンプルを使用すると、ビネット公開形式を更新し、ハンドルを更新した形式に戻すことができます。

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

