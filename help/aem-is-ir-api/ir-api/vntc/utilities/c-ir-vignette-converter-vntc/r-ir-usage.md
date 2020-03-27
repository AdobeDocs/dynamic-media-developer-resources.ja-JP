---
description: ここでは、vntcの使用構文について説明します。
seo-description: ここでは、vntcの使用構文について説明します。
seo-title: 使用方法
solution: Experience Manager
title: 使用方法
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用方法{#usage}

ここでは、vntcの使用構文について説明します。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* は、処理するファイルのパスと名前です。 現在の作業ディレクトリからの相対パスまたは絶対パスを指定できます。 有効なビネット、キャビネットスタイル、または窓カバリングスタイルファイルで、次のサフィックスのいずれかを付ける必要があります。 [!DNL .vnt]、ま [!DNL .vnc]たは [!DNL .vnw]。 必須。

*[!DNL destFile]* は、出力ビネットファイルのパスと名前です。 指定しなかった場合、出力ファイルはで指定したフォルダーに配置されま `-destpath`す。 このシナリオでは、入力ファイル名とサフィックスサフィックスからファイル名が自動的に生成され、に指定した文字列で区切られま `-separator`す。 ビネットの場合、サイズのサフィックスは、単一解像度の出力ビネットのピクセル幅、複数解像度の出力ビネットの最初のビューの幅、ピラミッドの場合は「0」です。 キャビネットスタイルのファイルの場合、出力解像度がファイルのサフィックスとして使用されます。 *[!DNL destFile]* が指定された場合は無 `-info` 視されます。
