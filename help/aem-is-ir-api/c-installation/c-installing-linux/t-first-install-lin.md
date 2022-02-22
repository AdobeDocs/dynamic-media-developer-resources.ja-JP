---
title: 初めてのインストール
description: この手順では、Linux®に初めて画像サービングをインストールする方法を示します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 初めてのインストール{#installing-for-the-first-time}

この手順では、Linux®に初めて画像サービングをインストールする方法を示します。

1. root 権限でサーバーホストにログインします。
1. フォルダーの作成 [!DNL /usr/local/scene7/licenses].

   画像サービングまたは画像レンダリングのライセンスキーファイル ( [!DNL .sc8] ファイルサフィックス ) が使用可能な場合は、このフォルダにコピーします。 それ以外の場合は、インストールに進み、後でライセンスキーをインストールします。
1. 画像サービング配布 tar ファイルを解凍し、解凍します。
1. 内 [!DNL Setup] フォルダーを開くには、次のコマンドを実行してインストールウィザードを起動します。 [!DNL ./install-is].

   ライセンスキーが見つからない場合は、ライセンスファイルの取得方法を説明する手順が表示されます。 この時点でインストールするか、画像サービングのインストールに進み、後でライセンスキーをインストールします。
1. エンドユーザー使用許諾契約 (EULA) が表示されたら、使用許諾契約を読んで、 `y` をクリックして続行します。

   次の表に示すプロンプトが表示されます。

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> メインリスニングポート [8080]:</span> </p> </td>
   <td colname="col2"> <p>画像サービングおよび画像レンダリング用のメイン HTTP リスニングポート。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 管理リスニングポート [8083]:</span> </p> </td> 
   <td colname="col2"> <p>管理者のリスニングポート。 </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 最大 HTTP キャッシュサイズ (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>メイン応答キャッシュの初期サイズ。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> キャッシュのルートフォルダ [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>PS キャッシュフォルダー。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server 所有者 ID [root] :</span> </p> </td>
   <td colname="col2"> <p>画像サービングサーバーをインストールするユーザーアカウント。 </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Image Server グループ ID [root]:</span> </p> </td>
   <td colname="col2"> <p>画像サービングサーバーをインストールするグループアカウント。 </p> </td>
  </tr>
 </tbody>
</table>

1. 押す **[!UICONTROL 入力]** をクリックしてデフォルト値を受け入れるか、別の値を指定します。

   指定したポート番号がすべて一意であることを確認し、このホストでは別途使用されないようにします。

   >[!IMPORTANT]
   >
   >root 以外のアカウントを指定する場合は、Image Server が読み取りおよび書き込みが必要なすべてのファイルおよびフォルダに対するアクセス権限が、設定ファイルで再設定されたときに正しく設定されていることを確認する必要があります。
   >
   >画像サービングが [!DNL /usr/local/Scene7/ImageServing]. 特定の画像レンダリングコンテンツが [!DNL /usr/local/Scene7/ImageRendering].
   >
   >インストールが終了すると、インストールウィザードは Image Server の起動を試みます。 有効なライセンスキーが見つからない場合、Image Server は起動できません。 有効なライセンスがあり、Image Server が起動しない場合は、ログファイルを参照してください。

>[!NOTE]
>
>画像サービングをインストールした後にライセンスがインストールされている場合は、使用前に Image Server を手動で起動する必要があります。
