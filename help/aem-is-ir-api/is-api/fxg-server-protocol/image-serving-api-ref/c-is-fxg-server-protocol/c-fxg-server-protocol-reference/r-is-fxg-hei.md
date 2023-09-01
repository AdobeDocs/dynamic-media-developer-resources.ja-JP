---
title: hei
description: ビューの高さ。 返信画像の高さを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# hei{#hei}

ビューの高さ。 返信画像の高さを指定します。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（ピクセル単位、整数値 0 以上）。 </p></td> 
 </tr> 
</table>

ラスター形式は、[ 既定のビューサイズ ] （または [DefaultPix] 設定）を使用してレンダリングされます。 選択 **[!UICONTROL アプリケーション設定]** > **[!UICONTROL 公開設定]** > **[!UICONTROL Image Server]**「幅」と「高さ」の値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 設定を保存し、画像サービング公開を実行して変更を適用します。

次の条件を満たす場合、 `scale=1` コマンドを使用すると、FXG で指定されたサイズでラスター形式の要求がレンダリングされます。

## 初期設定 {#section-76ee3daa77cb468ab310821357cc9404}

次の場合 `wid=`, `hei=`または `scale=` が指定されていない場合、返信画像は FXG ファイルで指定されているデフォルトの表示サイズになります。

## 例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

形式が指定されていない場合、イメージはイメージファイルとしてレンダリングSWFされます。 この場合、SWFは通常ブラウザーウィンドウのサイズに拡大されるので、高さと幅は意味を持ちません。 その結果、hei と wid はラスター形式またはPDF形式にのみ適用されます。 ラスター形式には次のものが含まれます。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF — アルファ
* TIF-alpha
* PNG-alpha
