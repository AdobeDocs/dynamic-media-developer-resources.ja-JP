---
title: 光沢
description: マテリアル表面の光沢度。 マテリアル サーフェスの相対的な光沢度を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
TQID: 'https://experienceleague.adobe.com/-69G38JBpD4-X1wvkFtfvvZpdbHs7pcPiHnbNDgGRCA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# 光沢{#gloss}

マテリアル表面の光沢度。 マテリアル サーフェスの相対的な光沢度を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>デフォルト（参照）光沢値の光沢（0...100%）または–1。 </p></td> 
 </tr> 
</table>

光沢値が大きいほど、反射がより強くシャープになり、周辺光沢効果が有効になっている場合は、主に照明コントラストを上げることで、マテリアル表面のスペキュラ ハイライトが強くなります。 各マテリアルタイプ（`type=`）は、最小および最大のレンダリング効果を定義します。 一部のマテリアルタイプ（壁紙など）では、`gloss=`がレンダリング効果の外観に与える影響は最小限ですが、他のマテリアルタイプ（石やセラミックなど）では、効果は大幅に顕著です。

ビネットが複数のイルミネーション マップを定義している場合、`gloss=`は、現在のレンダリング操作に使用するイルミネーション マップを選択します。 `illum=-1`レンダラーは、光沢値が指定した光沢に最も近い照明マップを選択します。

`gloss=-1`選択した照明マップの参照光沢値を、ビネットのビュープロパティで定義されているとおりに選択します。 この値を使用すると、光沢効果が有効になっている場合でも、照明マップが作成済みとまったく同じように使用されます。追加の変更は必要ありません。 `illum=-1`の場合、周辺光量補正ビューの最初の照明マップの参照光沢値が使用されます。

## プロパティ {#section-92c20c7890fc4aad8d1725d1a1f82da6}

マテリアル属性： 周辺光量補正で複数のイルミネーション マップが定義されない場合は無視されます。 または、`illum=`が指定されている場合、ビネットに3D反射データが含まれていない場合。 または、現在のオブジェクトが3D反射をサポートしていない場合、または周辺光量補正で光沢効果が無効になっている場合です。

## 初期設定 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` マテリアルがカタログ エントリに基づいている場合、そうでない場合は、既定の照明マップの参照光沢値または`illum=`で指定された照明マップ。

## 関連項目 {#section-29f5b761481a4c52a499a2e16e63c70b}

[属性：：光沢](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)、[ タイプ=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)、[ ラフ=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)、[glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)、[illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)

