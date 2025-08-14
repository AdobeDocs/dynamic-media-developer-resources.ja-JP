---
title: wid
description: ビューの幅 返信画像（ビュー画像）の幅を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# wid{#wid}

ビューの幅 返信画像（ビュー画像）の幅を指定します。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位）（0 より大きい整数）、 </p></td> 
 </tr> 
</table>

## 初期設定 {#section-830bae0b6bac440098444d7cdcb23e2e}

`wid=`、`hei=`、`scale=` のいずれも指定されていない場合、返信画像は FXG ファイルで指定されたデフォルトの表示サイズになります。

ラスター形式は、既定のビューサイズ（または DefaultPix 設定）を使用してレンダリングされます。 **[!UICONTROL アプリケーション設定]**/**[!UICONTROL 公開設定]**/**[!UICONTROL Image Server]** をクリックし、幅と高さの値を入力します。 サイズが小さいほど、パフォーマンスが向上します。 設定を保存し、画像サービング公開を実行して変更を適用します。

`scale=1` コマンドを適用すると、ラスター形式要求は FXG で指定されたサイズでレンダリングされます。

## 例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

形式を指定しない場合、画像はSWF ファイルとしてレンダリングされます。 この場合、SWFは通常、ブラウザーウィンドウのサイズに拡大されるので、高さと幅に意味はありません。 その結果、`hei` と `wid` はラスター形式またはPDF形式にのみ適用されます。 ラスター形式には次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIFアルファ
* TIF-α
* PNG – アルファ
