---
description: この節では、HTTPプロトコルのコマンドについて説明します。
solution: Experience Manager
title: コマンドリファレンス
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 10%

---

# コマンドリファレンス{#command-reference}

この節では、HTTPプロトコルのコマンドについて説明します。

**AEMのDynamic Mediaのみ**:ユーザーインターフェイスで使用できる基本的な画像設定のほか、AEM()で [!DNL Dynamic Media] は、「画像の変 [!DNL Adobe Experience Manager]更」フィールドで多数の高度な画像変更を指定で **き** ます。これらのパラメーターは以下で定義します。 ただし、次の機能はAEMのDynamic Mediaではサポートされていません。

* カラー補正コマンド：`icc=`と`iccEmbed=`が表示されます。
* 基本的なテンプレートコマンドとテキストレンダリングコマンド：`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`と`textPs=`が表示されます。
* ローカライゼーションコマンド：`locale=`と`req=xlate`が表示されます。
* `req=set` は、一般的には使用できません。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* コア以外のDynamic Mediaサービス：SVG、画像レンダリング、Web-to-Print。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

AEM 6.5のドキュメントのDynamic Media [画像プリセットオプション](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic)も参照してください。

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
* [効果](r-effect.md)
* [effectMask](r-effectmask.md)
* [拡張](r-extend.md)
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
* [層](r-layer.md)
* [ロケール](r-locale.md)
* [マップ](r-map.md)
* [マスク](r-mask.md)
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
* [origin](r-origin.md)
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
* [循環](r-rotate.md)
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
* [タイプ](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
