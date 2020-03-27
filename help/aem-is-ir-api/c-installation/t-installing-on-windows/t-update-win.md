---
description: Scene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-description: Scene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-title: IS 4.7.4以降からの更新
solution: Experience Manager
title: IS 4.7.4以降からの更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Scene7画像サービングをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、正しいプロセスについてサポートにお問い合わせください。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>アップグレ [!DNL webapps] ード時にフォルダを削除できます。 アップグレードする前に、フォ [!DNL webapps] ルダーをバックアップします。

1. 管理者権限でサーバーホストにログインします。
1. 画像サービング配布zipファイルの内容を抽出します。
1. setup/setup.exeを実行して、インストールウィザードを起動します。
1. 「次へ **[!UICONTROL 」をクリックして、使用許諾契約書(EULA)に進み、使用許諾契約を読み、「はい」をクリック]** します ****。

   次のページには、以前の設定が表示されます。
1. 「次へ **** 」をクリックして、更新のインストールを開始します。

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >インストーラーは、古いサーバー設定ファイルをフォルダーにバックアップ [!DNL BACKUP/] します。

1. インストールが完了したら、[完了]をクリックしてインストールウィザードを終了します。

   場合によっては、インストールウィザードでシステムの再起動を求められることがあります。
>更新中に、ファイルは [!DNL ImageServing/conf/server.xml] 最新の設定に更新されます。 値を変更または追加した場合は、既存の値を保存し、アップグレード [!DNL server.xml] 後に変更を再実装する必要があります。
>
>アップデートのインストール後、サーバーを稼働させる前に、HTTP応答キャッシュのウォームアップを検討します。 詳細は、ユーティリティの説明 `playlog` を参照してください。

