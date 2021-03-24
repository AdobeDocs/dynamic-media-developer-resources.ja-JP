---
description: デバッグ要求。 このdebugコマンドは、req=imgのように、リクエストの解析と前処理、画像カタログ参照の実行、カタログ修飾子の選択、マクロや変数の置換などを行います。
solution: Experience Manager
title: 解決
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 2%

---


# 解決{#resolve}

デバッグ要求。 このdebugコマンドは、req=imgと同様に、リクエストの解析や前処理、画像カタログ参照の実行、catalog::Modifier選択、マクロや変数の置換などを行います。

`req=resolve`

結果の画像の代わりに、MIMEタイプ`text/plain`の最終要求文字列が返されます。

HTTP応答はキャッシュできません。
