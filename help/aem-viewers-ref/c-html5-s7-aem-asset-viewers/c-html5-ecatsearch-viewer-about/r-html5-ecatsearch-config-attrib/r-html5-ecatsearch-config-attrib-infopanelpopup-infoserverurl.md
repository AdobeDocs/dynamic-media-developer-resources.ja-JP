---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>情報サーバのURLテンプレートは、情報パネルコンテンツテンプレートで変数の置き換え用のキーと値のペアを取得するために使用されます。指定したテンプレートには、通常、マクロプレースホルダが含まれます。このプレースホルダは、リクエストがサーバーに送信される前に、実際のデータに置き換えられます。 </p> <p><span class="codeph"> $1$</span> は、InfoPanelPopupactivationをトリガーしたロールオーバー値に置き換えら <span class="codeph"> </span> れます。 </p> <p><span class="codeph"> $2$</span> は、画像セット内の現在のフレームのシーケンス番号に置き換えられます。 </p> <p><span class="codeph"> $3$</span> は、現在の項目の親セットの名前で指定された最初のパス要素に置き換えられます。これは通常、カタログIDに対応します。 </p> <p><span class="codeph"> $4$</span> は、パスの次の要素に置き換えられ、アセットIDに対応します。実際の情報サーバの要求構文は、情報サーバに依存し、サーバごとに異なります。 例えば、次に示すのは一般的なDynamic Media情報サーバの要求テンプレートです。 </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTMLコードとJavaScriptコードがクライアントのコンピューター上で実行されることに注意してください。 したがって、このようなHTMLコードとJavaScriptコードは必ず安全にしてください。

## プロパティ {#section-71356e3c13244e62b0582980d9d05328}

（オプション）

## 初期設定 {#section-22e9af803f724434807d34e200eb7518}

なし

## 例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
