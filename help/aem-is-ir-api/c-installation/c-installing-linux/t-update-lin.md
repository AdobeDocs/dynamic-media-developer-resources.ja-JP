---
title: IS 4.7.4 以降からの更新
description: Linux®でDynamic Media Image Serving をアップグレードする場合は、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# IS 4.7.4 以降からの更新{#updating-from-is-or-later}

Linux®でDynamic Media Image Serving をアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、サポートに問い合わせて、正しい処理をおこなってください。

この [!DNL webapps] アップグレード時にフォルダーを削除できます。 をバックアップしてください [!DNL webapps] フォルダをアップグレードする前に

1. root 権限でサーバーホストにログインします。
1. 画像サービング配布 tar ファイルを解凍し、解凍します。
1. 内 [!DNL setup] フォルダー、実行 [!DNL `./install-is`] をクリックして、インストールウィザードを起動します。

   更新インストーラーは、インストールされたパッケージの整合性とバージョンを確認します。 成功した場合は、エンドユーザー使用許諾契約 (「EULA」) が表示されます。
1. 使用許諾契約を読んで、と入力します。 **[!UICONTROL y]** をクリックして、インストールを続行します。

   古いサーバ構成ファイルを [!DNL BACKUP/] フォルダー。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`

更新時に、 [!DNL ImageServing/conf/server.xml] ファイルが最新の設定に更新されました。 値を変更または追加した場合は、既存の [!DNL server.xml] アップグレード後に変更を再実装します。

アップデートのインストール後に、サーバーをライブにする前に HTTP 応答キャッシュをウォームアップすることを検討してください。 詳しくは、 [!DNL playlog] ユーティリティを参照してください。
