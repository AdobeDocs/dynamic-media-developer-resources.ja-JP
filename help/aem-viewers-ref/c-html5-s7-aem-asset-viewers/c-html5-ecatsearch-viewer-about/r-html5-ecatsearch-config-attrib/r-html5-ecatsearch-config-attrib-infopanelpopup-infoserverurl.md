---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
TQID: 'https://experienceleague.adobe.com/en4zktUgJGVG-e0fahRGTxasP3CVxhgfie6d0e3q6r4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>情報サーバーのURL テンプレートは、情報パネルのコンテンツテンプレートで変数置換のキーと値のペアを取得するために使用されます。 指定されたテンプレートには、通常、リクエストがサーバーに送信される前に、実際のデータに置き換えられるマクロプレースホルダーが含まれています。 </p> <p><span class="codeph"> $1$</span>は、<span class="codeph"> InfoPanelPopup</span>のアクティベーションをトリガーしたロールオーバー値に置き換えられます。 </p> <p><span class="codeph"> $2$</span>は、画像セット内の現在のフレームのシーケンス番号に置き換えられます。 </p> <p><span class="codeph"> $3$</span>は、現在の項目の親セットの名前で指定された最初のパス要素に置き換えられます。 通常、カタログ IDに対応します。 </p> <p><span class="codeph"> $4$</span>は、パス内の次の要素に置き換えられ、アセット idに対応します。 実際のinfo server リクエスト構文はinfo serverに依存し、サーバーごとに異なります。 例えば、一般的なDynamic Media情報サーバーリクエストテンプレートは次のとおりです。 </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTML コードとJavaScript コードがクライアントのコンピューターで実行されることに注意してください。 したがって、このようなHTML コードとJavaScript コードが安全であることを確認してください。

## プロパティ {#section-71356e3c13244e62b0582980d9d05328}

オプション。

## 初期設定 {#section-22e9af803f724434807d34e200eb7518}

なし

## 例 {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
