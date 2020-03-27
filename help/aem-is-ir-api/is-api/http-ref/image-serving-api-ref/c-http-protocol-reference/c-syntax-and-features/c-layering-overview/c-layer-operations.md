---
description: レイヤー0に対するサイズ調整(size=)と位置調整(pos=)、layer=コマンドで合成順序（z順序）を指定する以外に、レイヤーを回転（回転=）して反転（反転=）することができます。
seo-description: レイヤー0に対するサイズ調整(size=)と位置調整(pos=)、layer=コマンドで合成順序（z順序）を指定する以外に、レイヤーを回転（回転=）して反転（反転=）することができます。
seo-title: レイヤーの操作
solution: Experience Manager
title: レイヤーの操作
topic: Scene7 Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# レイヤーの操作{#layer-operations}

レイヤー0に対するサイズ調整(size=)と位置調整(pos=)、layer=コマンドで合成順序（z順序）を指定する以外に、レイヤーを回転（回転=）して反転（反転=）することができます。

テンプレート `origin=` 内で画像やテキ `anchor=` ストが動的に変更される場合、属性と属性を使用して、レイヤー間の希望の配置を維持できます。

このコマ `maskUse=` ンドは、画像レイヤーで、別々のマスクを持つ画像の背景領域にアクセスする場合に使用できます。

`opac=` を使用して、レイヤーの不透明度を変更したり、レイヤーの表示/ `hide=` 非表示を切り替えたりできます。
