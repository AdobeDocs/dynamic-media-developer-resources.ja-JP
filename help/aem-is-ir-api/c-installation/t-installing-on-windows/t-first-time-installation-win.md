---
title: 初めてのインストール
description: Windowsで初めてImage Servingをインストールするには、次の手順を実行します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
TQID: 'https://experienceleague.adobe.com/bL2S5Uv6RkMg5CbPb6mXZvDPf30sHkuXPKc6m7TNXqc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 0%

---

# 初めてのインストール{#installing-for-the-first-time}

Windowsで初めてImage Servingをインストールするには、次の手順を実行します。

1. 管理者権限でサーバーホストにログインします。
1. ライセンスを既に受け取っている場合は、そのライセンスをサーバーにコピーし、ファイルをダブルクリックしてライセンスのインストールを実行します。

   まだライセンスをお持ちでない場合は、インストールを続行し、後でライセンスをインストールできます。

1. 画像サービング配布zip ファイルの内容を抽出します。
1. [!DNL setup]/[!DNL setup.exe]を実行して、インストールウィザードを起動します。
1. 「**[!UICONTROL 次へ]**」を選択して、エンドユーザー使用許諾契約（EULA）に進み、使用許諾契約を読み、「**[!UICONTROL はい]**」を選択します。

   次に[!DNL Authentication] ダイアログボックスが表示されます。
1. ライセンスが既にインストールされていて、[!DNL Authentication] ダイアログボックスにライセンス情報が表示されている場合は、**[!UICONTROL 次へ]**&#x200B;を選択して続行します。

   ライセンスをお持ちでない場合は、「**[!UICONTROL ライセンスを申請]**」を選択してください。 次のダイアログボックスには、マシンのネットワークインターフェイスカード MAC アドレスの1つが表示されます。 このMAC アドレス、会社名、およびインストールする製品をプロンプトに従って電子メールで送信します。

   **重要：** ライセンスは、このホストにインストールされているネットワークインターフェイスカードの1つのMAC アドレスに基づいています。 このカードを無効、削除、または交換すると、ライセンスは有効として認識されなくなります。 画像サービングに使用するハードウェア設定のライセンスを必ず取得してください。

   有効なライセンスなしでISを引き続きインストールし、後でライセンスをインストールできます。 続行するには、**[!UICONTROL 戻る]**&#x200B;を選択して[!DNL Authentication] ダイアログボックスに戻り、**[!UICONTROL 次へ]**&#x200B;を選択します。
1. 「[!DNL Platform Server]管理者設定」ページに進みます。 必要に応じて新しい値を入力するか、デフォルト値をそのまま使用します。

   次の項目を設定できます。

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP接続ポート </p> </td>
      <td> <p>画像サービングおよび画像レンダリング用のメイン HTTP リスニングポート </p> </td>
   </tr> 
   <tr> 
      <td> <p> 管理者リスニングポート </p> </td>
      <td> <p>管理者リスニングポート </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] キャッシュ サイズ （MB） </p> </td>
      <td> <p>メイン応答キャッシュの初期サイズ </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] キャッシュの場所 </p> </td>
      <td> <p>PS キャッシュフォルダー </p> </td>
   </tr>
   </tbody>
   </table>

   指定されたポート番号は一意で、他のアプリケーションやサービスで使用されていない必要があります。

   次の画面では、選択した設定を確認できます。

1. **[!UICONTROL 戻る]**&#x200B;を選択して変更するか、**[!UICONTROL 次へ]**&#x200B;を選択してインストールを開始します。

1. 「**[!UICONTROL 完了]**」を選択して、インストールウィザードを終了します。
