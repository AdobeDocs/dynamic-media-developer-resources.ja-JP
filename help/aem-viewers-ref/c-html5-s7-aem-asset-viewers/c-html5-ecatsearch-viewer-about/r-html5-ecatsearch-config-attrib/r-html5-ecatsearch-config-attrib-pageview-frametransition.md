---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
TQID: 'https://experienceleague.adobe.com/X3qkuLchMxlcb-CpwM4-KLGNphsJe-DJMD3fsYz7KyY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`期間`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> スライド|ターン|自動</span> </p> </td> 
   <td colname="col2"> <p> フレーム変更に適用されるエフェクトのタイプを指定します。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> スライド </span>は、古いフレームがスライドして見えなくなり、新しいフレームがスライドして表示されるトランジションをアクティブにします。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p>ユーザーが4つのスプレッドコーナーのいずれかをドラッグしてインタラクティブなページフリップを実行できる場合、<span class="codeph"> turn</span>はページフリップエフェクトを有効にします。 </p> <p><span class="codeph"> turn</span>が使用されている場合、コンポーネントの外観は<span class="codeph"> pageturnstyle</span>修飾子で制御され、<span class="codeph"> .s7pagedivider</span> CSS クラスは無視されます。 </p> <p>注意：  <p>Motorola Xoomでは、<span class="codeph"> turn</span> アニメーションはサポートされていません。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span>は、デスクトップシステムのフレームの切り替えトランジションとタッチデバイスのスライドの切り替えを設定します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname">期間</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> スライド </span>または<span class="codeph"> ターン </span>のトランジション効果のデュレーションを秒単位で指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4d25a3f483834d2b9586fa70270ce6bd}

オプション。

## 初期設定 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]

