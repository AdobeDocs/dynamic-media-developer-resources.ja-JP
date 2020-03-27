---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
topic: Dynamic media
uuid: c7063907-78e8-47f8-9424-78ab9d123ad1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`テンプレート`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> テンプレート</span></span> </p> </td> 
   <td> <p>情報サーバから返されたデータの結合先のコンテンツテンプレート。 </p> <p>コンテンツテンプレートは、次のDTDに続くXMLです。 </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>コンテンツテンプレートの実際の構文は次のとおりです。 </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>つまり、テンプレートは&lt; <span class="codeph"> info&gt;要素で始まる必要があります</span> 。この要素には、オプションのデフォルトの <span class="codeph"> &lt;var&gt;要素を含めることができます</span> 。 テンプレートのコンテンツ <span class="codeph"> TEMPLATE_CONTENTは</span> HTMLテキストです。 また、コンテンツテンプレートには、変数名を <span class="codeph"> $</span> ($)で囲み、情報サーバが返す変数値またはデフォルトの変数値に置き換えることができます。 </p> <p>テンプレートで定義される初期設定の変数は、グローバル変数（rollover属性が設定されていない場合）または特定のロールオーバーキーに固有の変数（rollover属性が存在する場合）のいずれかです。 </p> <p>テンプレートの処理時に、ロールオーバーキーに固有の変数がグローバル変数よりも優先されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTMLコードとJavaScriptコードがクライアントのコンピューター上で実行されることに注意してください。 したがって、このようなHTMLコードとJavaScriptコードが安全であることを確認してください。

## プロパティ {#section-6dd7785357d740d095fa9f7fd0f67da4}

（オプション）

## 初期設定 {#section-cd5db06d08aa4de49e37d6c938b41570}

なし

## 例 {#section-16d184665c484964af9a22f79ff3f840}

情報サーバの応答が製品名を変数として返し、製品 `$1$` 画像のURLを変数として返す場合 `$2$`。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
