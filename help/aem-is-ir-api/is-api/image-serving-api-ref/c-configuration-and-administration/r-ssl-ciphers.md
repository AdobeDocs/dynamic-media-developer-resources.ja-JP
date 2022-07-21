---
description: server.xml の Connector タグは、SSL 接続用に選択できる暗号を制限する ciphers 属性をサポートしています。
solution: Experience Manager
title: SSL 暗号の定義
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 370444b85cb2636d109df4e2681e3e078d6f1e1a
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# SSL 暗号の定義{#defining-ssl-ciphers}

server.xml の Connector タグは、SSL 接続用に選択できる暗号を制限する ciphers 属性をサポートしています。

デフォルトでは、すべての暗号が利用可能です。 リストはコンマで区切られ、次の値のいずれかを含めることができます。

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

いずれかの値が正しくない場合、Tomcat は 1 つの暗号をすべて有効にします。 だから、設定後に外部ツールでチェックして、どの暗号が実際に有効になっているかを調べる必要がある。

例えば、次の設定では、「128 ビット」暗号スイート以降のみを有効にします。

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`
