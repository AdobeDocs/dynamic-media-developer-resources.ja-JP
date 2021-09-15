---
title: config
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 4%

---

# config{#config}

すべてのビューアに共通のパラメーター。

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>ビューア設定のカタログ/ID。 </p> <p> <span class="codeph"> catalog::UserData </span>内にビューア設定プロパティが含まれる画像カタログエントリを指定します。 このコマンドがある場合、ビューアは<span class="codeph"> configId </span>の<span class="codeph"> req=userdata </span>コマンドをサーバに送信し、応答からプロパティを抽出します。 プロパティを使用してビューアが初期化されます。 URL文字列が同じプロパティを指定している場合、 <span class="codeph"> catalog::UserData </span>の値を上書きします。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`catalog::UserData`で指定できるすべてのビューアコマンドには、`asset`、`serverUrl`、`contentUrl`、`searchServerUrl`、`config`自体が必要です。

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

なし

## 例 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

2020という画像カタログには、エントリ`preset-oct`が含まれています。 このカタログエントリの`catalog::UserData`フィールドには、次のデータが含まれます。

```
style=customStyle.css
```

次のコマンドを使用してビューアを読み込みます。

```
config=2020/preset-oct
```

この例は、URLで明示的に指定された次のコマンドと同じです。

```
style=customStyle.css
```

## 例 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

2019という画像カタログにエントリ`spin-oct`が含まれています。 このカタログエントリの`catalog::UserData`フィールドには、次のデータが含まれます。

```
zoomStep=3 
maxZoom=200
```

次のコマンドを使用してビューアを読み込みます。

```
config=2019/spin-oct
```

この例は、URLで明示的に指定された次のコマンドと同じです。

```
zoomStep=3&maxZoom=200
```

## 例 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

`Shoppable_Banner`という名前のビューアプリセットには、次のデータが含まれます。

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

次のコマンドを使用してビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

この例は、URLで明示的に指定された次のコマンドと同じです。

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 例 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

`Shoppable_Video_Dark`という名前のビューアプリセットには、次のデータが含まれます。

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

次のコマンドを使用してビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

この例は、URLで明示的に指定された次のコマンドと同じです。

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 例 5 {#section-19b988551d1d492a9079948e0b04b38f}

`Carousel_Dotted_light`という名前のビューアプリセット（以下のデータ）。

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

次のコマンドを使用してビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

この例は、URLで明示的に指定された次のコマンドと同じです。

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
