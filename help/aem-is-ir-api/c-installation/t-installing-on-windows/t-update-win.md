---
title: IS 4.7.4 以降からの更新
description: Dynamic Media Image Serving をアップグレードする場合は、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# IS 4.7.4 以降からの更新{#updating-from-is-or-later}

Dynamic Media Image Serving をアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、サポートに問い合わせて、正しい処理をおこなってください。

>[!NOTE]
>
>この [!DNL webapps] アップグレード時にフォルダを削除できます。 バックアップ [!DNL webapps] フォルダをアップグレードする前に

1. 管理者権限でサーバーホストにログインします。
1. 画像サービング配布 zip ファイルの内容を抽出します。
1. を実行して、インストールウィザードを起動します。 `setup/setup.exe`.
1. 選択 **[!UICONTROL 次へ]** エンドユーザー使用許諾契約 (EULA) に進むには、使用許諾契約を読み、 **[!UICONTROL はい]**.

   次のページには、以前の設定が表示されます。
1. クリック **[!UICONTROL 次へ]** をクリックして、更新プログラムのインストールを開始します。

   >[!NOTE]
   >
   >古いサーバ構成ファイルを [!DNL BACKUP/] フォルダー。

1. インストールが完了したら、 **[!UICONTROL 完了]** をクリックして、インストールウィザードを終了します。

   インストールウィザードで、システムを再起動するように求められる場合があります。

更新時に、 [!DNL ImageServing/conf/server.xml] ファイルが最新の設定に更新されました。 値を変更または追加した場合は、既存の [!DNL server.xml] アップグレード後に変更を再実装します。

アップデートのインストール後に、サーバーをライブにする前に HTTP 応答キャッシュをウォームアップすることを検討してください。 詳しくは、 `playlog` ユーティリティを参照してください。
