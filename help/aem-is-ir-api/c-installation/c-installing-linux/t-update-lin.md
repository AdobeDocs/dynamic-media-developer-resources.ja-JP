---
description: Linux上のScene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-description: Linux上のScene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-title: IS 4.7.4以降からの更新
solution: Experience Manager
title: IS 4.7.4以降からの更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 038f0f8f2c4f815e47749e0bab153c63e5396c91
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Linux上のScene7画像サービングをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、適切なプロセスについてサポートにお問い合わせください。

アップグレード時に [!DNL webapps] フォルダを削除できます。 アップグレードする前に、 [!DNL webapps] フォルダをバックアップしてください。

1. root権限でサーバーホストにログインします。
1. 画像サービングの配布tarファイルを解凍し、解凍します。
1. を実行 [!DNL ./install-is] して、フォル [!DNL setup] ダー内のインストールウィザードを起動します。

   アップデートインストーラーは、インストール済みパッケージの整合性とバージョンを確認します。 成功した場合は、エンドユーザ使用許諾契約(「EULA」)が表示されます。
1. 使用許諾契約書を読み、「 **[!UICONTROL y]**」と入力してインストールを続行します。

   インストーラーは、古いサーバー設定ファイルを [!DNL BACKUP/] フォルダーにバックアップします。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`

更新中に、 [!DNL ImageServing/conf/server.xml] ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の値を保存し、アップグレード後に変更を再実装する必要があ [!DNL server.xml] ります。

アップデートのインストール後は、サーバーをライブにする前にHTTP応答キャッシュのウォームアップを検討してください。 詳細は、ユー [!DNL playlog] ティリティの説明を参照してください。
