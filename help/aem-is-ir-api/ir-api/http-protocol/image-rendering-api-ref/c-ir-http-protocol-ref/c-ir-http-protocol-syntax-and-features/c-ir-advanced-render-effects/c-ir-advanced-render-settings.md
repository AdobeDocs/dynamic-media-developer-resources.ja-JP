---
title: レンダリングの詳細設定
description: ビネットオーサリングツール（Dynamic Media画像オーサリングパッケージの一部）は、ビネットレンダリングエンジンの低レベル要素を制御するメカニズムを提供します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ad8f4b4-dd9c-43f5-aacc-67a564e34d92
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 17%

---

# レンダリングの詳細設定{#advanced-render-settings}

ビネットオーサリングツール（Dynamic Media画像オーサリングパッケージの一部）は、ビネットレンダリングエンジンの低レベル要素を制御するメカニズムを提供します。

>[!NOTE]
>
>レンダリング設定は、画像レンダリングと画像オーサリングの詳細機能です。 レンダリング設定の使用に関するトレーニング、コンサルティング、またはその両方について、AdobeのテクニカルサポートまたはAdobeのコンサルティング担当者にお問い合わせください。

これらの設定は、画像オーサリングでインタラクティブに制御されます。 `rs=` コマンド（または `catalog::RenderSettings` の値）を使用して、画像レンダリングに同じ設定を適用することができます。 このメカニズムを使用すると、マテリアルごとに異なるシャープ オプションを選択し、ハイライトの彩度やシャドウのコントラストの変化など、照明レンダリング アルゴリズムの動作を変更することができます。

## 詳細レンダリング設定（rs=）値 {#section-d9e7f341ebd44f07a4e90f1f5910726b}

<table id="table_1517FC39C7344EBB9F17BE20415DB057"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>コード </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
   <th colname="col3" class="entry"> <p>最小値 </p> </th> 
   <th colname="col4" class="entry"> <p>最大値 </p> </th> 
   <th colname="col5" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col2"> <p>Render Effects/Alternate Shader は、ビネットの設定をオーバーライドします。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>A0=レンダリング効果 </p> <p>A1=代替シェーダ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U </p> </td> 
   <td colname="col2"> <p>USM （アンシャープマスク）。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>2 </p> </td> 
   <td colname="col5"> <p>USM を使用するには、U が 0 より大きい必要があります </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>W </p> </td> 
   <td colname="col2"> <p>USM 金額（%）。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>500 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V </p> </td> 
   <td colname="col2"> <p>USM 半径（ピクセル）。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>X </p> </td> 
   <td colname="col2"> <p>USM 閾値（レベル）。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q </p> </td> 
   <td colname="col2"> <p>サイズ変更モード </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_87184BB93E7F46D59BA1AAAFA8455512"> 
      <li id="li_E7711C3678ED4DE09E710F7C430CEF42">最近接ルータ </li> 
      <li id="li_CAE975B91C604DA0AA493F700AEBE199">双線形 </li> 
      <li id="li_24E5A40B8A3F4C808A68686C27647CD5">バイキュービック法 </li> 
      <li id="li_42ACFCE65B4843ACAFA6A52255364642">スーパーサンプリング （既定値） </li> 
      <li id="li_34EC85C4D15145DF80F7D3DB7B6244D3">ランチョス窓 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>R </p> </td> 
   <td colname="col2"> <p>再サンプリングモード。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_FD4A9D73C32F47C3BF13776BB4D2818D"> 
      <li id="li_F08AD1D093D74059B60302374B472B52">初期設定 </li> 
      <li id="li_FD4C859D975B44399475D4D93D6B05AB">最近接ルータ </li> 
      <li id="li_CA93566F5D4F4D3CAA1D0816562A3851">双線形 </li> 
      <li id="li_D334ACF969E749A89A464B21C96CE8A6">スーパーサンプリング </li> 
      <li id="li_FAC72C36FF4A418F8A5B05F3B4E7C5D8">アダプティブ </li> 
      <li id="li_6E9D81045A0C4804A4D35D9B239F6486">ポアソンSampler </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>スーパーサンプリング：ランダム </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>200 </p> </td> 
   <td colname="col5"> <p>初期設定は 0。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>スーパーサンプリング：ランダムレート。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>20 </p> </td> 
   <td colname="col5"> <p>初期設定は 5。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>M </p> </td> 
   <td colname="col2"> <p>アダプティブリサイズ：深度。 </p> </td> 
   <td colname="col3"> <p>4 </p> </td> 
   <td colname="col4"> <p>8 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>N </p> </td> 
   <td colname="col2"> <p>アダプティブリサイズ：幅。 </p> </td> 
   <td colname="col3"> <p>2 </p> </td> 
   <td colname="col4"> <p>10 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>P </p> </td> 
   <td colname="col2"> <p>ポアソン：サンプル/ピクセル </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>4 </p> </td> 
   <td colname="col5"> <p>初期設定は 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Y </p> </td> 
   <td colname="col2"> <p>ポアソン：切り替えを使用します。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>初期設定は 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> レンダリング エフェクト（古いシェーダ） </b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I </p> </td> 
   <td colname="col2"> <p>ハイライト。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>J </p> </td> 
   <td colname="col2"> <p>彩度をハイライトします。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>50 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H </p> </td> 
   <td colname="col2"> <p>明るいマテリアルの影。 </p> </td> 
   <td colname="col3"> <p>50 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>K </p> </td> 
   <td colname="col2"> <p>影の彩度。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>400 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>光沢ベースの外挿強度。 </p> </td> 
   <td colname="col3"> <p>100 </p> </td> 
   <td colname="col4"> <p>600 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0 </p> </td> 
   <td colname="col2"> <p>輝度補正（チェックボックス） </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p>デフォルトはオン（空白）で、選択解除= F100G0 です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b> 代替シェーダ </b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Z </p> </td> 
   <td colname="col2"> <p>基本コントラスト。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>初期設定は 50。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>a </p> </td> 
   <td colname="col2"> <p>明るさ補正。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の相違：a36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>b </p> </td> 
   <td colname="col2"> <p>彩度調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の相違：b36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>c </p> </td> 
   <td colname="col2"> <p>影の調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の相違：c36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>d </p> </td> 
   <td colname="col2"> <p>ハイライト調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の相違：d36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>e </p> </td> 
   <td colname="col2"> <p>鏡面反射光ハイライト </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の相違：e36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>xx </p> </td> 
   <td colname="col2"> <p>シェイプ： </p> </td> 
   <td colname="col3"> <p>-100 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>上記の値については「xx」を参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> <p>照明調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の違い：k64.138.175.60.xx.133.242 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>u &amp; s </p> </td> 
   <td colname="col2"> <p>シャドウの色相のシフト。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の違い：u8.1.2.3.4.5.6.7.8.s8.1.2.3.4.5.6.7.8。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>v &amp; t </p> </td> 
   <td colname="col2"> <p>ハイライトの色相シフト。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>形式の違い：v8.1.2.3.4.5.6.7.8.t8.1.2.3.4.5.6.7.8。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>w </p> </td> 
   <td colname="col2"> <p>彩度調整。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>g </p> </td> 
   <td colname="col2"> <p>彩度ブーストが低い。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 詳細レンダリング設定のサンプル {#section-56528569eae44ecd997a289b211ff256}

<table id="table_062DCF66ACCC4A6997E3CA951C0A12B8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>構成の設定 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>H60I30J10K200L400U1V10W100X0 </p> </td> 
   <td colname="col2"> <p>画像オーサリングのデフォルト値。 
     <ul id="ul_AA7CF1A3E6984B318265BBE8FFFBB4EE">
      <li> USM1
      <li id="li_8EC075956E2E4D5A91355122DC9BC938">H60 =明るいマテリアルの影（50 ～ 100） </li> 
      <li id="li_F760B65E057146A7B56673D6B1A9A304">I30 = ハイライト（0 ～ 100） </li> 
      <li id="li_376C275FDB3548958C09BD266C77318F">J10 =彩度をハイライト（0 ～ 50）。 </li> 
      <li id="li_FE26429972F544869CDFE2DD61F39CC5">K200 =影の彩度（0～400） </li> 
      <li id="li_FB6BAA708427428AA4A3AC2E5D3B9932">L400 = グロス ベースの外挿強度（100 ～ 600） </li> 
      <li id="li_6B2EEEE7F0D54E078462AAFC4E4FAB42">U1 = USM （アンシャープマスク）（0-2）。 </li> 
      <li id="li_7CD4E3662A6C48F9B5895D133D28BA2A">V10 = USM 半径（1～100 ピクセル） </li> 
      <li id="li_949B6DB4959B46A892787CD5B3AD7485">W100 = USM 金額（1%-500%）。 </li> 
      <li id="li_F39D3834D4A2478D993E5E9C9B434CFE">X0 = USM しきい値（0～255 レベル）。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C6E6DD90ECAB4D2B9284A25A29923DC6"> 
      <li id="li_7B7A8C43BCEB4CB58C7074974CAB0419">USM1 </li> 
      <li id="li_A003B68023424DCABBF3A2CAF98C39A4">最大および明るさの補正がすべてオンになります。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_AAEC098CED1C436E933B1C1B88DFB659"> 
      <li id="li_0CC34CDD796E4DFD802824FF21DB021B">USM1 </li> 
      <li id="li_E36886FB1D00444CBA19D7245E89B292">最大および明るさの補正はすべてオフです。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H100I100J50K400L600U2V100W500X255 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6BB668C6C055493DAAA38F4D3B9C20A7"> 
      <li id="li_D8BAFB41CF4C4B3FAD6F89AF5D7F223A">USM2 </li> 
      <li id="li_DA685F4DE4BA427BA7BE241A75C96152">最大および明るさの補正はすべてオフです。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H80I70J40L300U1V8W80X5 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7C374842312E4AD0B62692BBCE6743A8"> 
      <li id="li_CC730580B54741FBBBFF507DE0FE1F15">H80 = USM 金額 </li> 
      <li id="li_C2801B2C093444AC9401793BC571EC27">I70 = ハイライト </li> 
      <li id="li_518C6A690EC34614B0806A0C6BC535FF">J40 =彩度をハイライト </li> 
      <li id="li_F280CF29D1E341D9AC9C0C16C2DEA1E6">L300 = グロス ベースの外挿強度 </li> 
      <li id="li_3F589F109AC94280911BD535C49E42E4">U1 = USM </li> 
      <li id="li_113FEC9B37D54511BAB3FEAC7C271858">V8 = USM 半径 </li> 
      <li id="li_E1BA7406A76B476EB1A89D6EDD87930C">W80 =明るいマテリアルの影 </li> 
      <li id="li_AAD479EF6A7F43B98A8C147FCD684ECA">X5 = USM しきい値 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q5R3S11T103U1V6W120X5Z80b.188.88.75.37 </p> </td> 
   <td colname="col2"> <p>シャープ付き代替シェーダ： </p> <p> 
     <ul id="ul_93AD53BB37EA47F6A3CEE424D3AAE18C"> 
      <li id="li_9EF1DF4167164721882E4842C2E0B20C">USM1 </li> 
      <li id="li_7B5D8B7BB5544E7FA4AD702EE281086B">USM 金額（120） </li> 
      <li id="li_B3BE096BB0654A2DBADDD6832E499F2A">USM 半径（0.6） </li> 
      <li id="li_793DAB145CE7469ABC1182BCBD324657">USM しきい値（5） </li> 
      <li id="li_B1954FEBE2084726828D64E8165DA4DA">サイズ変更（ランチョス） </li> 
      <li id="li_E5ED76998C0543D8A3F9AD178CFD3C2C">リサンプル（スーパーサンプリング、ランダム=半分、レート=半分） </li> 
      <li id="li_CCEE53544E7D48858398BF3168F1E87D">コントラスト （強） </li> 
      <li id="li_EB0D25C095FB4D5798AC031AB759849B">彩度調整（中央の 1 番目の頂点、エッジに沿った 2 番目の頂点、中央の 3 番目の頂点） </li> 
      <li id="li_5C2304DA4A4D4799AE5DCCCB1E2ECBB3">シャープ （右に 3/4） </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- RB: I don't know why this is in here; it was added by someone else: 
Alternate Shader Rendering (default on) checkbox provides a more precise Advanced Shader diffuse rendering pipeline. For a number of effects it also provides an alternate Advanced Shader rendering pipeline. Note that the underlying OpenGL hardware must provide support for the Advanced (Per-Pixel) GLSL Shaders for this option to be vailable; else this checkbox is automatically disabled. -->

<!-- RB: I don't know why this is in here; it was added by someone else:
It should probably also go into the different renders - Render Effects and Alternate Shader - or link to descriptions of each. -->
