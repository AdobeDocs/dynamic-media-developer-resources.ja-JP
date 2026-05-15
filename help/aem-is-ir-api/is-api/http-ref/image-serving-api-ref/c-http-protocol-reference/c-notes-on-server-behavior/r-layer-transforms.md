---
description: 変換は、ソースイメージとテキストレイヤーに適用されます。
solution: Experience Manager
title: レイヤーの変形
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: 'https://experienceleague.adobe.com/jChFcZzWWOlbicpu0WeRSJb608dGT9JmVSItV-uEjBY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# レイヤーの変形{#layer-transforms}

変換は、ソースイメージとテキストレイヤーに適用されます。

次の操作を指定された順序でソース画像に適用して、レイヤー0との目的の空間関係を実現します。

1. 指定した場合は、`crop=`を適用します。
1. `size=`に基づいて拡大・縮小するか、`size=`が指定されていない場合は`scale=`に基づいて拡大・縮小するか、`scale=`が指定されていない場合は`res=`に基づいて拡大・縮小するか、`res=`が指定されていない場合は、フル解像度のソース画像を使用します。
1. 指定した場合は、`flip=`を適用します。
1. 指定した場合は、`rotate=`を適用します。
1. 指定した場合は、`extend=`を適用します。
1. `origin=`と`pos=`に基づいてカンバス内のレイヤーを配置します（以下を参照）。

テキストレイヤーには、次の変形が適用されます。

1. テキストボックスのサイズは、`size=`が部分的に指定されたか、まったく指定されていない場合は、`size=`、またはテキストの幅と高さによって決まります。 テキストは、rtf テキスト整列属性を使用してテキストボックス内で整列されます。 テキストボックスによってテキストが切り抜かれる場合があります。
1. `textAttr=`で指定された解像度に基づいてテキストコンテンツを拡大・縮小します。
1. 指定した場合は、`rotate=`を適用します。
1. 指定した場合は、`extend=`を適用します。
1. `origin=`と`pos=`に基づいてカンバス内のレイヤーを配置します（以下を参照）。

画像レイヤーとテキストレイヤーの両方で、レイヤー0がカンバスを効果的に構成するため、キャンバス内のレイヤーの最後のステップ位置はレイヤー0には適用されません。
