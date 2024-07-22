---
title: コマンドリファレンス
description: ここでは、HTTP プロトコル・コマンドについて説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# コマンドリファレンス{#command-reference}

ここでは、HTTP プロトコル・コマンドについて説明します。

>[!TIP]
>
>Dynamic Media [_Snapshot_](https://snapshot.scene7.com/) を使用して、Dynamic Mediaの画像修飾子とスマートイメージングのメリットを体験してみましょう。
>
> スナップショットは、最適化された動的な画像配信におけるDynamic Mediaのパワーをわかりやすく伝えるために作られた、視覚的なデモツールです。 テスト画像やDynamic Mediaの URL を試して、様々なDynamic Media画像修飾子の出力を視覚的に観察し、次の項目に対するスマートイメージング最適化を確認します。
>* ファイルサイズ （WebP および AVIF 配信を使用）
>* ネットワーク帯域幅
>* DPR （デバイスピクセル比）
>
>スナップショットの使用がどれほど簡単かを知るには、[ スナップショットのトレーニングビデオ ](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) （3 分 17 秒）を再生してください。


**Adobe Experience ManagerのDynamic Mediaのみ** - ユーザーインターフェイスで使用できる基本画像設定以外に、AEM（[!DNL Adobe Experience Manager]）の [!DNL Dynamic Media] では、「**画像修飾子**」フィールドで指定できる高度な画像修正が多数サポートされています。 これらのパラメーターは、以下で定義されます。 ただし、次の機能はAEMのDynamic Mediaではサポートされていません。

* カラー補正コマンド：`icc=` および `iccEmbed=`。
* 基本テンプレートおよびテキストレンダリングコマンド：`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` および `textPs=`。
* ローカリゼーションコマンド：`locale=` および `req=xlate`。
* `req=set` は、一般的には使用できません。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非コア Dynamic Media サービス：SVG、画像レンダリングおよび Web-to-Print。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

AEM 6.5 ドキュメントのDynamic Media[ 画像プリセットオプション ](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) も参照してください。

* [align](r-align.md)
* [アンカー](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [キャッシュ](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [切り抜き](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
* [効果](r-effect.md)
* [effectMask](r-effectmask.md)
* [extend](r-extend.md)
* [発作](r-fit.md)
* [反転](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [ヘイ](r-is-http-hei.md)
* [非表示](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [レイヤー](r-layer.md)
* [ロケール](r-locale.md)
* [マップ](r-map.md)
* [マスク](r-mask.md)
* [maskUse](r-maskuse.md)
* [ネットワーク](r-network.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [起源](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [透視図](r-perspective.md)
* [位置](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [量子化](r-is-http-quantize.md)
* [rect](r-rect.md)
* [要](r-req/r-req.md)
* [件の](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [循環](r-rotate.md)
* [スケール](r-is-http-scale.md)
* [scl](r-scl.md)
* [サイズ](r-size-reference.md)
* [src](r-src.md)
* [テンプレート](r-template.md)
* [テキスト](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [タイプ](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
