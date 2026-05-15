---
title: IS 4.7.4以降からの更新
description: Dynamic Media画像サービングをアップグレードする場合は、次の手順を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
TQID: 'https://experienceleague.adobe.com/ibeLWHpA-Lk2wiXkSgGL02uMEYH4t8l0xjjXuN9ooiE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 0%

---

# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Dynamic Media画像サービングをアップグレードする場合は、次の手順を使用します。

古いバージョンの画像サービングからアップグレードする場合は、正しいプロセスについてサポートにお問い合わせください。

>[!NOTE]
>
>アップグレード時に[!DNL webapps] フォルダーが削除される可能性があります。 アップグレードする前に[!DNL webapps] フォルダーをバックアップします。

1. 管理者権限でサーバーホストにログインします。
1. 画像サービング配布zip ファイルの内容を抽出します。
1. `setup/setup.exe`を実行して、インストールウィザードを起動します。
1. 「**[!UICONTROL 次へ]**」を選択して、エンドユーザー使用許諾契約（EULA）に進み、使用許諾契約を読み、「**[!UICONTROL はい]**」を選択します。

   次のページには、以前の設定設定が表示されます。
1. 「**[!UICONTROL 次へ]**」をクリックして、更新プログラムのインストールを開始します。

   >[!NOTE]
   >
   >インストーラーは、古いサーバー設定ファイルを[!DNL BACKUP/] フォルダーにバックアップします。

1. インストールが完了したら、**[!UICONTROL 終了]**&#x200B;を選択してインストールウィザードを終了します。

   インストールウィザードで、システムの再起動を求められる場合があります。

更新中に、[!DNL ImageServing/conf/server.xml] ファイルが最新の設定に更新されます。 値を変更または追加した場合は、既存の[!DNL server.xml]を保存し、アップグレード後に変更を再実装する必要があります。

アップデートのインストール後、サーバーを公開する前に、HTTP応答キャッシュのウォーミングアップを検討してください。 詳しくは、`playlog` ユーティリティの説明を参照してください。
