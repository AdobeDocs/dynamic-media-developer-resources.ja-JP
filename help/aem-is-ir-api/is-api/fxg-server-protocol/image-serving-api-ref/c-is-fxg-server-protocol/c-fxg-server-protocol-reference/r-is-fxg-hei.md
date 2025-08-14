---
title: ヘイ
description: ビューの高さ 返信画像の高さを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# ヘイ{#hei}

ビューの高さ 返信画像の高さを指定します。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（ピクセル単位）（0 より大きい整数）。 </p></td> 
 </tr> 
</table>

ラスター形式は、既定のビューサイズ（または DefaultPix 設定）を使用してレンダリングされます。 **[!UICONTROL アプリケーション設定]**/**[!UICONTROL 公開設定]**/**[!UICONTROL Image Server]** を選択し、幅と高さの値を入力します。 サイズが小さいほど、パフォーマンスが向上します。 設定を保存し、画像サービング公開を実行して変更を適用します。

`scale=1` コマンドを適用すると、ラスター形式要求は FXG で指定されたサイズでレンダリングされます。

## 初期設定 {#section-76ee3daa77cb468ab310821357cc9404}

`wid=`、`hei=`、`scale=` が指定されていない場合、返信画像は FXG ファイルで指定されたデフォルトの表示サイズです。

## 例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

形式を指定しない場合、画像はSWF ファイルとしてレンダリングされます。 この場合、SWFは通常、ブラウザーウィンドウのサイズに拡大されるので、高さと幅に意味はありません。 その結果、hei と wid はラスター形式またはPDF形式にのみ適用されます。 ラスター形式には次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIFアルファ
* TIF-α
* PNG – アルファ
