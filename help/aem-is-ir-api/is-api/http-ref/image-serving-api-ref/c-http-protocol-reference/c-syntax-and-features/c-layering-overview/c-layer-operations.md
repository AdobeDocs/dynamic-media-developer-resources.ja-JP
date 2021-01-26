---
description: レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの相対的な位置(pos=)に加えて、layer=コマンドで合成順序（z順序）を指定すると、レイヤを回転（回転=）して反転（反転=）できます。
seo-description: レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの相対的な位置(pos=)に加えて、layer=コマンドで合成順序（z順序）を指定すると、レイヤを回転（回転=）して反転（反転=）できます。
seo-title: レイヤーの操作
solution: Experience Manager
title: レイヤーの操作
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# レイヤ操作{#layer-operations}

レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの相対的な位置(pos=)に加えて、layer=コマンドで合成順序（z順序）を指定すると、レイヤを回転（回転=）して反転（反転=）できます。

テンプレートで画像やテキストが動的に変更される場合、`origin=`属性と`anchor=`属性を使用して、レイヤー間の希望の配置を維持できます。

`maskUse=`コマンドは、画像レイヤーが、別々のマスクを持つ画像の背景領域にアクセスするために使用できます。

`opac=` を使用して、レイヤーの不透明度を変更したり、レイヤーの表示/非表示 `hide=` を切り替えたりできます。
