---
description: レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの設定に加え、layer=コマンドで合成順序（z順序）を指定する以外に、レイヤを回転(rotate=)したり反転(flip=)したりできます。
solution: Experience Manager
title: レイヤー操作
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# レイヤー操作{#layer-operations}

レイヤ0に対するサイズ(size=)と位置(pos=)のレイヤの設定に加え、layer=コマンドで合成順序（z順序）を指定する以外に、レイヤを回転(rotate=)したり反転(flip=)したりできます。

`origin=`属性と`anchor=`属性を使用して、テンプレートで画像やテキストが動的に変更された場合に、レイヤー間での適切な配置を維持できます。

`maskUse=`コマンドは、別々のマスクを持つ画像の背景領域に、画像レイヤーがアクセスする場合に使用できます。

`opac=` を使用して、レイヤーの不透明度を変更したり、レイヤーの表 `hide=` 示/非表示を切り替えたりできます。
