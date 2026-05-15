---
title: コマンド参照
description: この節では、HTTP プロトコルコマンドについて説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
TQID: 'https://experienceleague.adobe.com/NURaQ7eznu6tyM5IhrlLMxaZ1L38L7t9lHb826jSyfs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 3%

---

# コマンド参照{#command-reference}

この節では、HTTP プロトコルコマンドについて説明します。

>[!TIP]
>
>Dynamic Media [_スナップショット_](https://snapshot.scene7.com/)を使用して、Dynamic Media画像修飾子とスマートイメージングのメリットを試してみて確認します。
>
> Snapshotは、最適化されたダイナミックな画像配信を実現するDynamic Mediaの機能を示すように設計された、視覚的なデモンストレーションツールです。 テスト画像またはDynamic Media URLを試して、様々なDynamic Media画像修飾子の出力を視覚的に確認し、次の点に関するスマートイメージングの最適化を確認します。
>* ファイルサイズ（WebPおよびAVIF配信用）
>* ネットワーク帯域幅
>* DPR （デバイスピクセルレシオ）
>
>スナップショットを簡単に使用する方法を説明するには、[&#x200B; スナップショットトレーニングビデオ &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en)を再生します（3分17秒）。


**Adobe Experience ManagerのDynamic Mediaの場合のみ** - ユーザーインターフェイスで使用できる基本的な画像設定を超えて、AEM （[!DNL Adobe Experience Manager]）の[!DNL Dynamic Media]では、**画像修飾子** フィールドで指定できる多数の高度な画像変更がサポートされています。 これらのパラメーターは以下で定義されます。 ただし、次の機能は、AEMのDynamic Mediaではサポートされていないことに注意してください。

* 色補正コマンド：`icc=`および`iccEmbed=`。
* 基本的なテンプレートとテキスト レンダリング コマンド：`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`および`textPs=`。
* ローカリゼーションコマンド：`locale=`および`req=xlate`。
* `req=set`は一般的な使用には使用できません。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* コア以外のDynamic Media サービス：SVG、画像レンダリング、Web-to-Print。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

AEM 6.5 ドキュメントのDynamic Media [画像プリセットオプション &#x200B;](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic)も参照してください。

* [整列](r-align.md)
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
* [エフェクト](r-effect.md)
* [effectMask](r-effectmask.md)
* [拡張](r-extend.md)
* [フィット](r-fit.md)
* [反転](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [へい](r-is-http-hei.md)
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
* [オリジン](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [遠近法](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [量子化](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [循環](r-rotate.md)
* [拡大・縮小](r-is-http-scale.md)
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
