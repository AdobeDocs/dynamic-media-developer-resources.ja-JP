---
title: サブ
description: サブ選択： 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用したり、以前に適用したマテリアルを削除したりできます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9968fbb-c38b-4180-81be-19992fa8f347
TQID: 'https://experienceleague.adobe.com/1vZwrwUBziB5UYudKf6n-eKQP2Weluqjo1iiVDMSUms'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 6%

---

# サブ{#sub}

サブ選択： 選択したオブジェクトまたはグループの異なる領域に異なるマテリアルを適用したり、以前に適用したマテリアルを削除したりできます。

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>壁全体を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>壁の上半分を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>壁の下半分を選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>上部の壁の境界線エリアを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>中央の壁の境界線エリアを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>下部の壁の境界線エリアを選択します。 </p> </td> 
 </tr> 
</table>

現在、壁オブジェクトでのみサポートされています。 前のMSSを終了し、指定された部分選択に適用されるマテリアルの新しいMSSを開始します。

上壁または下壁のいずれかに指定されたマテリアルは、壁の残りの半分にも別のマテリアルが指定されていない限り、壁全体に適用されます。

## プロパティ {#section-b202139d6d0847cc8d520a154104ab9d}

選択コマンド、MSS区切り記号。

## 初期設定 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 関連項目 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)

