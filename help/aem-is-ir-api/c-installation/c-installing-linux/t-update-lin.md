---
title: を 4.7.4 以降から更新する
description: Linux® で提供されているDynamic Media イメージをアップグレードする場合は、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# を 4.7.4 以降から更新する{#updating-from-is-or-later}

Linux® で提供されているDynamic Media イメージをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、サポートに連絡して正しいプロセスを確認してください。

[!DNL webapps] フォルダーは、アップグレード時に削除できます。 アップグレードの前に [!DNL webapps] フォルダーをバックアップしてください。

1. root 権限でサーバ・ホストにログインします。
1. 画像サービング配布 tar ファイルを解凍します。
1. [!DNL setup] フォルダーで [!DNL `./install-is`] を実行して、インストールウィザードを起動します。

   アップデートインストーラーは、インストールされたパッケージの整合性とバージョンをチェックします。 成功すると、使用許諾契約書（「EULA」）が表示されます。
1. 使用許諾契約書を読み、「**[!UICONTROL y]**」と入力してインストールを続行します。

   インストーラーは、古いサーバー設定ファイルを [!DNL BACKUP/] フォルダーにバックアップします。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`

更新中、[!DNL ImageServing/conf/server.xml] ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の [!DNL server.xml] を保存し、アップグレード後に変更を再実装します。

更新のインストール後、サーバーを稼働させる前に、HTTP 応答キャッシュをウォームアップすることを検討してください。 詳細については、[!DNL playlog] ユーティリティの説明を参照してください。
