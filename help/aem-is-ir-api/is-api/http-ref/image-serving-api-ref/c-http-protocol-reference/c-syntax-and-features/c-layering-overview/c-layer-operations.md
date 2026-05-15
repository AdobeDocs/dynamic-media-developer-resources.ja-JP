---
description: レイヤー0に対してサイズ変更（size=）および配置（pos=）レイヤーを指定し、layer= コマンドで合成順序（z次）を指定することに加えて、レイヤーを回転（rotate=）および反転（flip=）できます。
solution: Experience Manager
title: レイヤー操作
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
TQID: 'https://experienceleague.adobe.com/uuGkOMzbkysv9BpR8zEK6dkuKgnseu3qwqLslA5W6zw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# レイヤー操作{#layer-operations}

レイヤー0に対してサイズ変更（size=）および配置（pos=）レイヤーを指定し、layer= コマンドで合成順序（z次）を指定することに加えて、レイヤーを回転（rotate=）および反転（flip=）できます。

テンプレートで画像またはテキストが動的に変更される場合、`origin=`属性と`anchor=`属性を使用して、レイヤー間で必要な整列を維持できます。

画像レイヤーが個別のマスクを持つ画像の背景領域にアクセスするには、`maskUse=` コマンドを使用できます。

`opac=`を使用してレイヤーの不透明度を変更し、`hide=`を使用してレイヤーの表示と非表示を切り替えることができます。
