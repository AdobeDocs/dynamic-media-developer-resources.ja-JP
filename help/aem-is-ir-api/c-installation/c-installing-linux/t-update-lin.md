---
description: Linux上のDynamic Media画像サービングをアップグレードする場合は、次の手順を実行します。
solution: Experience Manager
title: IS 4.7.4以降からの更新
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# IS 4.7.4以降からの更新{#updating-from-is-or-later}

Linux上のDynamic Media画像サービングをアップグレードする場合は、次の手順を実行します。

古いバージョンの画像サービングからアップグレードする場合は、適切なプロセスについてサポートにお問い合わせください。

[!DNL webapps]フォルダーはアップグレード時に削除できます。 アップグレードする前に[!DNL webapps]フォルダーをバックアップしてください。

1. root権限でサーバーホストにログインします。
1. 画像サービングの配布tarファイルを解凍し、解凍します。
1. [!DNL ./install-is]を実行して[!DNL setup]フォルダーにあるインストールウィザードを起動します。

   アップデートインストーラーは、インストール済みパッケージの整合性とバージョンを確認します。 成功した場合は、エンドユーザ使用許諾契約(「EULA」)が表示されます。
1. 使用許諾契約書を読み、&quot;**[!UICONTROL y]**&quot;と入力してインストールを続行します。

   インストーラーは、古いサーバー設定ファイルを[!DNL BACKUP/]フォルダーにバックアップします。

   インストールが完了すると、次のメッセージが表示されます。

   `Image Server was started successfully`

更新中に、[!DNL ImageServing/conf/server.xml]ファイルは最新の設定に更新されます。 値を変更または追加した場合は、既存の[!DNL server.xml]を保存し、アップグレード後に変更を再実装する必要があります。

アップデートのインストール後は、サーバーをライブにする前にHTTP応答キャッシュのウォームアップを検討してください。 詳細は、[!DNL playlog]ユーティリティの説明を参照してください。
