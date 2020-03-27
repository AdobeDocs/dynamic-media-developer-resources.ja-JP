---
description: ビネット公開形式の設定を更新します。
seo-description: ビネット公開形式の設定を更新します。
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateVignettePublishFormat{#updatevignettepublishformat}

ビネット公開形式の設定を更新します。

## 認証されたユーザータイプ {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-8c7ba8d2bce14071b21fccb11f44749f}

**入力(updateVignettePublishFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| ` *`vignetteFormatHandle`*` | `xsd:string` | はい | 発行形式ハンドル。 |
| ` *`name`*` | `xsd:string` | いいえ | 発行形式名。 |
| ` *`targetWidth`*` | `xsd:int` | はい | ビネットビューのターゲット幅をピクセル単位で指定します。 出力ビネットがマスタービネットと同じサイズになるように、ゼロを使用します。 |
| ` *`targetHeight`*` | `xsd:int` | はい | 結果のビネットビューのターゲットの高さをピクセル単位で指定します。 出力ビネットがマスタービネットと同じサイズになるように、ゼロを使用します。 |
| ` *`createPyramid`*` | `xsd:boolean` | はい | 画像レンダリングサーバでのズーム処理に最適なピラミッドビネットを作成します。このオプションでは、1 つのビネット出力ファイルで複数サイズの表示を作成します。ターゲットビネットサイズフィールドで設定された最大サイズから作成を開始します。表示のサイズは、幅と高さが 128x128 ピクセル以内になるまで、1/2 ずつ縮小されます。 |
| ` *`thumbWidth`*` | `xsd:int` | はい | 生成される各サムネールの幅をピクセル単位で指定します。この設定はオプションです。 サムネールファイルを作成しない場合は、ゼロのままにします。 |
| ` *`saveAsVersion`*` | `xsd:int` | はい | 公開するビネットのファイル形式を指定します。 新しいバージョンのImage Authoringと古いバージョンのImage Rendering Serverを使用する場合は、ImageRendering Serverが読み取ることのできるビネットバージョンを指定する必要があります。 より新しいバージョンを指定した場合、Image Rendering Serverは公開されたビネットを読み取れません。 最新バージョンでビネットを公開するには、0に設定します。 |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | はい | ビネット名と幅を示すサフィックスを区切る文字を指定します。 |
| ` *`シャープ`*` | `xsd:int` | いいえ | 各公開ビネットサイズに対して、メインビュー画像にシャープを適用します。シャープを適用すると、ビネットを拡大・縮小したときのぼかしを補正できます。 |
| ` *`usmAmount`*` | `xsd:double` | はい | デジタルアンシャープマスクは、特にスキャンされた画像のシャープを高める柔軟で強力な方法です。 各オーバーシュートの大きさ（エッジの境界線がどの程度暗く、明るくなるか）を制御します。 |
| ` *`usmRadius`*` | `xsd:double` | はい | 拡大するエッジのサイズやエッジの縁の幅に影響を与え、半径を小さくすると細部の拡大・縮小が促進されます。 半径の値を大きくすると、エッジにハローが発生する場合があります。 細かいディテールは、同じサイズの小さなディテールまたは半径より小さなディテールが失われるので、小さな半径が必要です。 |
| ` *`usmThreshold`*` | `xsd:int` | はい | シャープを適用する明るさの最小値や、隣接する階調値の間隔を指定してフィルターを機能させるかどうかを制御します。 この設定により、より細かいエッジを残したまま、より回転するエッジにシャープを適用できます。 許容されるしきい値の範囲は0 ～ 255です。 |

**出力(updateVignettePublishFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | はい | 更新されたビネット公開形式の処理。 |

## 例 {#section-fcba4bf2b7264786a676e315a35dbe43}

次のコードサンプルを使用すると、ビネット公開形式を更新し、ハンドルを更新された形式に戻すことができます。

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

