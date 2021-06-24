---
description: Dynamic Media Image Servingをアップグレードする場合は、次の手順を実行します。
solution: Experience Manager
title: IS 4.7.4以降からの更新
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Dynamic Media Image Servingをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、正しいプロセスについてサポートにお問い合わせください。

>[!NOTE]
>
>[!DNL webapps]フォルダーはアップグレード時に削除される場合があります。 アップグレードする前に[!DNL webapps]フォルダーをバックアップします。

1. 管理者権限でサーバーホストにログインします。
1. 画像サービング配布zipファイルの内容を抽出します。
1. setup/setup.exeを実行して、インストールウィザードを起動します。
1. 「**[!UICONTROL 次へ]**」をクリックしてエンドユーザー使用許諾契約(EULA)に進み、使用許諾契約書を読んで、「**[!UICONTROL はい]**」をクリックします。

   次のページには、前の設定が表示されます。
1. **[!UICONTROL 「次へ]**」をクリックして、更新のインストールを開始します。

   >[!NOTE]
   >
   >インストーラーは、古いサーバー設定ファイルを[!DNL BACKUP/]フォルダーにバックアップします。

1. インストールが完了したら、「完了」をクリックしてインストールウィザードを終了します。

   場合によっては、インストールウィザードでシステムを再起動するように求められます。

更新中、[!DNL ImageServing/conf/server.xml]ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の[!DNL server.xml]を保存し、アップグレード後に変更を再実装する必要があります。

アップデートのインストール後は、サーバーをライブにする前にHTTP応答キャッシュをウォームアップすることを検討してください。 詳しくは、 `playlog`ユーティリティの説明を参照してください。
