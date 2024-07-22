---
title: 使用方法
description: このトピックでは、vntc の使用構文について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# 使用方法{#usage}

このトピックでは、vntc の使用構文について説明します。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* は、処理するファイルのパスと名前です。 現在の作業ディレクトリに対する相対パスまたは絶対パスを指定できます。 有効なビネット、キャビネット スタイル、またはウィンドウ カバースタイル ファイルで、次のいずれかのサフィックスが付いている必要があります。

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

必須。

*[!DNL destFile]* は、出力ビネットファイルのパスと名前です。 指定しない場合、出力ファイルは `-destpath` で指定したフォルダーに配置されます。 このシナリオでは、入力ファイル名とサイズサフィックスから、`-separator` で指定した文字列で区切られたファイル名が自動的に生成されます。 ビネットの場合、サイズ サフィックスは、単一解像度の出力ビネットのピクセル幅、複数解像度の出力ビネットの最初のビューの幅、またはピラミッド型のビネットがある場合は「0」になります。 キャビネット形式のファイルの場合、出力解像度がファイルの接尾辞として使用されます。 `-info` が指定されている場合、*[!DNL destFile]* は無視されます。
