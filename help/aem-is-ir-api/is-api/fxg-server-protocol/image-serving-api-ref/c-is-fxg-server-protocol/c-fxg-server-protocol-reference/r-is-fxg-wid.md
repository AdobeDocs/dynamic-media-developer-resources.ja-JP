---
title: wid
description: 表示の幅。 返信画像（表示画像）の幅を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# wid{#wid}

表示の幅。 返信画像（表示画像）の幅を指定します。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の幅（0 より大きい整数） </p></td> 
 </tr> 
</table>

## 初期設定 {#section-830bae0b6bac440098444d7cdcb23e2e}

どちらでもない場合 `wid=`, `hei=`または `scale=` を指定した場合、返信画像は FXG ファイルで指定されたデフォルトの表示サイズになります。

ラスター形式は、[ 既定のビューサイズ ] （または [DefaultPix] 設定）を使用してレンダリングされます。 クリック **[!UICONTROL アプリケーション設定]** > **[!UICONTROL 公開設定]** > **[!UICONTROL Image Server]**「幅」と「高さ」の値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 設定を保存し、画像サービング公開を実行して変更を適用します。

次の条件を満たす場合、 `scale=1` コマンドを使用すると、FXG で指定されたサイズでラスター形式の要求がレンダリングされます。

## 例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

形式が指定されていない場合、イメージはイメージファイルとしてレンダリングSWFされます。 この場合、SWFは通常ブラウザーウィンドウのサイズに拡大されるので、高さと幅は意味を持ちません。 その結果、 `hei` および `wid` は、ラスター形式またはPDF形式にのみ適用されます。 ラスター形式には次のものが含まれます。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF — アルファ
* TIF-alpha
* PNG-alpha
