---
title: config
description: すべてのビューアに共通のパラメーター。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
TQID: 'https://experienceleague.adobe.com/dqbTP8mI5YGjwqG2AbkT3L0HIeLZ9qDIA6A78R5i-IQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 264
ht-degree: 2%

---

# config{#config}

すべてのビューアに共通のパラメーター。

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span> </span> </p> </td> 
   <td colname="col2"> <p>ビューア設定のカタログ/ID。 </p> <p> <span class="codeph"> カタログ：:UserData </span>のビューア設定プロパティを含む画像カタログエントリを指定します。 このコマンドが存在する場合、ビューアは<span class="codeph">configId </span>の<span class="codeph"> req=userdata </span> コマンドをサーバーに送信し、応答からプロパティを抽出します。 プロパティは、ビューアの初期化に使用されます。 URL文字列で同じプロパティが指定されている場合は、<span class="codeph"> カタログ：:UserData </span>の値が上書きされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

`catalog::UserData`で指定できるすべてのビューアーコマンドには、`asset`、`serverUrl`、`contentUrl`、`searchServerUrl`および`config`自体が必要です。

## プロパティ {#section-10ee45d637134e0fbcd943c62578cb78}

オプション。

## 初期設定 {#section-d411e450028c460392cb8508f8ccc5d9}

なし

## 例 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

2020という名前の画像カタログには、エントリ `preset-oct`が含まれています。 このカタログ エントリの`catalog::UserData` フィールドには、次のデータが含まれます。

```
style=customStyle.css
```

次のコマンドでビューアを読み込みます。

```
config=2020/preset-oct
```

この例は、URLで明示的に指定された次のコマンドと同等です。

```
style=customStyle.css
```

## 例2 {#section-577fce5ddbee43fc96d88b2055df47aa}

2019という名前の画像カタログには、エントリ `spin-oct`が含まれています。 このカタログ エントリの`catalog::UserData` フィールドには、次のデータが含まれます。

```
zoomStep=3 
maxZoom=200
```

次のコマンドでビューアを読み込みます。

```
config=2019/spin-oct
```

この例は、URLで明示的に指定された次のコマンドと同等です。

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

この例は、URLで明示的に指定された次のコマンドと同等です。

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 例4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

`Shoppable_Video_Dark`という名前のビューアプリセットには、次のデータが含まれます。

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

次のコマンドでビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

この例は、URLで明示的に指定された次のコマンドと同等です。

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 例5 {#section-19b988551d1d492a9079948e0b04b38f}

次のデータの`Carousel_Dotted_light`という名前のビューアプリセット：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

次のコマンドでビューアを読み込みます。

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

この例は、URLで明示的に指定された次のコマンドと同等です。

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
