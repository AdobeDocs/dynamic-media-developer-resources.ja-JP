---
description: この節では、HTTPプロトコルのコマンドについて説明します。
seo-description: この節では、HTTPプロトコルのコマンドについて説明します。
seo-title: コマンドリファレンス
solution: Experience Manager
title: コマンドリファレンス
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 10%

---


# コマンドリファレンス{#command-reference}

この節では、HTTPプロトコルのコマンドについて説明します。

**AEMのDynamic Mediaのみ**:ユーザインターフェイスで使用できる基本的な画像設定の他に、AEM [!DNL Dynamic Media] ( [!DNL Adobe Experience Manager])では、「 **画像** 修飾子」フィールドで指定できる多数の高度な画像変更をサポートしています。これらのパラメーターは次のように定義します。 ただし、次の機能はAEMのDynamic Mediaではサポートされていません。

* カラー補正コマンド：`icc=`と`iccEmbed=`。
* 基本的なテンプレート化およびテキストレンダリングコマンド：`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`と`textPs=`。
* ローカライゼーションコマンド：`locale=`と`req=xlate`。
* `req=set` は一般的な使用方法には使用できません。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非コアDynamic Mediaサービス：SVG、画像レンダリング、Web-to-Print。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

AEM 6.5ドキュメントのDynamic Media[画像プリセットオプション](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options)も参照してください。

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
* [effect](r-effect.md)
* [effectMask](r-effectmask.md)
* [延長する](r-extend.md)
* [フィット](r-fit.md)
* [反転](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [非表示](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [layer](r-layer.md)
* [locale](r-locale.md)
* [マップ](r-map.md)
* [mask](r-mask.md)
* [maskUse](r-maskuse.md)
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
* [接触チャネル](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [視点](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [量子化する](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
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
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
