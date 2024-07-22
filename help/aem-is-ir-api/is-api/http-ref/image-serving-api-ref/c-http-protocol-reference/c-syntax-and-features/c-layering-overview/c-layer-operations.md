---
description: レイヤ 0 を基準にしてレイヤのサイズ変更（size=）と位置（pos=）を行い、layer= コマンドで合成順序（z 順）を指定する以外に、レイヤの回転（rotate=）と反転（flip=）を行うことができます。
solution: Experience Manager
title: レイヤーの操作
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# レイヤーの操作{#layer-operations}

レイヤ 0 を基準にしてレイヤのサイズ変更（size=）と位置（pos=）を行い、layer= コマンドで合成順序（z 順）を指定する以外に、レイヤの回転（rotate=）と反転（flip=）を行うことができます。

`origin=` 属性と `anchor=` 属性を使用すると、テンプレートで画像やテキストが動的に変更される際に、レイヤー間の適切な配置を維持できます。

`maskUse=` コマンドは、画像レイヤーが、個別のマスクを持つ画像の背景領域にアクセスするために使用できます。

`opac=` を使用して、レイヤーの不透明度を変更したり、レイヤーを表示または非表示にしたりで `hide=` ます。
