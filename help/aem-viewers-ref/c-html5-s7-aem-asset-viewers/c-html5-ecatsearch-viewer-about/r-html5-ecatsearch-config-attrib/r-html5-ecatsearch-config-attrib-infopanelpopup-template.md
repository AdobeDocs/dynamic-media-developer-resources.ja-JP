---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *` テンプレート `*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> テンプレ <span class="codeph"><span class="varname"> ト </span></span> </p> </td> 
   <td> <p>情報サーバーから返されたデータが結合されるコンテンツテンプレート。 </p> <p>コンテンツテンプレートは、この DTD に続く XML です。 </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>コンテンツテンプレートの実際の構文は次のとおりです。 </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>つまり、テンプレートは <span class="codeph"> &lt;info&gt;</span> 要素で始める必要があります。この要素には、オプションのデフォルト <span class="codeph"> &lt;var&gt;</span> 要素を含めることができます。 テンプレートコンテンツ自体 <span class="codeph">TEMPLATE_CONTENT</span> はHTMLのテキストです。 さらに、コンテンツテンプレートには、<span class="codeph"> $</span> 文字で囲まれた変数名を含めることができます。 これらの文字は、情報サーバーが返す変数値またはデフォルトの変数値に置き換えられます。 </p> <p>テンプレートで定義されるデフォルト変数は、グローバル（rollover 属性が設定されていない場合）または特定のロールオーバーキーに固有（rollover 属性が存在する場合）のいずれかです。 </p> <p>テンプレート処理中は、ロールオーバーキー専用の変数がグローバル変数よりも優先されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定する場合、情報パネルに渡されたHTML コードとJavaScript コードはクライアントのコンピューター上で実行されます。 そのため、このようなHTML コードとJavaScript コードが安全であることを確認してください。

## プロパティ {#section-6dd7785357d740d095fa9f7fd0f67da4}

オプション。

## 初期設定 {#section-cd5db06d08aa4de49e37d6c938b41570}

なし

## 例 {#section-16d184665c484964af9a22f79ff3f840}

情報サーバー応答が製品名を変数 `$1$` として返し、製品画像 URL が変数 `$2$` として返されるとします。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
