﻿---
title: '就地保留與訴訟暫止: Exchange Online Help'
TOCTitle: 就地保留與訴訟暫止
ms:assetid: 71031c06-852d-44d8-b558-dff444eaef8c
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Ff637980(v=EXCHG.150)
ms:contentKeyID: 50473464
ms.date: 04/24/2018
mtps_version: v=EXCHG.150
ms.translationtype: HT
---

# 就地保留與訴訟暫止

 

_**適用版本：** Exchange Online, Exchange Server 2013_

_**上次修改主題的時間：** 2017-11-15_

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.note(EXCHG.150).gif" title="注意事項" alt="注意事項" />注意事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>我們已延後 2017 年 7 月 1 日的期限以在 Exchange Online 中建立新的就地保留 (在 Office 365 和 Exchange Online 獨立計劃中)。但今年稍晚或明年初，您將無法在 Exchange Online 中建立新的就地保留。使用就地保留的替代方法是，您可以使用 <a href="https://go.microsoft.com/fwlink/?linkid=780738">eDiscovery 案例</a>或 Office 365 安全性和規範中心的<a href="https://go.microsoft.com/fwlink/?linkid=827811">保留原則</a>。在我們解除委任新就地保留後，您仍然可以修改現有的就地保留，而在 Exchange Server 2013 和 Exchange混合部署中建立新的就地保留仍會受到支援。而且，您依然能夠讓信箱處於「訴訟暫止」。</td>
</tr>
</tbody>
</table>


如果合理預期到訴訟的可能性，組織就需要保留與案件相關的電子儲存資訊 (ESI)，包括電子郵件。了解案件的特定資料之前通常會有此預期心理，而且需要保留的資料範圍通常很廣。組織可能必須保留所有與特定主題相關的電子郵件，或是有關特定個人的所有電子郵件。取決於組織的電子化探索 (eDiscovery) 實務，可以採取下列措施來保留電子郵件：

  - 組織可能會要求使用者不要刪除任何郵件，並妥善保留電子郵件。不過，使用者仍可能故意或不小心刪除電子郵件。

  - 例如通訊記錄管理 (MRM) 之類的自動刪除機制，可能會遭到擱置。如此一來，大量的電子郵件會塞滿使用者信箱，進而影響使用者生產力。即使擱置自動刪除機制，也無法防止使用者以手動方式刪除電子郵件。

  - 某些組織會將電子郵件複製或是移至封存中，確保它們不會遭到刪除、更動或竄改。不管是以人工方式將郵件複製或移動至封存，還是使用 Exchange 以外的協力廠商產品來收集並儲存電子郵件，都會導致成本增加。

如果組織無法保留電子郵件，會暴露在法律與財務風險之中，例如被要求檢查組織的記錄保留與搜索流程、錯誤的法律判斷、禁運或罰鍰等。

您可以使用就地保留或訴訟暫止功能來達成下列目標：

  - 保留使用者信箱並永遠維持信箱項目不變。

  - 保留由使用者或自動刪除程序 (例如 MRM) 刪除的信箱項目。

  - 使用查詢式就地保留功能來搜尋並保留符合指定條件的項目。

  - 無限期或於指定期間內保留項目。

  - 針對不同案例或調查，對使用者進行多項保留。

  - 無需暫停 MRM，讓使用者不會察覺到被保留。

  - 針對暫停使用的項目啟用就地 eDiscovery 搜尋。

**目錄**

就地保留案例

就地保留與訴訟暫止

將信箱設定為就地保留狀態

將公用資料夾設定為保留狀態

保留和可復原的項目資料夾

保留和信箱配額

保留和電子郵件轉寄

保留封存的 Lync 內容

刪除保留狀態的信箱

將處於保留狀態的信箱從 Exchange 2013 移轉至 Office 365

## 就地保留案例

在 Exchange Server 2010 中，合法保留的概念是無限期保留使用者的所有信箱資料，或保留至撤除保留為止。在 Exchange 2013 中，就地保留功能引進了一個新模式，允許您指定下列參數：

  - **保留的項目**   可以使用關鍵字、寄件者與收件者、開始與結束日期等查詢參數來指定要保留的項目，以及指定電子郵件訊息或行事曆項目等想要保留的郵件類型。

  - **保留期限**   您可以指定項目的保留期間。

藉由使用此新的模式，就地保留功能允許針對以下情況建立更精細的保留原則來保留信箱項目：

  - **無限期保留**   此無限期保留情況類似於訴訟暫止。其目的在於保留信箱項目，您便可符合 eDiscovery 的要求。絕不會在訴訟或調查期間刪除項目。因為無法事先得知持續時間，因此未設定結束日期。為了無限期保留所有郵件項目，請勿在建立就地保留時指定任何查詢參數或持續時間。

  - **查詢式保留**   如果您的組織根據指定的查詢參數來保留項目，您便可以使用查詢式就地保留。您可以指定關鍵字、開始與結束日期、寄件者與收件者地址及郵件類型等查詢參數。在建立查詢式就地保留之後，即可保留所有符合查詢參數的現有及未來信箱項目 (包括日後收到的郵件)。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Bb124558.important(EXCHG.150).gif" title="重要事項" alt="重要事項" />重要事項：</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>標示為無法搜尋的項目 (通常是由於無法編製附件索引) 也會被保留，因為無法判斷其是否符合查詢參數。如需無法搜尋的項目相關詳細資訊，請參閱 <a href="unsearchable-items-in-exchange-ediscovery-exchange-2013-help.md">Exchange eDiscovery 中項目] 無法搜尋</a>。</td>
    </tr>
    </tbody>
    </table>


  - **時間型保留**   就地保留和訴訟暫止功能允許您指定項目的持續保留時間。持續時間自接收或建立信箱項目的日期開始計算。
    
    如果您的組織需要將所有信箱項目保留一段特定時間 (例如七年)，則您可以建立時間型保留。在 Exchange 2013 中，您可以指定保留項目的保留時間。保留項目會依據其接收日期開始逐漸日久。例如，假設以時間為基礎的就地保留信箱的保留期間設定為 365 天。如果該信箱內的項目在收到後的 300 天遭到刪除，則在永久刪除前，該項目會額外保留 65 天。以時間為基礎的就地保留功能可配合保留原則使用，以確保能持續保留項目至指定期間並於到期後永久刪除。

您可以使用就地保留功能將使用者設定為多項保留狀態。當使用者處於多項保留狀態時，會結合任何查詢式保留的搜尋查詢 (使用 **OR** 運算子)。在此情況下，信箱上所有查詢式保留中關鍵字的數目上限是 500。如果超過 500 個關鍵字，則信箱中的所有內容都會被保留 (不只是符合搜尋條件的內容)。關鍵字總數減少到 500 或以下之前，會保留所有內容。

回到頁首

## 就地保留與訴訟暫止

Exchange 2013 仍提供於 Exchange 2010 中所引進用以保留 eDiscovery 資料的訴訟暫止保留功能。訴訟暫止功能會使用信箱的 **LitigationHoldEnabled** 屬性。就地保留會根據查詢參數及設置多項保留的能力來提供更精細的保留功能，而訴訟暫止僅允許保留所有項目。信箱處於訴訟暫止狀態時，您也可以指定項目的持續保留時間。持續時間自接收或建立信箱項目的日期開始計算。如果未設定持續時間，則會無限期保留項目，或將項目保留到移除保留為止。

當信箱上同時設定了一或多項就地保留以及訴訟暫止 (未設定持續時間)，則會無限期保留所有項目或是直到撤除保留狀態為止。如果在撤除訴訟暫止之後，使用者仍處於一項或多項就地保留，便會按該保留設定所指定的持續時間保留符合就地保留標準的項目。當您將 Exchange 2010 中設定為訴訟暫止狀態的信箱移至 Exchange 2013 信箱伺服器時，則會持續套用訴訟暫止設定，以確保在移動期間和之後能符合規範要求。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.note(EXCHG.150).gif" title="注意事項" alt="注意事項" />注意事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>當您對信箱進行就地保留或訴訟暫止時，會同時保留主要和封存信箱。如果您在 Exchange 混合式部署中對內部部署主要信箱進行保留，雲端型封存信箱 (如果已啟用) 也會保留。</td>
</tr>
</tbody>
</table>


如需詳細資訊，請參閱：

  - [將信箱設為訴訟暫止](place-a-mailbox-on-litigation-hold-exchange-2013-help.md)

  - [將所有的信箱就地保留](place-all-mailboxes-on-hold-exchange-2013-help.md)

## 將信箱設定為就地保留狀態

已經新增至 [探索管理](discovery-management-exchange-2013-help.md) 角色型存取控制 (RBAC) 角色群組，或是已經指派合法保留及信箱搜尋管理角色的授權使用者，可以將信箱使用者設定為就地保留狀態。您可以將工作委派給組織法務部門裡的記錄管理員、法務人員或是律師，但指派最少的權限。若要了解關於指派 探索管理 角色群組的相關資訊，請參閱[Exchange 中指派 eDiscovery 權限](assign-ediscovery-permissions-in-exchange-exchange-2013-help.md)。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.important(EXCHG.150).gif" title="重要事項" alt="重要事項" />重要事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>在 Exchange 2010 中，合法保留角色已提供使用者足夠的權限將信箱設定為訴訟暫止狀態。在 Exchange 2013 中，您可以使用相同的權限設定信箱無限期或以時間為基礎的就地保留功能。不過，若想建立一個查詢式就地保留，必須將信箱搜尋角色指派給使用者。探索管理 角色群組同時具有這兩個指派的角色。</td>
</tr>
</tbody>
</table>


在 Exchange 2013 中，就地保留功能已和就地 eDiscovery 搜尋整合在一起。您可以使用 Exchange 系統管理中心 (EAC) 中的**就地 eDiscovery &保留**精靈或 Exchange 管理命令中的 **New-MailboxSearch** 的相關指令程式將信箱設定為就地保留狀態。若要深入了解將信箱設定為就地保留的相關資訊，請參閱[建立或移除就地保留](create-or-remove-an-in-place-hold-exchange-2013-help.md)。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.note(EXCHG.150).gif" title="注意事項" alt="注意事項" />注意事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>如果您使用 Exchange Online 封存為內部部署信箱佈建一個雲端型封存，則必須從您的內部部署 Exchange 2013 組織中管理就地保留。保留設定會透過 DirSync 自動傳播至雲端型封存。如先前所述，當您對內部部署信箱進行保留，對應的雲端型封存也會保留。</td>
</tr>
</tbody>
</table>


許多組織會要求當使用者處於保留狀態時，必須通知使用者。此外，當信箱處於保留狀態，就不需要暫停任何適用信箱使用者的保留原則。由於郵件會如預期持續遭到刪除，使用者可能不會注意到自己正處於保留狀態。如果您的組織要求通知處於保留狀態的使用者，您可以將通知郵件新增至信箱使用者的 **Retention Comment** 屬性，並使用 **RetentionUrl** 屬性來連結至包含更多資訊的網頁。Outlook 2010 和更新版本會在背景區顯示該通知和 URL。您必須使用命令介面為信箱新增並管理這些屬性。

回到頁首

## 將公用資料夾設定為保留狀態

在 Exchange Online 中，您可以使用就地保留將公用資料夾設定為保留狀態。不支援對公用資料夾使用訴訟暫止。當您建立就地保留時，唯一的選項是保留您組織中所有的公用資料夾。結果是所有公用資料夾信箱都會設定為就地保留。

此外，當您將公用資料夾設定為就地保留，也會保留與公用資料夾階層同步處理程序相關的電子郵件訊息。這可能會導致數千項與階層同步處理相關的電子郵件項目被保留。這些訊息可能會填滿公用資料夾信箱上 \[可復原的項目\] 資料夾的儲存空間配額。若要避免這種情況，您可以建立查詢式就地保留，並將下列 `property:value` 配對新增到搜尋查詢中：

    NOT(subject:HierarchySync*)

結果是主旨行中包含「HierarchySync」字詞的任何郵件 (與公用資料夾階層的同步處理相關) 皆不會被保留。

## 保留和可復原的項目資料夾

就地保留和訴訟暫止使用 \[可復原的項目\] 資料夾來保留項目。\[可復原的項目\] 資料夾會取代舊版 Exchange 中非正式地稱為*暫放*的功能。在 Outlook、Outlook Web App 與其他電子郵件用戶端的預設檢視中，不會顯示 \[可復原的項目\] 資料夾。若要深入了解 \[可復原的項目\] 資料夾，請參閱 [可復原的項目資料夾](recoverable-items-folder-exchange-2013-help.md)。

當使用者刪除來自 \[已刪除的項目\] 資料夾以外之資料夾的郵件時，該郵件預設會移至 \[已刪除的項目\] 資料夾。這就是所謂的*移動*。當使用者*虛刪除*項目 (按住 SHIFT 鍵再按 DELETE 鍵) 或是從 \[已刪除的項目\] 資料夾中刪除項目，該郵件就會移至 \[可復原的項目\] 資料夾，而不會顯示在使用者的檢視當中。

\[可復原的項目\] 資料夾中的項目，會依據使用者信箱資料庫上所設定的已刪除項目保留期間來進行保留。根據預設，信箱資料庫會將已刪除項目的保留期間設為 14 天。您也可以為 \[可復原的項目\] 資料夾設定儲存配額。如此一來，組織便可免於因為 \[可復原的項目\] 資料夾快速成長 (進而導致信箱資料庫成長) 而引發的阻斷服務 (DoS) 攻擊風險。如果信箱未置於就地保留狀態或訴訟暫止狀態，當超出 \[可復原的項目\] 警告配額，或是該項目位於資料夾的時間超過刪除的項目保留期間，系統就會依據先進先出的方式永久清除項目。

\[可復原的項目\] 資料夾包含下列子資料夾，用於將刪除的項目儲存在不同的站台中以利就地保留和訴訟暫止：

  - **Deletions**   從 \[已刪除的項目\] 資料夾中移除或是從其他資料夾虛刪除的項目，都會被移至「刪除」子資料夾，使用者只要在 Outlook 和 Outlook Web App 中使用「復原刪除的郵件」功能，就可以看到這些項目。這些項目預設會駐留在此資料夾中，直到信箱資料庫或信箱上設定之已刪除的項目保留期間到期為止。

  - **Purges**   當使用者從 \[可復原的項目\] 資料夾 (使用 Outlook 和 Outlook Web App 中的「復原刪除的項目」工具) 中刪除項目，該項目就會移至 \[清除\] 資料夾。當項目超出信箱資料庫或信箱上設定的已刪除項目保留期間，也會移至 \[清除\] 資料夾。如果使用者使用「復原刪除的項目」工具，則不會看到此資料夾中的項目。當信箱助理員開始處理信箱時，會清除位於信箱資料庫中 \[清除\] 資料夾裡的項目。當您將信箱使用者設為訴訟暫止時，信箱助理員不會清除此資料夾中的項目。

  - **DiscoveryHold**   如果使用者處於就地保留狀態，刪除的郵件便會移至此資料夾。當信箱助理員開始處理信箱時，會評估此資料夾裡的郵件。符合就地保留查詢的項目會保留至該查詢中指定的保留期間為止。如果未指定保留期間，則會無限期保留項目直到將該使用者撤除保留為止。

  - **Versions**   當使用者處於就地保留或訴訟暫止狀態時，必須防止使用者或程序竄改或修改信箱項目。使用*寫入時複製*可達到此目的。當使用者或程序變更信箱項目的特定屬性時，會在變更完成之前在 \[版本\] 資料夾中儲存一份原始項目副本。若有後續變更，則會重複進行此程序。\[版本\] 資料夾內擷取的項目也同時加入了索引並會出現在就地 eDiscovery 搜尋的結果中。撤除保留後，受管理的資料夾助理員會移除 \[版本\] 資料夾中的副本。

### 觸發寫入時複製的內容

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>項目類型</th>
<th>觸發寫入時複製的內容</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>郵件 (IPM.Note*)</p>
<p>文章 (IPM.Post*)</p></td>
<td><ul>
<li><p>主旨</p></li>
<li><p>本文</p></li>
<li><p>附件</p></li>
<li><p>寄件者/收件者</p></li>
<li><p>傳送/接收日期</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>郵件與文章以外的項目</p></td>
<td><p>除以下內容外的任何可見內容變更：</p>
<ul>
<li><p>項目位置 (當項目在資料夾之間移動)</p></li>
<li><p>項目狀態變更 (閱讀或未閱讀)</p></li>
<li><p>套用至某個項目的保留標記變更</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>預設資料夾 [草稿] 中的項目</p></td>
<td><p>無 (免除寫入時複製的 [草稿] 資料夾中的項目)</p></td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.important(EXCHG.150).gif" title="重要事項" alt="重要事項" />重要事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>當收到出席者的會議回應以及更新會議的追蹤資訊時，召集人信箱中的行事曆項目會停用寫入時複製。對於行事曆項目和有設定提醒的項目，會停用 ReminderTime 及 ReminderSignalTime 內容的寫入時複製。寫入時複製不會擷取對這些內容所做的變更。寫入時複製不會擷取對 RSS 摘要所做的變更。</td>
</tr>
</tbody>
</table>


雖然使用者看不到 \[DiscoveryHold\]、\[清除\] 與 \[版本\] 資料夾，Exchange 搜尋還是會對 \[可復原的項目\] 資料夾中的所有項目編製索引，以便透過就地 eDiscovery 來搜索所有項目。當撤除信箱使用者的就地保留或訴訟暫止狀態後，受管理的資料夾助理員會清除 \[DiscoveryHold\]、\[清除\] 與 \[版本\] 資料夾中的項目。

回到頁首

## 保留和信箱配額

\[可復原的項目\] 資料夾中的項目，不是依據使用者信箱配額來計算。在 Exchange 中，\[可復原的項目\] 資料夾擁有自己的配額。針對 Exchange，*RecoverableItemsWarningQuota* 和 *RecoverableItemsQuota* 信箱內容的預設值分別設定為 20 GB 和 30 GB。若要為 Exchange Server 2013 修改信箱資料庫的這些值，請使用 [Set-MailboxDatabase](https://technet.microsoft.com/zh-tw/library/bb123971\(v=exchg.150\)) Cmdlet。若要修改個別信箱的這些值，請使用 [Set-Mailbox](https://technet.microsoft.com/zh-tw/library/bb123981\(v=exchg.150\)) Cmdlet。

當使用者的 \[可復原的項目\] 資料夾超出可復原項目的警告配額 (按照 *RecoverableItemsWarningQuota* 參數所指定)，就會在信箱伺服器的應用程式事件記錄中記錄此事件。當資料夾超出可復原項目的配額 (按照 *RecoverableItemsQuota* 參數所指定)，使用者將無法清空 \[已刪除的項目\] 資料夾，或是永久刪除信箱項目。此外，「寫入時複製」功能將無法對修改的項目建立副本。因此，請務必針對處於就地保留狀態的信箱使用者，監視其可復原的項目配額。

在 Exchange Online 中，當您對信箱進行訴訟暫止或就地保留，\[可復原的項目\] 資料夾 (位於使用者主要信箱中) 的配額會自動增加到 100 GB。在保留信箱的主要信箱中，當 \[可復原的項目\] 資料夾的儲存配額接近限制時，您可以執行下列動作︰

  - **啟用封存信箱和開啟自動展開封存**   您只要啟用封存信箱，然後開啟 Exchange Online 中的自動展開封存功能，就可以啟用 \[可復原的項目\] 資料夾的無限制儲存容量。如此，主要信箱中的 \[可復原的項目\] 資料夾會有 100 GB，而使用者封存中的 \[可復原的項目\] 資料夾會有無限制的儲存容量。請參閱作法：[在 Office 365 安全與規範中心啟用封存信箱](https://go.microsoft.com/fwlink/p/?linkid=863320)以及[在 Office 365 中啟用無限制封存](https://go.microsoft.com/fwlink/p/?linkid=844569)。
    
    **附註：** 
    
      - 針對快要超過 \[可復原的項目\] 資料夾儲存配額的信箱，在啟用封存之後，您可以執行「受管理的資料夾助理員」來手動觸發助理員處理此信箱，讓過期的項目移至封存信箱中的 \[可復原的項目\] 資料夾。如需相關指示，請參閱[為處於保留狀態的信箱增加 \[可復原的項目\] 配額](https://go.microsoft.com/fwlink/p/?linkid=786479)中的步驟 4。
    
      - 請注意，使用者信箱中的其他項目可能移至新的封存信箱。啟用封存信箱之後，請考慮告訴使用者可能有這種情形。

  - **為保留信箱建立自訂保留原則**    除了對訴訟暫止或就地保留的信箱啟用封存信箱和自動展開封存，您也可以為保留信箱建立自訂保留原則。這可讓您將保留原則套用至保留信箱，不同於在未保留信箱上套用的預設 MRM 原則。這可讓您套用專為保留信箱所設計的保留標籤。這包括為 \[可復原的項目\] 資料夾建立新的保留標籤。

如需詳細資訊，請參閱[為處於保留狀態的信箱增加 \[可復原的項目\] 配額](https://go.microsoft.com/fwlink/p/?linkid=786479)。

## 保留和電子郵件轉寄

使用者可以使用 Outlook 和 Outlook Web App 來設定信箱的電子郵件轉寄功能。電子郵件轉寄功能可讓使用者設定信箱，以將傳送至其信箱的電子郵件訊息轉寄至位於組織內或組織外的另一個信箱。可設定電子郵件轉寄功能，讓傳送到原始信箱的郵件不會複製到該信箱，只會傳送到轉寄的地址。

如果信箱設定了電子郵件轉寄功能，郵件不會複製到原始信箱，那如果該信箱處於保留狀態會發生什麼情況？情況會根據該信箱是在 Exchange 2013 或 Exchange Online 組織中而有不同。

  - **Exchange Online**   在傳送程序期間已檢查信箱的保留設定。如果郵件符合信箱的保留條件，郵件的複本會儲存到 \[可復原的項目\] 資料夾中。這表示您可以使用就地 eDiscovery 來搜尋原始信箱，尋找轉寄到另一個信箱的郵件。

  - **Exchange 2013**   如果郵件轉寄到另一個信箱，且未複製到原始信箱，則這些郵件並未擷取及複製到 \[可復原的項目\] 資料夾中。這代表轉寄的郵件無法在就地 eDiscovery 搜尋中傳回。若要解決此問題，Exchange 2013 組織可以考慮移除讓使用者設定電子郵件轉寄的功能。

回到頁首

## 保留封存的 Lync 內容

Exchange 2013、Microsoft Lync 2013 和 Microsoft SharePoint 2013 提供整合式保留和 eDiscovery 體驗，可讓您在不同的儲存區中保留和搜尋項目。Exchange 2013 容許您在 Exchange 中封存 Lync Server 2013 內容，免除了必須分離 SQL Server 資料庫以儲存封存的 Lync 內容的需求。SharePoint 2013 內建的保留和 eDiscovery 功能允許您透過單一主控台在所有儲存區間保留和搜尋資料。

將 Exchange 2013 信箱設定為就地保留或訴訟暫止狀態時，Microsoft Lync 2013 內容 (例如，即時訊息對話和線上會議中分享的檔案) 會封存在信箱中。如果使用 Microsoft SharePoint 2013 中的 eDiscovery 中心或 Exchange 2013 中的就地 eDiscovery 搜尋信箱，任何符合該搜尋查詢的封存 Lync 內容也會出現在搜尋結果中。您也可以限定搜尋封存於該信箱內的 Lync 內容。

若要能夠封存 Exchange 2013 信箱內的 Lync 內容，您必須設定將 Exchange 2013 與 Lync 2013 整合。如需詳細資料，請參閱下列主題：

  - [規劃封存](https://technet.microsoft.com/zh-tw/library/jj205069\(v=ocs.15\))

  - [部署封存](https://technet.microsoft.com/zh-tw/library/jj205147\(v=ocs.15\))

回到頁首

## 刪除保留狀態的信箱

當您刪除已進行訴訟暫止或就地保留的信箱時，結果會根據信箱是在 Exchange 2013 或 Exchange Online 組織中而有不同。

  - **Exchange 2013**   如果系統管理員刪除的使用者帳戶有信箱，則 Exchange 資訊儲存庫最終會偵測到信箱已不再連接到使用者帳戶，並將該信箱標示為待刪除，即使信箱已保留。若您想保留信箱，必須執行下列作業：
    
    1.  不要刪除使用者帳戶，而是停用使用者帳戶。
    
    2.  變更信箱的屬性，以限制其對信箱的使用和存取。例如，將收發配額設為 1，封鎖可以傳送訊息至信箱的人，並限制可以存取信箱的對象。
    
    3.  保留信箱直到所有資料皆刪除，或直到不再需要保留資料。

  - **Exchange Online**   如果使用者的信箱處於就地保留或訴訟暫止狀態，且對應的 Office 365 帳戶已刪除，則信箱會轉換為*非作用中信箱*，這是一種虛刪除的信箱。非作用中信箱可在使用者離開組織後保留使用者的信箱內容。非作用中信箱的項目之保留期限為信箱成為非作用中之前信箱的保留時間。這可讓系統管理員、法務人員或記錄管理員使用「就地 eDiscovery」功能，存取及搜尋非作用中信箱的內容。非使用中的信箱無法接收電子郵件，也不會顯示在組織的共用通訊錄或其他清單中。如需詳細資訊，請參閱[Exchange Online 中的非使用中信箱](https://technet.microsoft.com/zh-tw/library/dn798632\(v=exchg.150\))。

回到頁首

## 將處於保留狀態的信箱從 Exchange 2013 移轉至 Office 365

如果您擁有 Exchange 混合部署，當您將內部部署 Exchange 2013 信箱移動 (上架) 到 Office 365 中的 Exchange Online 時，會發生下列狀況：

  - 如果內部部署信箱處於訴訟暫止或就地保留狀態，保留設定會保留到信箱移動至 Exchange Online 之後。

  - 如果內部部署信箱處於訴訟暫止或就地保留狀態，\[可復原的項目\] 資料夾中的所有內容都會移至 Exchange Online 信箱中。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.note(EXCHG.150).gif" title="注意事項" alt="注意事項" />注意事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>當您將 Exchange Online 信箱移動 (下架) 至您的內部部署 Exchange 2013 組織時，[可復原的項目] 資料夾中的保留設定和內容會同時保留。</td>
</tr>
</tbody>
</table>


還有其他方法可將內部部署電子郵件資料移轉至 Office 365，例如使用階段性 Exchange 移轉或 Exchange 完全移轉。

  - 階段性移轉可用來將信箱從 Exchange 2003 或 Exchange 2007 移轉至 Office 365。 在這些 Exchange 版本中，\[可復原的項目\] 資料夾 (以及其功能) 不存在。 因此，當您將 Exchange 2003 或 Exchange 2007 信箱移轉至 Office 365 時，就不需要移動任何 \[可復原的項目\] 資料夾內容。

  - 完全移轉可用來將信箱從 Exchange 2003、Exchange 2007 與 Exchange 2010 移轉至 Office 365。 如先前所述，Exchange 2003 和 Exchange 2007 信箱沒有要移轉的 \[可復原的項目\] 資料夾。 因為 \[可復原的項目\] 資料夾是在 Exchange 2010 中引進，所以當您使用完全移轉來移轉 Exchange 2010 信箱時，\[可復原的項目\] 資料夾中的內容就已經移轉至 Office 365。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.tip(EXCHG.150).gif" title="提示" alt="提示" />提示：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>對於 Exchange 2013 和 Exchange 2010，建議您使用 Exchange 混合部署將內部部署信箱移轉至 Office 365。</td>
</tr>
</tbody>
</table>


回到頁首
