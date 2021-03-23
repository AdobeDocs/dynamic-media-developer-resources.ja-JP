---
description: server.xmlのConnectorタグでは、SSL接続用に選択できる暗号を制限するciphers属性をサポートしています。
seo-description: server.xmlのConnectorタグでは、SSL接続用に選択できる暗号を制限するciphers属性をサポートしています。
seo-title: SSL暗号の定義
solution: Experience Manager
title: SSL暗号の定義
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# SSL暗号の定義{#defining-ssl-ciphers}

server.xmlのConnectorタグでは、SSL接続用に選択できる暗号を制限するciphers属性をサポートしています。

デフォルトでは、すべての暗号が使用可能です。 リストはカンマで区切られ、次の値のいずれかを含めることができます。

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

いずれかの値が間違っている場合、Tomcatはすべての暗号を有効にします。 だから、設定後に外部ツールを使って、どの暗号が実際に有効になっているかを調べるのが不可欠だ。

例えば、次の設定では「128ビット」以降の暗号スイートのみが有効になります。

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
