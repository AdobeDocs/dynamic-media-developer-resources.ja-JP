---
title: 初めてのインストール
description: この手順では、Linux® で初めて画像サービングをインストールする方法を示します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 初めてのインストール{#installing-for-the-first-time}

この手順では、Linux® で初めて画像サービングをインストールする方法を示します。

1. ルート権限でサーバーホストにログインします。
1. フォルダー [!DNL /usr/local/scene7/licenses] を作成します。

   画像サービングまたは画像レンダリングのライセンスキー [!DNL .sc8] ァイル（ファイルのサフィックス付き）が使用可能な場合は、このフォルダーにコピーします。 それ以外の場合は、インストールを続行し、後でライセンスキーをインストールします。
1. 画像サービング配布 tar ファイルを解凍します。
1. [!DNL Setup] フォルダーで、[!DNL ./install-is] を実行してインストールウィザードを起動します。

   ライセンス キーが見つからない場合は、ライセンス ファイルの取得方法を説明する指示が表示されます。 この時点でインストールを行うか、イメージサービングのインストールに進み、後でライセンスキーをインストールします。
1. 使用許諾契約書（EULA）が表示されたら、使用許諾契約書を読み、`y` と入力して続行します。

   次の表に示すプロンプトがインストーラに表示されます。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> メイン リスニング ポート [8080]:</span> </p> </td>
   <td colname="col2"> <p>画像サービングおよび画像レンダリング用のメイン HTTP リスニングポート。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理リスニング ポート [8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理リスニングポート。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大 HTTP キャッシュ サイズ （MB） [2000]:</span> </p> </td> 
   <td colname="col2"> <p>メイン応答キャッシュの初期サイズ。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> キャッシュルートフォルダー [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS キャッシュ フォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server 所有者 ID [ ルート ]:</span> </p> </td>
   <td colname="col2"> <p>画像サービングサーバーをインストールするユーザーアカウント。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server グループ ID [ ルート ]:</span> </p> </td>
   <td colname="col2"> <p>画像サービングサーバーをインストールするグループアカウント。 </p> </td>
  </tr>
 </tbody>
</table>

1. **[!UICONTROL Enter]** キーを押して、デフォルト値をそのまま使用するか、別の値を指定します。

   指定したすべてのポート番号が一意であり、このホストで使用されていないことを確認してください。

   >[!IMPORTANT]
   >
   >ルート以外のアカウントを指定した場合は、設定ファイルでこれらのフォルダーを再設定する際に、Image Server が読み取りおよび書き込みを必要とするすべてのファイルとフォルダーのアクセス権が正しく設定されていることを確認する必要があります。
   >
   >これで、画像サービングが [!DNL /usr/local/Scene7/ImageServing] にインストールされました。 特定の画像レンダリングコンテンツが [!DNL /usr/local/Scene7/ImageRendering] にインストールされます。
   >
   >インストールの最後に、インストールウィザードは Image Server の起動を試みます。 有効なライセンスキーが見つからない場合、Image Server を起動できません。 有効なライセンスがあり、Image Server がまだ起動しない場合は、ログファイルを参照してください。

>[!NOTE]
>
>画像サービングのインストール後にライセンスをインストールした場合は、使用前に Image Server を手動で起動する必要があります。
