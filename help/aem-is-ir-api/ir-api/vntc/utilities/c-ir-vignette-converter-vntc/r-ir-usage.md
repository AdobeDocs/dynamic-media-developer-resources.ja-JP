---
title: 使用方法
description: ここでは、vntc の使用構文について説明します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# 使用方法{#usage}

ここでは、vntc の使用構文について説明します。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* は、処理するファイルのパスと名前です。 現在の作業ディレクトリからの相対パスまたは絶対パスを指定できます。 有効なビネット、キャビネットスタイル、または窓カバリングスタイルファイルで、次のサフィックスのいずれかを付ける必要があります。

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

必須。

*[!DNL destFile]* は、出力ビネットファイルのパスと名前です。 指定しなかった場合、出力ファイルは `-destpath`. このシナリオでは、入力ファイル名とサイズサフィックスから、で指定された文字列で区切られたファイル名が自動的に生成されます。 `-separator`. ビネットの場合、サイズサフィックスは、単一解像度の出力ビネットのピクセル幅、複数解像度の出力ビネットの最初の表示の幅、またはピラミッドビネットがある場合は「0」です。 キャビネットスタイルファイルの場合、出力解像度がファイルサフィックスとして使用されます。 *[!DNL destFile]* 次の場合は無視されます： `-info` が指定されている。
