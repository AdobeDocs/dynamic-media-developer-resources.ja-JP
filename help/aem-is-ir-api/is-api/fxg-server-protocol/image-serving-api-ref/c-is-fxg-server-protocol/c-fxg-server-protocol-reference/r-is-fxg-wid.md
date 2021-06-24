---
description: ビューの幅。 返信画像（ビュー画像）の幅を指定します。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# wid{#wid}

ビューの幅。 返信画像（ビュー画像）の幅を指定します。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位、0より大きい整数） </p></td> 
 </tr> 
</table>

## 初期設定 {#section-830bae0b6bac440098444d7cdcb23e2e}

`wid=`、`hei=`、`scale=`のいずれも指定されていない場合、返信画像はFXGファイルで指定されたデフォルトの表示サイズになります。

ラスター形式は、[既定のビューサイズ]（または[既定のPix]設定）を使用してレンダリングされます。 **[!UICONTROL アプリケーション設定]** / **[!UICONTROL 公開設定]** / **[!UICONTROL Image Server]**&#x200B;をクリックし、「幅」と「高さ」の値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 設定を保存し、画像サービングの公開を実行して変更を適用する必要があります。

`scale=1`コマンドを適用すると、FXGで指定されたサイズでラスター形式の要求がレンダリングされます。

## 例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

形式を指定しない限り、画像はSWFファイルとしてレンダリングされます。 この場合、SWFは通常、ブラウザーウィンドウのサイズに拡大されるので、高さと幅は意味を持ちません。 その結果、heiとwidはラスター形式またはPDF形式にのみ適用されます。 ラスター形式には、次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
