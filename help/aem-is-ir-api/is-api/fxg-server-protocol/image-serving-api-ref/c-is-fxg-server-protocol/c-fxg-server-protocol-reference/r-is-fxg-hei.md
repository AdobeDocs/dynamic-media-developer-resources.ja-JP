---
description: ビューの高さ 返信画像の高さを指定します。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 3%

---

# hei{#hei}

ビューの高さ 返信画像の高さを指定します。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（ピクセル単位、0より大きい整数）。 </p></td> 
 </tr> 
</table>

ラスター形式は、[既定のビューサイズ]（または[既定のPix]設定）を使用してレンダリングされます。 **[!UICONTROL アプリケーション設定]** / **[!UICONTROL 公開設定]** / **[!UICONTROL Image Server]**&#x200B;をクリックし、「幅」と「高さ」の値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 設定を保存し、画像サービングの公開を実行して変更を適用する必要があります。

`scale=1`コマンドを適用すると、FXGで指定されたサイズでラスター形式の要求がレンダリングされます。

## 初期設定 {#section-76ee3daa77cb468ab310821357cc9404}

`wid=`、`hei=`、`scale=`のいずれも指定されていない場合、返信画像はFXGファイルで指定されたデフォルトの表示サイズになります。

## 例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

形式を指定しない限り、画像はSWFファイルとしてレンダリングされます。 この場合、SWFは通常、ブラウザーウィンドウのサイズに拡大されるので、高さと幅は意味を持ちません。 その結果、heiとwidはラスター形式またはPDF形式にのみ適用されます。 ラスター形式には、次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
