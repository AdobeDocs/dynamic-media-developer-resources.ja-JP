---
description: Linux上のScene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-description: Linux上のScene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-title: IS 4.7.4以降からの更新
solution: Experience Manager
title: IS 4.7.4以降からの更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Linux上のScene7画像サービングをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、正しいプロセスについてサポートにお問い合わせください。

アップグレ [!DNL webapps] ード時にフォルダを削除できます。 アップグレードする前に、フォル [!DNL webapps] ダをバックアップしてください。

1. root権限でサーバーホストにログインします。
1. 画像サービング配布用tarファイルを解凍し、解凍します。
1. を実行 [!DNL ./install-is] して、フォルダー内のインストールウィザードを起動 [!DNL setup] します。

   アップデートインストーラーは、インストールされたパッケージの整合性とバージョンを確認します。 成功した場合は、エンドユーザ使用許諾契約(「EULA」)が表示されます。
1. 使用許諾契約を読み、「 **[!UICONTROL y]**」と入力してインストールを続行します。

   インストーラーは、古いサーバー設定ファイルをフォルダーにバックアップ [!DNL BACKUP/] します。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`
>更新中に、ファイルは [!DNL ImageServing/conf/server.xml] 最新の設定に更新されます。 値を変更または追加した場合は、既存の値を保存し、アップグレード [!DNL server.xml] 後に変更を再実装する必要があります。
>
>アップデートのインストール後、サーバーを稼働させる前に、HTTP応答キャッシュのウォームアップを検討します。 詳細は、ユーティリティの説明 [!DNL playlog] を参照してください。

