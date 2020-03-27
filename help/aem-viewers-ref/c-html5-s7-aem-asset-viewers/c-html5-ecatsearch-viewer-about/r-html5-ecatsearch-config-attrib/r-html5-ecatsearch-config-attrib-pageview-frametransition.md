---
description: 'null'
seo-description: 'null'
seo-title: PageView.frametransition
solution: Experience Manager
title: PageView.frametransition
topic: Dynamic media
uuid: 12595a89-bad5-4224-aeff-52ce6bb615ee
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.frametransition{#pageview-frametransition}

[!DNL ` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`期間`*]`]

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> フレーム変更時に適用する効果のタイプを指定します。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slideは</span> 、前のフレームをビューからスライドアウトし、新しいフレームをスライドインして表示するトランジションをアクティブにします。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> turnは</span> 、ユーザが四隅のいずれかをドラッグして、インタラクティブなページフリップを実行できる場合に、ページフリップ効果を有効にします。 </p> <p>turnを使 <span class="codeph"> 用する</span> と、コンポーネントの外観はpageturnstyle修飾子で制御され、 <span class="codeph"> .s7pagedivider</span><span class="codeph"></span> CSSクラスは無視されます。 </p> <p>注意：  <p><span class="codeph"> turnアニメーション</span> は、Motorola Xoomではサポートされていません。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> autoは、デスクトップ</span> システムではターンフレームトランジションを設定し、タッチデバイスではスライドトランジションを設定します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p>スライドまたは回転のトランジション効果の時 <span class="codeph"> 間を</span> 秒単位 <span class="codeph"> で指定します</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4d25a3f483834d2b9586fa70270ce6bd}

（オプション）

## 初期設定 {#section-d677f04f1c894966884ce9d77a5ea1c1}

[!DNL `slide,0.3`]

## 例 {#section-b877011e5f6240718e9451be8f622c02}

[!DNL `frametransition=auto,1`]
