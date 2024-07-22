---
title: を 4.7.4 以降から更新する
description: Dynamic Media画像サービングをアップグレードする際は、次の手順を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# を 4.7.4 以降から更新する{#updating-from-is-or-later}

Dynamic Media画像サービングをアップグレードする際は、次の手順を使用します。

古いバージョンの画像サービングからアップグレードする場合は、サポートに連絡して正しいプロセスを確認してください。

>[!NOTE]
>
>アップグレード時に [!DNL webapps] フォルダーが削除される場合があります。 アップグレードの前に、[!DNL webapps] フォルダーをバックアップします。

1. 管理者権限でサーバーホストにログインします。
1. 画像サービング配布 zip ファイルの内容を解凍します。
1. `setup/setup.exe` を実行して、インストールウィザードを起動します。
1. **[!UICONTROL 次へ]** を選択して使用許諾契約書（EULA）に進み、使用許諾契約書を読み、**[!UICONTROL はい]** を選択します。

   次のページには、以前の設定が表示されます。
1. **[!UICONTROL 次へ]** をクリックして、更新プログラムのインストールを開始します。

   >[!NOTE]
   >
   >インストーラーは、古いサーバー設定ファイルを [!DNL BACKUP/] フォルダーにバックアップします。

1. インストールが完了したら、「**[!UICONTROL 完了]**」を選択してインストールウィザードを終了します。

   インストールウィザードから、システムの再起動を求められる場合があります。

更新中、[!DNL ImageServing/conf/server.xml] ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の [!DNL server.xml] を保存し、アップグレード後に変更を再実装する必要があります。

更新のインストール後、サーバーを稼働させる前に、HTTP 応答キャッシュをウォームアップすることを検討してください。 詳細については、`playlog` ユーティリティの説明を参照してください。
