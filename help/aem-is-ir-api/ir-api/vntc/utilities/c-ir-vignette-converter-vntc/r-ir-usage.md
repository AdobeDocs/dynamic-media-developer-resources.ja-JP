---
title: 使用方法
description: このトピックでは、vntcの使用法の構文について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 1%

---

# 使用方法{#usage}

このトピックでは、vntcの使用法の構文について説明します。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]*&#x200B;は、処理するファイルのパスと名前です。 現在の作業ディレクトリに対する相対パスまたは絶対パスを指定できます。 有効なビネット、キャビネットスタイル、またはウィンドウのカバーするスタイルファイルで、次のいずれかの接尾辞が付いている必要があります。

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

必須。

*[!DNL destFile]*&#x200B;は、出力ビネットファイルのパスと名前です。 指定しない場合、出力ファイルは`-destpath`で指定されたフォルダーに配置されます。 このシナリオでは、ファイル名は、入力ファイル名とサイズのサフィックスから自動的に生成され、`-separator`で指定された文字列で区切られます。 周辺光量補正の場合、サイズの接尾辞は、単一解像度の出力ビネットのピクセル幅、多解像度の出力ビネットの最初のビューの幅、またはピラミッドビネットがある場合は「0」になります。 キャビネットスタイルファイルの場合、出力解像度はファイルのサフィックスとして使用されます。 `-info`が指定されている場合、*[!DNL destFile]*&#x200B;は無視されます。
