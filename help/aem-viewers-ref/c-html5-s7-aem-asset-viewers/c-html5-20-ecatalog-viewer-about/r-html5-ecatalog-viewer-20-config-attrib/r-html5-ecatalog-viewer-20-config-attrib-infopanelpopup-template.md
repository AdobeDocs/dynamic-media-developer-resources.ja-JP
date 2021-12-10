---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`テンプレート`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> テンプレート</span></span> </p> </td> 
   <td> <p>情報サーバから返されたデータの結合先となるコンテンツテンプレート。 </p> <p>コンテンツテンプレートは、次の DTD に続く XML です。 </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>コンテンツテンプレートの実際の構文は次のとおりです。 </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>つまり、テンプレートは <span class="codeph"> &lt;info&gt;</span> オプションのデフォルトを含む要素 <span class="codeph"> &lt;var&gt;</span> 要素。 テンプレートの内容自体 <span class="codeph"> TEMPLATE_CONTENT</span> はHTMLテキストです。 また、コンテンツテンプレートには、変数名を <span class="codeph"> $</span> 情報サーバが返す変数値、またはデフォルト値に置き換えられる文字。 </p> <p>テンプレートで定義されるデフォルトの変数は、グローバル変数（rollover 属性が設定されていない場合）または特定のロールオーバーキーに固有の変数（rollover 属性が存在する場合）にすることができます。 </p> <p>テンプレート処理時に、ロールオーバーキーに固有の変数がグローバル変数よりも優先されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されたHTMLコードおよび JavaScript コードがクライアントのコンピューターで実行されます。 そのため、このようなHTMLコードと JavaScript コードは必ず安全にしてください。

## プロパティ {#section-6dd7785357d740d095fa9f7fd0f67da4}

（オプション）

## 初期設定 {#section-cd5db06d08aa4de49e37d6c938b41570}

なし

## 例 {#section-16d184665c484964af9a22f79ff3f840}

情報サーバの応答が製品名を変数として返す場合 `$1$` と製品画像の URL が変数として返されます。 `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
