---
title: wid
description: ビューの幅： 返信画像（ビュー画像）の幅を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
TQID: 'https://experienceleague.adobe.com/A1n6WpZEsDWfdLoQZZY-ykX4zXjG86BRXHnVfcpO9yo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 1%

---

# wid{#wid}

ビューの幅： 返信画像（ビュー画像）の幅を指定します。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の幅（ピクセル単位）（0より大きい整数）、 </p></td> 
 </tr> 
</table>

## 初期設定 {#section-830bae0b6bac440098444d7cdcb23e2e}

`wid=`、`hei=`および`scale=`のいずれも指定しない場合、返信画像はFXG ファイルで指定されたデフォルトのビューサイズになります。

ラスタライズ形式は、デフォルトの表示サイズ（またはDefaultPix設定）を使用してレンダリングされます。 **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**&#x200B;をクリックし、幅と高さの値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 設定を保存し、画像サービング公開を実行して変更を適用します。

`scale=1` コマンドを適用すると、FXGで指定されたサイズでラスター形式の要求がレンダリングされます。

## 例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

フォーマットを指定しない限り、画像はSWF ファイルとしてレンダリングされます。 この場合、SWFは通常ブラウザーウィンドウのサイズに展開されるので、高さと幅は意味がありません。 結果、`hei`と`wid`はラスターまたはPDF形式にのみ適用されます。 ラスター形式には次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
