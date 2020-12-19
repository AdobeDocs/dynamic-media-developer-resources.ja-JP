---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: feeb02c0-f3f9-4559-acd9-cad30788b70b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 5%

---


# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`期間`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> フレーム変更時に適用する効果のタイプを指定します。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> ス</span> ライドにより、前のフレームが表示からスライドアウトし、新しいフレームが表示にスライドインするトランジションがアクティブになります。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> ページのフリップ効果を</span> 有効にすると、ユーザーが四隅の1つをドラッグして、インタラクティブなページのフリップを実行できます。 </p> <p><span class="codeph"> turn</span>を使用する場合、コンポーネントの外観は<span class="codeph"> pageturnstyle</span>修飾子を使用して制御され、<span class="codeph"> .s7pagedivider</span> CSSクラスは無視されます。 </p> <p>注意：  <p><span class="codeph"> Motorola Xoomでは、</span> 自動アニメーションはサポートされていません。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> デスクトップシステムではターンフレームトランジション、タッチデバイスではスライドトランジションを</span> 自動設定します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> slide</span>または<span class="codeph"> turn</span>トランジション効果の時間を秒単位で指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4d25a3f483834d2b9586fa70270ce6bd}

（オプション）

## 初期設定 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 例 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
