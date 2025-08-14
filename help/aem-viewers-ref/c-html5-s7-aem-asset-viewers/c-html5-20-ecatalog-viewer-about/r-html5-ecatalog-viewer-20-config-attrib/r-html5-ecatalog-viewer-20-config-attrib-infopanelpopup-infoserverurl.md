---
title: InfoPanelPopup.infoServerUrl
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 83abaecb-cc85-4918-98ed-2770b4ca407b
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>情報サーバー URL テンプレートは、情報パネルコンテンツテンプレート内の変数置換のキーと値のペアを取得するために使用されます。 指定されたテンプレートには通常、リクエストがサーバーに送信される前に実際のデータに置き換えられるマクロのプレースホルダーが含まれています。 </p> <p><span class="codeph"> $1$</span> は、<span class="codeph"> InfoPanelPopup</span> アクティベーションをトリガーしたロールオーバー値に置き換えられます。 </p> <p><span class="codeph"> $2$</span> は、画像セット内の現在のフレームのシーケンス番号に置き換えられます。 </p> <p><span class="codeph"> $3$</span> は、現在の項目の親セットの名前で指定された最初のパス要素に置き換えられます。 通常は、カタログ ID に対応します。 </p> <p><span class="codeph"> $4$</span> は、パス内の次の要素に置き換えられ、アセット id に対応します。 実際の info サーバーリクエストの構文は info サーバーに依存し、サーバーによって異なります。 例えば、以下は一般的な Dynamic Media 情報サーバーのリクエストテンプレートです。 </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されたHTML コードとJavaScript コードがクライアントのコンピューター上で実行されます。 そのため、このようなHTML コードとJavaScript コードが安全であることを確認してください。

## プロパティ {#section-71356e3c13244e62b0582980d9d05328}

オプション。

## 初期設定 {#section-22e9af803f724434807d34e200eb7518}

なし

## 例 {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
