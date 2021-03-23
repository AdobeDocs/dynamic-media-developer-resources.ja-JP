---
description: レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの相対的な位置(pos=)に加えて、layer=コマンドで合成順序（z順序）を指定すると、レイヤを回転（回転=）して反転（反転=）できます。
seo-description: レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの相対的な位置(pos=)に加えて、layer=コマンドで合成順序（z順序）を指定すると、レイヤを回転（回転=）して反転（反転=）できます。
seo-title: レイヤーの操作
solution: Experience Manager
title: レイヤーの操作
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# レイヤ操作{#layer-operations}

レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの相対的な位置(pos=)に加えて、layer=コマンドで合成順序（z順序）を指定すると、レイヤを回転（回転=）して反転（反転=）できます。

テンプレートで画像やテキストが動的に変更される場合、`origin=`属性と`anchor=`属性を使用して、レイヤー間の希望の配置を維持できます。

`maskUse=`コマンドは、画像レイヤーが、別々のマスクを持つ画像の背景領域にアクセスするために使用できます。

`opac=` を使用して、レイヤーの不透明度を変更したり、レイヤーの表示/非表示 `hide=` を切り替えたりできます。
