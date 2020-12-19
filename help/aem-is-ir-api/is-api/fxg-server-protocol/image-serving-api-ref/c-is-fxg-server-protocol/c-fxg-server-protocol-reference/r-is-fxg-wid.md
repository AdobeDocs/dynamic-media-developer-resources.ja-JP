---
description: 表示の幅。 返信画像(表示画像)の幅を指定します。
seo-description: 表示の幅。 返信画像(表示画像)の幅を指定します。
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 4%

---


# wid{#wid}

表示の幅。 返信画像(表示画像)の幅を指定します。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、0より大きい整数）、 </p></td> 
 </tr> 
</table>

## 初期設定 {#section-830bae0b6bac440098444d7cdcb23e2e}

`wid=`、`hei=`、`scale=`のいずれも指定されていない場合、返信表示はFXGファイルで指定されているデフォルトの画像サイズになります。

ラスター形式は、[既定の表示サイズ]（または[既定のPIX]設定）を使用してレンダリングされます。 **[!UICONTROL アプリケーション設定]**/**[!UICONTROL 公開設定]**/**[!UICONTROL Image Server]**&#x200B;をクリックし、幅と高さの値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 変更を適用するには、設定を保存し、画像サービング公開を実行する必要があります。

`scale=1`コマンドを適用すると、FXGで指定されたサイズでラスター形式の要求がレンダリングされます。

## 例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

形式を指定しない限り、画像はSWFファイルとしてレンダリングされます。 この場合、SWFは通常ブラウザーウィンドウのサイズに拡張されるので、高さと幅は意味を持ちません。 その結果、heiとwidはラスター形式またはPDF形式にのみ適用されます。 ラスター形式には次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

