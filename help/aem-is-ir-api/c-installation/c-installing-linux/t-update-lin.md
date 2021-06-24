---
description: LinuxでDynamic Media Image Servingをアップグレードする場合は、次の手順を実行します。
solution: Experience Manager
title: IS 4.7.4以降からの更新
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# IS 4.7.4以降からの更新{#updating-from-is-or-later}

LinuxでDynamic Media Image Servingをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、正しいプロセスについてサポートにお問い合わせください。

[!DNL webapps]フォルダーはアップグレード時に削除される場合があります。 アップグレードする前に[!DNL webapps]フォルダーをバックアップしてください。

1. root権限でサーバーホストにログインします。
1. 画像サービング配布tarファイルを解凍し、解凍します。
1. [!DNL ./install-is]を実行して、[!DNL setup]フォルダーにあるインストールウィザードを起動します。

   アップデートインストーラーは、インストールされたパッケージの整合性とバージョンを確認します。 成功した場合は、エンドユーザー使用許諾契約(「EULA」)が表示されます。
1. 使用許諾契約書を読み、「**[!UICONTROL y]**」と入力してインストールを続行します。

   インストーラーは、古いサーバー設定ファイルを[!DNL BACKUP/]フォルダーにバックアップします。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`

更新中、[!DNL ImageServing/conf/server.xml]ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の[!DNL server.xml]を保存し、アップグレード後に変更を再実装する必要があります。

アップデートのインストール後は、サーバーをライブにする前にHTTP応答キャッシュをウォームアップすることを検討してください。 詳しくは、 [!DNL playlog]ユーティリティの説明を参照してください。
