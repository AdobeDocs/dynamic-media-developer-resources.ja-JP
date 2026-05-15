---
title: へい
description: 表示の高さ。 返信画像の高さを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 1%

---

# へい{#hei}

表示の高さ。 返信画像の高さを指定します。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>画像の高さ（0 （0）より大きい値）。 </p></td> 
 </tr> 
</table>

ラスタライズ形式は、デフォルトの表示サイズ（またはDefaultPix設定）を使用してレンダリングされます。 **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**&#x200B;を選択し、幅と高さの値を入力します。 サイズを小さくすると、パフォーマンスが向上します。 設定を保存し、画像サービング公開を実行して変更を適用します。

`scale=1` コマンドを適用すると、FXGで指定されたサイズでラスター形式の要求がレンダリングされます。

## 初期設定 {#section-76ee3daa77cb468ab310821357cc9404}

`wid=`、`hei=`、または`scale=`が指定されていない場合、返信画像はFXG ファイルで指定されたデフォルトのビューサイズになります。

## 例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

フォーマットを指定しない限り、画像はSWF ファイルとしてレンダリングされます。 この場合、SWFは通常ブラウザーウィンドウのサイズに展開されるので、高さと幅は意味がありません。 その結果、heiとwidはラスター形式またはPDF形式にのみ適用されます。 ラスター形式には次のものがあります。

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
