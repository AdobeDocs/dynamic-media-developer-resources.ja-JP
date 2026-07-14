---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
TQID: 'https://experienceleague.adobe.com/VRC82qSYkgsI0ceaXdKtfGq-aYlw-Y0M-nRtq1pjg7A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 2%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *` テンプレート `*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> テンプレート </span></span> </p> </td> 
   <td> <p>情報サーバーから返されたデータが結合されるコンテンツテンプレート。 </p> <p>コンテンツテンプレートは、このDTDに続くXMLです。 </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>コンテンツテンプレートの実際の構文は次のとおりです。 </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>つまり、テンプレートは、オプションのデフォルト <span class="codeph"> &lt;var&gt;</span>要素を含む<span class="codeph"> &lt;info&gt;</span>要素で開始する必要があります。 テンプレートコンテンツ自体、<span class="codeph"> TEMPLATE_CONTENT</span>はHTML テキストです。 さらに、コンテンツテンプレートには、<span class="codeph"> $</span>文字で囲まれた変数名を含めることができます。 これらの文字は、情報サーバーが返す変数値またはデフォルトの変数値に置き換えられます。 </p> <p>テンプレートで定義されるデフォルト変数は、グローバル変数（ロールオーバー属性が設定されていない場合）または特定のロールオーバーキーに固有の変数（ロールオーバー属性が存在する場合）です。 </p> <p>テンプレート処理中に、キーのロールオーバーに固有の変数がグローバル変数よりも優先されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>情報パネルポップアップを設定すると、情報パネルに渡されるHTML コードとJavaScript コードがクライアントのコンピューターで実行されることに注意してください。 したがって、このようなHTML コードとJavaScript コードが安全であることを確認してください。

## プロパティ {#section-6dd7785357d740d095fa9f7fd0f67da4}

オプション。

## 初期設定 {#section-cd5db06d08aa4de49e37d6c938b41570}

なし

## 例 {#section-16d184665c484964af9a22f79ff3f840}

情報サーバー応答が製品名を変数`$1$`として返し、製品画像URLを変数`$2$`として返すと仮定します。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`

