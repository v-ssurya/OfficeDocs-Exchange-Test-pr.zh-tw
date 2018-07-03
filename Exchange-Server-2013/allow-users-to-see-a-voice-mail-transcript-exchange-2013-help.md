﻿---
title: '允許使用者查看將語音郵件文字記錄: Exchange Online Help'
TOCTitle: 允許使用者查看將語音郵件文字記錄
ms:assetid: c5192e05-905c-440f-beec-1f697edc15b3
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Ff629381(v=EXCHG.150)
ms:contentKeyID: 51409242
ms.date: 05/23/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 允許使用者查看將語音郵件文字記錄

 

_**適用版本：** Exchange Online, Exchange Server 2013, Exchange Server 2016_

_**上次修改主題的時間：** 2016-12-09_

語音郵件預覽是一種功能，可接收其語音郵件訊息從整合通訊 (UM) 的使用者。語音郵件預覽增強現有的 UM 語音信箱功能提供音訊錄製的文字版本。語音郵件文字會顯示在MicrosoftOutlook Web App、 Outlook 2010及更新版本、 內的電子郵件及其他支援的電子郵件程式\]。如需詳細資訊，查看[Microsoft 語音技術](http://go.microsoft.com/fwlink/p/?linkid=187348)。

## 使用者需使用特定的電子郵件程式嗎？

「 否 」。任何電子郵件程式，包括行動程式的郵件內文文字中包含語音郵件預覽。雖然使用者可以接收語音訊息使用其他電子郵件程式、 Outlook與Outlook Web App提供較佳的體驗。例如Outlook 2010及更新版本、 特定單字按一下語音郵件預覽文字中時, 播放音訊語音訊息會啟動在該 word 播放。這是有用的聆聽語音訊息的特定部分。

## 使用者可以搜尋特定的語音信箱訊息嗎？

\[是\]。單字和片語中的語音郵件預覽文字會自動地索引 ； 語音訊息就會出現在搜尋結果。Outlook 2010及更新版本或Outlook Web App，使用者也可以使用**音訊附註**\] 方塊中新增有關語音訊息文字。搜尋，使其更容易找到一則訊息也會包含下列備忘稿。

## 這項功能為何稱為「語音信箱預覽」？

請務必正確設定使用者的期望。語音郵件預覽不一定會產生來電者在其語音訊息說出相同的文字。事實上，它是一些方式通常是錯誤。若要呼叫該記錄會建議比一般可達到更完美結果。預覽建議讀者應該能夠瞭解的語音內容，這是要功能的實際功能接近 gist。

## 是什麼讓「語音信箱預覽」文字準確或不準確？

有時無法控制這些因素以及許多因素的語音郵件預覽文字的正確性而定。不過，語音郵件預覽文字是可能是更精確的時機：

  - 來電者留下簡單的語音訊息，不包括俚語、技術用語或罕見的字或片語。

  - 來電者使用的語言，輕鬆辨識及轉譯由語音郵件系統。一般而言，語音訊息 left 的來電者不太快速或太小說話和沒有強式重音將會產生更精確的句子和片語。

  - 語音訊息中不會有背景雜音和回音，且不會遺漏音訊。

## 哪些語言可以搭配「語音信箱預覽」使用？

「語音信箱預覽」文字以下列語言提供：

  - 英文 (美國) (en-US)

  - 英文 (加拿大) (en-CA)

  - 法文 (法國) (fr-FR)

  - 義大利文 (it-IT)

  - 波蘭文 (pl-PL)

  - 葡萄牙文 (葡萄牙) (pt-PT)

  - 西班牙文 (西班牙) (es-ES)

如果您有內部部署或混合式部署的 UM，您可以從[Microsoft 下載中心](https://go.microsoft.com/fwlink/?linkid=266542)下載的 UM 語言套件。

如果您有內部部署或混合部署 UM 語言套件、 撥號對應表及自動語音應答安裝之後可以設定成使用您所選擇的語言。線上客戶，您不需要安裝任何 UM 語言套件。許多公司具有一個 UM 撥號對應表。UM 會嘗試建立語音郵件預覽在預設的撥號對應表規劃語言，但只會成功如果的預設語言支援語音郵件預覽。UM 撥號對應表只可以設定為語音郵件預覽一種語言中一次建立。

若要設定 UM 以 en-US 以外的語言提供語音信箱預覽，請執行下列步驟：

1.  確認您要使用的語言支援「語音信箱預覽」。

2.  如果您有內部部署或混合式部署中，下載並安裝適當的 UM 語言套件。下載並安裝語言套件不會設定撥號對應表規劃預設語言。

3.  設定要用於語音郵件預覽語言撥號對應表。如需詳細資訊，請參閱[在 \[撥號對應表上設定的預設語言](set-the-default-language-on-a-dial-plan-exchange-2013-help.md)。

語音郵件預覽中支援的語言顯示文字的方式而定的語音訊息傳送的類型。有兩種類型：

  - **使用者未接聽電話時所錄製的語音訊息**
    
    這些訊息、 語言用於語音郵件預覽取決於發話者所使用的語言和是否支援的語言。例如，如果來電者會留下語音訊息中義大利文、 語音郵件預覽文字會出現在義大利文如果撥號對應表上已設定義大利文。不過，如果來電者會將一則訊息留在日文、 沒有語音郵件預覽文字都會隨附郵件因為日文無法使用。

  - **由 Outlook Voice Access 使用者傳送的語音訊息**
    
    Outlook語音存取使用者所傳送的郵件，語言用於語音郵件預覽是由語音郵件系統管理員所控制。即得出語音郵件預覽文字都會在相同的語音郵件系統的語言。不過，如果來電者來說語音郵件預覽不支援的語言使用Outlook語音存取並留下訊息，沒有語音郵件預覽文字都會隨附的郵件。若要深入了解Outlook語音存取，請參閱[設定 Outlook 語音存取](setting-up-outlook-voice-access-exchange-2013-help.md)。

## UM 是否可察覺出不正確的語音信箱預覽？

信賴等級決定的語音訊息所含每個語音郵件預覽。語音郵件系統措施在 \[錄製聲音完善符合文字、 數字及片語。如果輕鬆找到相符項目信賴等級為高。更高的信賴等級聯通常較高的精確度。

如果信賴等級決定要設為小於特定值、 片語**語音郵件預覽 （信賴較低）**會包含語音郵件預覽文字上方。如果信賴等級很低，最好是可能的語音郵件預覽文字就會不正確。

整合通訊會使用自動語音辨識 (ASR) 計算對預覽的信賴度，但是無法判斷哪些文字不正確、哪些正確。

不過，UM 沒有嘗試了解如何改善其語音郵件預覽的正確性。例如，它嘗試與使用者的個人連絡人與您的組織通訊錄或社交網路連絡人符合來電者的電話號碼 （如有）。如果 UM 找到相符項目，它會時執行錄音 ASR 包括來電者，以及其名稱及字的標準清單的名稱。

## 如果「語音信箱預覽」不是完全準確，能夠使用嗎？

如果不要嘗試讀取預覽太謹慎、 依據英文單字使用者可能會有較佳的經驗與語音郵件預覽。而這些應尋找名稱、 電話號碼及如"撥打本人回復 」 或 「 我需要會談"可以提供有關通話的用途線索的片語。

「預覽語音預覽」不一定能準確地述說訊息，不過可幫助使用者回答如下的問題：

  - 這個語音訊息是否和我的工作有關？

  - 這個語音訊息對我很重要嗎？

  - 來電者未留下數字吗？為不同的它們可能列出任何數字吗？

  - 來電者是否認為這個語音訊息是急迫的？

  - 我是否應該暫停會議，回電給這個人？

  - 我已預期呼叫來確認 「 我的要求。這是確認通話吗？

## 「語音信箱預覽」能夠開啟或關閉嗎？

\[是\]。如果您已啟用語音郵件預覽，使用者可以開啟或關閉使用Outlook 2010或更新版本或Outlook Web App。不過，撥號計劃語言必須支援語音郵件預覽，而且必須安裝該語言的 UM 語言套件。

雖然不論使用者是使用 Outlook 2010 (或更新版本) 還是 Outlook Web App，「語音信箱預覽」設定都是相同的，但是存取方式不同：

**Outlook Web App**

若要存取Outlook Web App的語音郵件預覽設定，使用者按一下 \[**設定**\] \>**電話**\>**語音信箱**。在 \[**語音信箱**\] 頁面上設定位於下方**語音郵件預覽**。

根據預設，這兩個語音郵件預覽時可使用選項使用者啟用整合通訊。如果 UM 撥號對應表設定成使用支援語音郵件預覽的 UM 語言套件，整合通訊會建立語音郵件預覽的使用者時：

  - 使用者未接聽電話，因此來電者留下語音信箱訊息。

  - 已啟用 UM 的使用者登入 Outlook Voice Access，並且錄製語音訊息給一或多個收件者。

時選取 \[語音郵件並**包含預覽文字的語音訊息我收到**來電者離開、 整合通訊會建立電子郵件訊息中的語音郵件預覽附加的音訊檔案，並將其傳送給收件者的信箱。要停用此選項如果已在撥號對應表的語言不包含語音郵件預覽支援及不想語音郵件訊息中包含的語音郵件預覽。

當使用者登入Outlook Voice Access 和其傳送語音訊息給另一位使用者，他們可能會想要清除**包含我傳送透過 Outlook 語音存取語音郵件預覽文字**\] 核取方塊。例如，它們可能會想為達成此目的如果他們正在傳送語音訊息中的語音郵件預覽不支援的語言或他們不想要包含語音訊息語音郵件預覽因為太長。
