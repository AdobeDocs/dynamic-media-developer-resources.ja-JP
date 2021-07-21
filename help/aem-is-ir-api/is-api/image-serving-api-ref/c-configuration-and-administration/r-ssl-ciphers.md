---
description: server.xmlのConnectorタグは、SSL接続用に選択できる暗号を制限するciphers属性をサポートしています。
solution: Experience Manager
title: SSL暗号の定義
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# SSL暗号の定義{#defining-ssl-ciphers}

server.xmlのConnectorタグは、SSL接続用に選択できる暗号を制限するciphers属性をサポートしています。

デフォルトでは、すべての暗号が使用可能です。 リストはコンマで区切られ、次の値のいずれかを含めることができます。

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

いずれかの値が正しくない場合、Tomcatはすべての暗号を有効にします。 したがって、設定後に外部ツールとチェックして、実際にどの暗号が有効かを確認する必要があります。

例えば、次の設定では、「128ビット」暗号スイート以降のみが有効になります。

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
