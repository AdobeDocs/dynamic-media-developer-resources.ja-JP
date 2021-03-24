---
description: ここでは、vntcの使用構文について説明します。
solution: Experience Manager
title: 使用方法
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 使用方法{#usage}

ここでは、vntcの使用構文について説明します。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* は、処理するファイルのパスと名前です。現在の作業ディレクトリからの相対パスまたは絶対パスを指定できます。 有効なビネット、キャビネットスタイル、または窓カバリングスタイルのファイルで、次のいずれかのサフィックスを付ける必要があります。[!DNL .vnt]、[!DNL .vnc]、または[!DNL .vnw]。 必須。

*[!DNL destFile]* は、出力ビネットファイルのパスと名前です。指定しなかった場合、出力ファイルは`-destpath`で指定されたフォルダーに配置されます。 このシナリオでは、入力ファイル名とサイズのサフィックスからファイル名が自動的に生成され、`-separator`で指定された文字列で区切られます。 ビネットの場合、サイズのサフィックスは、単一解像度の出力ビネットのピクセル幅、複数解像度の出力ビネットの最初の表示の幅、またはピラミッドのビネットの場合は「0」です。 キャビネットスタイルファイルの場合、出力解像度はファイルのサフィックスとして使用されます。 *[!DNL destFile]* を指定した場合は無視 `-info` されます。
