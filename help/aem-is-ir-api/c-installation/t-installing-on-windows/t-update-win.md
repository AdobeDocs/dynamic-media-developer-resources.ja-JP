---
description: Scene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-description: Scene7画像サービングをアップグレードする場合は、次の手順を実行します。
seo-title: IS 4.7.4以降からの更新
solution: Experience Manager
title: IS 4.7.4以降からの更新
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Scene7画像サービングをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、適切なプロセスについてサポートにお問い合わせください。

>[!NOTE]
>
>[!DNL webapps]フォルダーはアップグレード時に削除できます。 アップグレードする前に[!DNL webapps]フォルダーをバックアップします。

1. 管理者権限でサーバーホストにログインします。
1. 画像サービング配布zipファイルの内容を抽出します。
1. setup/setup.exeを実行してインストールウィザードを起動します。
1. 「**[!UICONTROL 次へ]**」をクリックして使用許諾契約書(EULA)に進み、使用許諾契約書を読み、「**[!UICONTROL はい]**」をクリックします。

   次のページには、以前の設定が表示されます。
1. **[!UICONTROL 「次へ]**」をクリックして、アップデートのインストールを開始します。

   >[!NOTE]
   >
   >インストーラーは、古いサーバー設定ファイルを[!DNL BACKUP/]フォルダーにバックアップします。

1. インストールが完了したら、[完了]をクリックしてインストールウィザードを終了します。

   場合によっては、インストールウィザードでシステムを再起動するように求められます。

更新中に、[!DNL ImageServing/conf/server.xml]ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の[!DNL server.xml]を保存し、アップグレード後に変更を再実装する必要があります。

アップデートのインストール後は、サーバーをライブにする前にHTTP応答キャッシュのウォームアップを検討してください。 詳細は、`playlog`ユーティリティの説明を参照してください。
