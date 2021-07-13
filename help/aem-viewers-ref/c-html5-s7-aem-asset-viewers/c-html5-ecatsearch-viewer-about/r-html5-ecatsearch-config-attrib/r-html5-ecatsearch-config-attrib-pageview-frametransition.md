---
description: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog検索
role: Developer,User
exl-id: 19239fa8-65a8-487f-9370-42bb93d862d5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`期間`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> フレームの変更時に適用される効果のタイプを指定します。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> </span> スライドを使用すると、前のフレームがビューからスライドアウトし、新しいフレームがスライドインして表示するトランジションがアクティブになります。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> </span> を自動的にオンにすると、4つの見開き隅の1つをドラッグして、インタラクティブなページ反転を実行できます。 </p> <p><span class="codeph"> turn</span>を使用すると、コンポーネントの外観が<span class="codeph"> pageturnstyle</span>修飾子で制御され、 <span class="codeph"> .s7pagedivider</span> CSSクラスは無視されます。 </p> <p>注意：  <p><span class="codeph"> </span> Motorola Xoomでは、自動アニメーションはサポートされていません。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> </span> は、デスクトップシステムではターンフレームトランジションを、タッチデバイスではスライドトランジションを自動設定します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">スライド</span>または<span class="codeph">ターン</span>トランジション効果の時間を秒単位で指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4d25a3f483834d2b9586fa70270ce6bd}

（オプション）

## 初期設定 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
