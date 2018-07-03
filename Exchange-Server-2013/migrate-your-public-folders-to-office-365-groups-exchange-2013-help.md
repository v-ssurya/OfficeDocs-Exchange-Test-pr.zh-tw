﻿---
title: '將公用資料夾移轉至 Office 365 群組: Exchange Online Help'
TOCTitle: 將公用資料夾移轉至 Office 365 群組
ms:assetid: d89e727b-675a-4623-b572-260f8b44b966
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Mt843872(v=EXCHG.150)
ms:contentKeyID: 74468727
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 將公用資料夾移轉至 Office 365 群組

 

_**適用版本：** Exchange Online, Exchange Server 2010, Exchange Server 2013_

_**上次修改主題的時間：** 2017-09-25_

**摘要：**  您應或不應該將 Exchange 公用資料夾移轉至 Office 365 群組的原因。

本文提供公用資料夾和 Office 365 群組和一或其他可能是最適合貴組織的解決方案的比較。而群組所引進更最近已筆只要 Exchange 公用資料夾。如果您想要將某些或所有的公用資料夾移轉至群組，本文說明程序的運作方式，並提供您逐步執行的程序逐步說明的文章連結。

## 公用資料夾有哪些？

[公用資料夾](public-folders-exchange-2013-help.md)包含不同的資料類型與組織中的階層式結構。

在下列情況中不建議使用的公用資料夾：

  - **封存資料**。使用者信箱限制有時會使用，而不是信箱的公用資料夾可封存資料。此作法是不建議使用，因為它會影響公用資料夾中的儲存空間和思考的目標信箱限制。

  - **文件共用和協同合作**。公用資料夾不提供文件管理功能，例如版本設定、 控制存回及取出功能及自動通知內容變更。

## 什麼是 Office 365 群組？

Office 365 中的群組可讓您選擇一組人員想要與、 共同作業，然後輕鬆地設定這些人員共用資源的集合。您不需要擔心手動將權限指派給這些資源，因為加入了一些給您群組的成員會自動提供成員的使用者需要存取這些工具的權限和您的群組提供的資源。群組也是這些工作的先前已由通訊群組清單處理與共用信箱以及全新改良經驗。

完整的群組本文，請參閱[了解 Office 365 群組](https://go.microsoft.com/fwlink/p/?linkid=858521)。

## 應您將公用資料夾移轉至 Office 365 群組吗？

Office 365 群組是最新的共同作業提供 microsoft，這表示有許多原因為何他們試試解決方案是透過公用資料夾、 太多較舊的技術。在 Outlook 中，例如群組可以取代擁有郵件功能的公用資料夾完全。編譯清單中的每個案例中的 Office 365 群組 works 優於公用資料夾之前，但有個重點：

  - **透過電子郵件的共同作業**。在 Outlook 中的群組具有專用的**交談**空間可讓使用者透過這些共同作業及儲存所有電子郵件。群組可以甚至是要設定接收訊息的人員外群組或從組織外部。如果您目前使用擁有郵件功能的公用資料夾儲存區與專案相關討論，例如或購買檢視小組所需要的訂單，使用群組會是人員的改進。您只想要播放一組使用者的資訊時，也較佳的情況下群組。

  - **透過文件的共同作業**。在 Outlook 中，群組會有專用**的檔案**\] 索引標籤會顯示所有檔案群組的 SharePoint 小組網站，以及從郵件附件。您會收到一個檢視的所有檔案，所以您不必移搜尋其像您設定公用資料夾中。共同撰寫也會成為更容易。如果您正在使用的公用資料夾儲存原本用意多人所耗用的檔案，請考慮移轉至群組。

  - **共用行事曆**。在建立時每個群組會取得共用行事曆。任何群組的成員可以建立該行事曆上的事件。當我的最愛\] 群組中，該群組行事曆可以顯示個人的行事曆旁。您也可以訂閱的群組事件，在其中建立該群組中的案例事件會出現在個人行事曆。如果您使用公用資料夾遷移至主機行事曆的小組，例如排程\] 或 \[時間表群組是體驗。

  - **簡體權限**。當您將使用者指派給群組時，其立即取得權限所需，而您需要手動指派適當的權限與公用資料夾。成員可新增為 「 擁有者 」 或 「 成員 」。擁有者可在群組中，包括能夠執行群組 」 管理工作的完整權限。成員也可以建立的內容及編輯檔案一樣的擁有者，但成員不能刪除他們不所建立的內容。如果公用資料夾的權限模型會為您太多得難以與您想要的某個項目簡單且快速、 Office 365 群組是移的方式。

  - **行動電話和 Web 的目前狀態**。公用資料夾無法透過行動裝置存取和網路上有一組有限的功能。Office 365 群組換句話說，可透過 Outlook 行動應用程式及 Web 上有一組豐富的功能。如果您的小組在移動，且需要行動裝置存取，那麼您應該使用 Office 365 群組。

  - **整體範圍的 Office 365 應用程式的存取**權。當您建立的群組時、 您解除鎖定存取各種應用程式以從 Office 365 套件。您可以取得 SharePoint 小組網站追蹤任務的規劃上儲存的檔案與計劃。Office 365 群組是結合的整個 Office 365 套裝軟體元素的成員資格服務。

雖然 Office 365 群組具有許多優點，您應該要知道您會發現後離開的公用資料夾經驗的一些主要差異。這些是主要是：

  - **資料夾階層**。雖然公用資料夾通常用來組織深入的根階層中的內容、 Office 365 群組具有平面結構。在群組中的所有電子郵件位於交談空間而所有文件移至 \[**檔案**\] 索引標籤。此外，您無法在 Office 365 群組中建立子資料夾。

  - **細微權限的角色**。儘管公用資料夾有各種權限的角色，Office 365 群組只提供兩個： 擁有者和成員。

您將移至群組之前，也是好記下建立和維護群組隨附的各種限制。請參閱*如何管理 「 我的群組？*中[了解 Office 365 群組](https://go.microsoft.com/fwlink/p/?linkid=858521)如需詳細資訊。

## 將公用資料夾遷移至 Office 365 群組

如果您決定切換至 Office 365 群組，您可以使用此程序稱為*批次移轉*將您的電子郵件和行事曆內容從現有的公用資料夾移至群組。執行批次移轉的特定步驟，取決於哪些 Exchange 版本的目前主控公用資料夾階層。本文結尾找到您逐步執行批次移轉程序的指示連結。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.note(EXCHG.150).gif" title="注意事項" alt="注意事項" />注意事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>當您完成將擁有郵件功能的公用資料夾移轉至 Office 365 中的特定群組時預設傳送給公用資料夾的所有電子郵件會在那個時候接收群組。</td>
</tr>
</tbody>
</table>


批次移轉的主要優點如下：

  - **信箱複寫服務 MRS 式移轉**。移轉程序會使用移轉批次指令程式。移轉至多個群組可在單一的遷移批次中一起觸發。也有指令碼可用來協助移轉程序。

  - **支援郵件和行事曆的公用資料夾**。複製的電子郵件與文章會顯示相同為群組交談群組並複製行事曆項目就會出現在群組行事曆。此遷移目前不支援其他公用資料夾類型，例如工作及連絡人。

  - **內部部署公用資料夾可移轉至 Office 365 群組直接**。此遷移不需要您第一次移動至您公用資料夾遷移至 Office 365 並再移至群組。MRS 資料複本指令程式直接從您的內部部署環境讀取公用資料夾資料並再將資料複製到 Office 365 群組。請注意 Exchange 2010 公用資料夾需要 「 Outlook 無所不在 」 端點。Exchange 2013 和 Exchange 2016 公用資料夾會需要 MRS Proxy 為基礎的端點。

  - **不"所有或 nothing"移轉**。您取得選擇特定的公用資料夾移轉至群組及只有那些所選擇的公用資料夾會移轉。

  - **一次升級資料複製**。批次移轉設計成可從來源公用資料夾簡單一次性資料複製到目標群組，而累加同步處理和最終的複雜性。

  - **合併與現有的資料\] 群組中的公用資料夾資料**。如果有任何複製的資料會合併與現有的群組內容的公用資料夾內容。累加資料複製需要時，只是可執行資料複製您需要的次數。這會透過將累加資料複製到群組中。

## 批次移轉的概觀

下列步驟概述移轉至 Office 365 群組的公用資料夾內容以批次遷移的整體程序。下面所列的各篇文章中包含特定的詳細資訊。

1.  **選取 \[來源：**  選擇您要移轉的公用資料夾。您可以選擇任何資料夾包含郵件或行事曆的內容。

2.  **建立目標：**  建立您資料夾相對應群組具有所需的設定，例如成員、 隱私權設定和資料分類。

3.  **複製資料：**  用於移轉批次指令程式將資料從公用資料夾複製至群組。

4.  **鎖定來源：**  一旦確認群組中的資料在鎖定的公用資料夾。

5.  **Cutover：**  複製已建立在步驟 3 和 4 之間的任何新資料。

請注意您的公用資料夾和其對應的群組會保持連線使用者的步驟 1 到 3 上述期間。步驟 3 中之後，您可以評估要繼續執行遷移，根據群組功能其餘和符合您的使用者與您的組織。您可以回復移轉並繼續在那個時候使用公用資料夾。如果您不要繼續移轉步驟 5 完成後，您可以刪除原始的公用資料夾。偶數移轉後可以回復到公用資料夾，提供您已從遷移程序儲存備份檔案，且未刪除原始的公用資料夾。

## 批次移轉必要條件與逐步說明

您可以執行批次移轉前 Exchange 環境中需要下列先決條件。特定先決條件取決於哪些 Exchange 版本的目前執行中。

1.  如果而公用資料夾存在於內部部署，您的伺服器必須執行下列版本之一：
    
      - Exchange 2010 SP3 RU8 或更新版本
    
      - Exchange 2013 CU15 或更新版本
    
      - Exchange 2016 CU4 或更新版本

2.  如果您的公用資料夾內部部署，您必須設定 Exchange 混合式環境。 請參閱[Exchange Server 混合部署](https://technet.microsoft.com/zh-tw/library/jj200581\(v=exchg.150\))如需詳細資訊。

**移轉指示**

選取適當的連結下方的逐步指示執行批次移轉。

  - [使用批次移轉至 Exchange Online 的公用資料夾移轉到 Office 365 群組](https://technet.microsoft.com/zh-tw/library/mt843871\(v=exchg.150\))

  - [使用批次移轉至 Exchange 2010 公用資料夾移轉到 Office 365 群組](use-batch-migration-to-migrate-exchange-2010-public-folders-to-office-365-groups-exchange-2013-help.md)

  - [使用批次移轉至 Exchange 2013 公用資料夾移轉到 Office 365 群組](use-batch-migration-to-migrate-exchange-2013-public-folders-to-office-365-groups-exchange-2013-help.md)

  - [使用批次移轉以移轉 Exchange 2016 公用資料夾遷移至 Office 365 群組](https://go.microsoft.com/fwlink/p/?linkid=859171)
