---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>情報サーバのURLテンプレートは、情報パネルのコンテンツテンプレート内の変数の置き換えに使用するキーと値のペアを取得するために使用されます。通常、指定したテンプレートには、マクロプレースホルダが含まれており、リクエストがサーバに送信される前に実際のデータに置き換えられます。 </p> <p><span class="codeph"> $1$は</span> 、InfoPanelPopupのアクティブ化をトリガーしたロールオーバー値に置き換 <span class="codeph"> えられます</span> 。 </p> <p><span class="codeph"> $2$は</span> 、画像セット内の現在のフレームのシーケンス番号に置き換えられます。 </p> <p><span class="codeph"> $3$は</span> 、現在の項目の親セットの名前で指定された最初のパス要素に置き換えられます。 通常、これはカタログIDに対応します。 </p> <p><span class="codeph"> $4$は</span> 、パス内の次の要素に置き換えられ、アセットIDに対応します。 実際の情報サーバの要求構文は、情報サーバによって異なり、サーバごとに異なります。 例えば、次に示すのは、一般的なScene7情報サーバの要求テンプレートです。 </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTMLコードとJavaScriptコードがクライアントのコンピューター上で実行されることに注意してください。 したがって、このようなHTMLコードとJavaScriptコードが安全であることを確認してください。

## プロパティ {#section-71356e3c13244e62b0582980d9d05328}

（オプション）

## 初期設定 {#section-22e9af803f724434807d34e200eb7518}

なし

## 例 {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
