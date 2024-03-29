---
title: 初めてのインストール
description: 画像サービングを Windows に初めてインストールするには、次の手順を使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# 初めてのインストール{#installing-for-the-first-time}

画像サービングを Windows に初めてインストールするには、次の手順を使用します。

1. 管理者権限でサーバーホストにログインします。
1. 既にライセンスを受け取っている場合は、サーバにコピーし、ファイルをダブルクリックしてライセンスのインストールを実行します。

   ライセンスをお持ちでない場合は、インストールを続行し、後でライセンスをインストールすることができます。

1. 画像サービング配布 zip ファイルの内容を抽出します。
1. を実行して、インストールウィザードを起動します。 [!DNL setup]/ [!DNL setup.exe].
1. 選択 **[!UICONTROL 次へ]** エンドユーザー使用許諾契約 (EULA) に進むには、使用許諾契約を読み、 **[!UICONTROL はい]**.

   この [!DNL Authentication] ダイアログボックスが次に表示されます。
1. ライセンスが既にインストールされていて、ライセンス情報が [!DNL Authentication] ダイアログボックスで、次を選択します。 **[!UICONTROL 次へ]** をクリックして続行します。

   ライセンスをお持ちでない場合は、 **[!UICONTROL ライセンスをリクエスト]**. 次のダイアログボックスには、お使いのコンピューターの Network Interface Card MACアドレスの 1 つが表示されます。 このMACのアドレス、会社名、およびインストールする製品を、プロンプトの指示に従って電子メールで送信してください。

   **重要：** このライセンスは、このホストにインストールされているネットワークインターフェイスカードの 1 つのMACアドレスに基づいています。 このカードを無効にしたり、削除したり、交換したりした場合、ライセンスは有効と認識されなくなります。 画像サービングに使用するハードウェア設定のライセンスを必ず取得してください。

   有効なライセンスがない状態で IS を引き続きインストールし、後でライセンスをインストールすることができます。 続行するには、「 」を選択します。 **[!UICONTROL 戻る]** に戻る [!DNL Authentication] ダイアログボックスで、 **[!UICONTROL 次へ]**.
1. 「[!DNL Platform Server] 管理者設定」ページに表示されます。 必要に応じて新しい値を入力するか、デフォルトを受け入れます。

   次の項目を設定できます。

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] HTTP 接続ポート </p> </td>
      <td> <p>画像サービングおよび画像レンダリング用のメイン HTTP リスニングポート </p> </td>
   </tr> 
   <tr> 
      <td> <p> 管理リスニングポート </p> </td>
      <td> <p>管理リスニングポート </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] キャッシュサイズ (MB) </p> </td>
      <td> <p>メイン応答キャッシュの初期サイズ </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] キャッシュの場所 </p> </td>
      <td> <p>PS キャッシュフォルダー </p> </td>
   </tr>
   </tbody>
   </table>

   指定するポート番号は一意である必要があり、他のアプリケーションやサービスでは使用できません。

   次の画面では、選択した設定を確認できます。

1. 選択 **[!UICONTROL 戻る]** 変更を加えるか、選択するには **[!UICONTROL 次へ]** をクリックして、インストールを開始します。

1. 選択 **[!UICONTROL 完了]** をクリックして、インストールウィザードを終了します。
