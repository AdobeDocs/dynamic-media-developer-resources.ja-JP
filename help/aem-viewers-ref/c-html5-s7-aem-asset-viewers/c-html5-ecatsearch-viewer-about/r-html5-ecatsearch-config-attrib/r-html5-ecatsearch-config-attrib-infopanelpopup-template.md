---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`テンプレート`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> テンプレート</span></span> </p> </td> 
   <td> <p>情報サーバから返されたデータの結合先となるコンテンツテンプレート。 </p> <p>コンテンツテンプレートは、次のDTDに従うXMLです。 </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>コンテンツテンプレートの実際の構文は次のとおりです。 </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>つまり、テンプレートは<span class="codeph"> &lt;info&gt;</span>要素で始まる必要があります。この要素には、オプションのデフォルトの<span class="codeph"> &lt;var&gt;</span>要素を含めることができます。 テンプレートコンテンツ自体の<span class="codeph"> TEMPLATE_CONTENT</span>はHTMLテキストです。 また、コンテンツテンプレートには、変数名を<span class="codeph"> $</span>文字で囲んで含めることもできます。 これらの文字は、情報サーバが返す変数値、またはデフォルト値に置き換えられます。 </p> <p>テンプレートで定義されるデフォルトの変数は、グローバル変数（rollover属性が設定されていない場合）か、特定のロールオーバーキーに固有の変数（rollover属性が存在する場合）のいずれかです。 </p> <p>テンプレートの処理時に、ロールオーバーキーに固有の変数がグローバル変数より優先されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTMLコードとJavaScriptコードがクライアントのコンピューター上で実行されることに注意してください。 したがって、このようなHTMLコードとJavaScriptコードは必ず安全にしてください。

## プロパティ {#section-6dd7785357d740d095fa9f7fd0f67da4}

（オプション）

## 初期設定 {#section-cd5db06d08aa4de49e37d6c938b41570}

なし

## 例 {#section-16d184665c484964af9a22f79ff3f840}

情報サーバの応答が製品名を変数`$1$`として返し、製品画像のURLを変数`$2$`として返すとします。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
