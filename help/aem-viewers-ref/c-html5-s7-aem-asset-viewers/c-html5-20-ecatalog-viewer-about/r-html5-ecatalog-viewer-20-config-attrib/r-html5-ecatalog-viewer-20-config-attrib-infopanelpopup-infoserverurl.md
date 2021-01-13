---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>情報サーバのURLテンプレートは、情報パネルコンテンツテンプレート内の変数の置換に使用するキー/値のペアを取得するために使用します。通常、指定したテンプレートには、マクロプレースホルダが含まれています。このプレースホルダは、要求がサーバに送信される前に、実際のデータに置き換えられます。 </p> <p><span class="codeph"> $1$</span> は、InfoPanelPopupactivationをトリガーしたロールオーバーの値に置き換えら <span class="codeph"> </span> れます。 </p> <p><span class="codeph"> $2$</span> は、画像セット内の現在のフレームのシーケンス番号に置き換えられます。 </p> <p><span class="codeph"> $3$</span> は、現在の項目の親セットの名前で指定された最初のパス要素に置き換えられます。通常、カタログIDに対応します。 </p> <p><span class="codeph"> $4$</span> は、パス内の次の要素に置き換えられ、アセットIDに対応します。実際の情報サーバ要求の構文は、情報サーバに依存し、サーバごとに異なります。 例えば、一般的なScene7情報サーバのリクエストテンプレートを次に示します。 </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定する場合、情報パネルに渡されるHTMLコードとJavaScriptコードは、クライアントのコンピューター上で実行されます。 したがって、このようなHTMLコードとJavaScriptコードが安全であることを確認してください。

## プロパティ {#section-71356e3c13244e62b0582980d9d05328}

（オプション）

## 初期設定 {#section-22e9af803f724434807d34e200eb7518}

なし

## 例 {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
