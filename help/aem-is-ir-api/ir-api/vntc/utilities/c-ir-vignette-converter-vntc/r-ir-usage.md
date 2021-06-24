---
description: ここでは、vntcの使用構文について説明します。
solution: Experience Manager
title: 使用方法
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# 使用方法{#usage}

ここでは、vntcの使用構文について説明します。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* は、処理するファイルのパスと名前です。現在の作業ディレクトリに対する相対パスまたは絶対パスを指定できます。 有効なビネット、キャビネットスタイル、または窓カバースタイルファイルで、次のサフィックスのいずれかを付ける必要があります。[!DNL .vnt]、[!DNL .vnc]、または[!DNL .vnw]。 必須。

*[!DNL destFile]* は、出力ビネットファイルのパスと名前です。指定しなかった場合、出力ファイルは`-destpath`で指定されたフォルダーに配置されます。 このシナリオでは、入力ファイル名とサイズサフィックスを`-separator`で指定された文字列で区切って、ファイル名が自動的に生成されます。 ビネットの場合、サイズサフィックスは、単一解像度出力ビネットのピクセル幅、複数解像度出力ビネットの最初のビューの幅、またはピラミッドビネットの場合は「0」です。 キャビネットスタイルファイルの場合、出力解像度がファイルサフィックスとして使用されます。 *[!DNL destFile]* が指定されている場合、は無 `-info` 視されます。
