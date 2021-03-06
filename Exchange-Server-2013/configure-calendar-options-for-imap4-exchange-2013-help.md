﻿---
title: '設定 IMAP4 的行事曆選項: Exchange 2013 Help'
TOCTitle: 設定 IMAP4 的行事曆選項
ms:assetid: 6679c8b2-3f0f-449a-a17c-a7b30001538c
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Aa998606(v=EXCHG.150)
ms:contentKeyID: 50553994
ms.date: 05/21/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 設定 IMAP4 的行事曆選項

 

_**適用版本：**Exchange Server 2013_

_**上次修改主題的時間：**2012-11-27_

您可以使用命令介面來設定您連線至其信箱使用 IMAP4 連線的使用者行事曆存取設定。您指定的設定決定如何 IMAP4 使用者可以存取其行事曆及 exchange 行事曆資訊 （例如傳送或回覆會議邀請） 與其他使用者。

如需 IMAP4 的詳細資訊，請參閱 [Exchange Server 2013 中的 POP3 和 IMAP4](pop3-and-imap4-in-exchange-server-2013-exchange-2013-help.md)。

## 開始之前有哪些須知？

  - 預估完成時間：5 分鐘。

  - 您必須已獲指派權限，才能執行此程序或這些程序。若要查看您需要的權限，請參閱 [用戶端和行動裝置權限](clients-and-mobile-devices-permissions-exchange-2013-help.md)主題中的「IMAP4 設定」項目。

  - 如需適用於此主題中程序的快速鍵相關資訊，請參閱 [Exchange 系統管理中心的鍵盤快速鍵](keyboard-shortcuts-in-the-exchange-admin-center-exchange-online-protection-help.md)。

<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.tip(EXCHG.150).gif" title="提示" alt="提示" />提示：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>有問題嗎？在 Exchange 論壇中尋求協助。 論壇的網址為：<a href="https://go.microsoft.com/fwlink/p/?linkid=60612">Exchange Server</a>、 <a href="https://go.microsoft.com/fwlink/p/?linkid=267542">Exchange Online</a> 或 <a href="https://go.microsoft.com/fwlink/p/?linkid=285351">Exchange Online Protection</a>。.</td>
</tr>
</tbody>
</table>


## 使用命令介面設定 IMAP4 的行事曆選項

此範例可讓 IMAP4 使用者使用交換行事曆資訊的 iCalendar 標準。

    Set-ImapSettings -Identity CAS01 -CalendarItemRetrievalOption iCalendar

此範例可讓 IMAP4 使用者從內部伺服器存取行事曆資訊。

    Set-ImapSettings -Identity CAS01 -CalendarItemRetrievalOption IntranetUrl 

此範例會讓 IMAP4 使用者能够在外部伺服器上從網際網路存取行事曆資訊。

    Set-ImapSettings -CalendarItemRetrievalOption InternetUrl

本範例會啟用使用直接Outlook Web App URL 來存取行事曆資訊的 IMAP4 使用者。如果您使用`Custom`，您必須指定使用*OWAServerUrl*參數 Outlook Web App URL。

    Set-Imap4Settings -CalendarItemRetrievalOption Custom -OwaServerUrl "https://OwaServer01"

您已指定 IMAP4 的行事曆選項之後，您必須重新啟動 IMAP4 服務。如需如何重新啟動 IMAP4 服務的資訊，請參閱[啟動及停止 IMAP4 服務](start-and-stop-the-imap4-services-exchange-2013-help.md)。

如需語法及參數的相關資訊，請參閱 [Set-ImapSettings](https://technet.microsoft.com/zh-tw/library/aa998252\(v=exchg.150\))。

## 如何才能了解這是否正常運作？

若要確認是否已成功設定行事曆選項，請執行下列其中一項操作：

在命令介面中執行下列命令。

    Get-ImapSettings | format-list

驗證行事曆設定是否正確。

## 相關資訊

在您設定 IMAP4 的行事曆選項之後，您可能還想要：

[設定 POP3 和 IMAP4 訊息擷取格式選項](configure-pop3-and-imap4-message-retrieval-format-options-exchange-2013-help.md)

[設定 IMAP4 的連線逾時限制](set-connection-time-out-limits-for-imap4-exchange-2013-help.md)

