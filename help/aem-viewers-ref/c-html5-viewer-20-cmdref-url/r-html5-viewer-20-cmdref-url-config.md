---
description: すべてのビューアに共通のパラメータ。
seo-description: すべてのビューアに共通のパラメータ。
seo-title: config
solution: Experience Manager
title: config
topic: Dynamic media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 3%

---


# config{#config}

すべてのビューアに共通のパラメータ。

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>ビューア設定のカタログ/ID。 </p> <p> <span class="codeph"> catalog::UserData </span>内にビューア設定プロパティが含まれる画像カタログエントリを指定します。 このコマンドがある場合、ビューアは<span class="codeph"> configId </span>の<span class="codeph"> req=userdata </span>コマンドをサーバに送信し、応答からプロパティを抽出します。 プロパティを使用してビューアが初期化されます。 URL文字列が同じプロパティを指定する場合、<span class="codeph"> catalog::UserData </span>の値よりも優先されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`catalog::UserData`で指定できるすべてのビューアコマンドには、`asset`、`serverUrl`、`contentUrl`、`searchServerUrl`、`config`が必要です。

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

（オプション）

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

なし

## 例 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

2020という画像カタログにエントリ`preset-oct`が含まれています。 このカタログエントリの`catalog::UserData`フィールドには、次のデータが含まれます。

```
style=customStyle.css
```

次のコマンドでビューアを読み込みます。

```
config=2020/preset-oct
```

これは、URLで明示的に次のコマンドを指定することと同じです。

```
style=customStyle.css
```

## 例2 {#section-577fce5ddbee43fc96d88b2055df47aa}

2019という画像カタログにエントリ`spin-oct`が含まれています。 このカタログエントリの`catalog::UserData`フィールドには、次のデータが含まれます。

```
zoomStep=3 
maxZoom=200
```

次のコマンドでビューアを読み込みます。

```
config=2019/spin-oct
```

これは、URLで明示的に次のコマンドを指定することと同じです。

```
zoomStep=3&maxZoom=200
```

## 例3 {#section-2b3a42c3926e4eb19fa14434def9195f}

`Shoppable_Banner`という名前のビューアプリセットには、次のデータが含まれます。

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

次のコマンドでビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

これは、URLで明示的に次のコマンドを指定することと同じです。

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 例5 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

`Shoppable_Video_Dark`という名前のビューアプリセットには、次のデータが含まれています。

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

次のコマンドでビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

これは、URLで明示的に次のコマンドを指定することと同じです。

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 例5 {#section-19b988551d1d492a9079948e0b04b38f}

`Carousel_Dotted_light`という名前のビューアプリセットは、次のデータを示します。

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

次のコマンドでビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

これは、URLで明示的に次のコマンドを指定することと同じです。

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

