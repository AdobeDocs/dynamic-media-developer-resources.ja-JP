---
title: IS 4.7.4以降からの更新
description: Linux®でDynamic Media Image Servingをアップグレードする場合は、次の手順を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
TQID: 'https://experienceleague.adobe.com/RGRlIuemg6bPstlymZg7Ajr9i2ANq-HNjoIULaJydfs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 0%

---

# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Linux®でDynamic Media Image Servingをアップグレードする場合は、次の手順を使用します。

古いバージョンの画像サービングからアップグレードする場合は、正しいプロセスについてサポートにお問い合わせください。

アップグレード時に[!DNL webapps] フォルダーを削除できます。 アップグレードする前に、[!DNL webapps] フォルダーをバックアップしてください。

1. root権限でサーバーホストにログインします。
1. 画像サービング配布tar ファイルを解凍して展開します。
1. [!DNL setup] フォルダーで、[!DNL `./install-is`]を実行してインストールウィザードを起動します。

   更新インストーラーは、インストールされたパッケージの整合性とバージョンを確認します。 成功した場合は、エンドユーザー使用許諾契約（「EULA」）が表示されます。
1. ライセンス契約を読み、**[!UICONTROL y]**&#x200B;と入力してインストールを続行します。

   インストーラーは、古いサーバー設定ファイルを[!DNL BACKUP/] フォルダーにバックアップします。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`

更新中に、[!DNL ImageServing/conf/server.xml] ファイルが最新の設定に更新されます。 値を変更または追加した場合は、既存の[!DNL server.xml]を保存し、アップグレード後に変更を再実装してください。

アップデートのインストール後、サーバーを公開する前に、HTTP応答キャッシュのウォーミングアップを検討してください。 詳しくは、[!DNL playlog] ユーティリティの説明を参照してください。

