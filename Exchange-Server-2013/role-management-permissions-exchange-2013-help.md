﻿---
title: '角色管理權限: Exchange 2013 Help'
TOCTitle: 角色管理權限
ms:assetid: cb9591c4-fbb3-4199-8007-6bbfdfd5a2e9
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/Dd638186(v=EXCHG.150)
ms:contentKeyID: 50474237
ms.date: 05/21/2018
mtps_version: v=EXCHG.150
ms.translationtype: MT
---

# 角色管理權限

 

_**適用版本：** Exchange Online, Exchange Server 2013_

_**上次修改主題的時間：** 2015-03-09_

設定的權限執行工作所需管理角色是根據所執行的程序或您想要執行此指令程式而異。如需管理角色的詳細資訊，請參閱[了解管理角色](understanding-management-roles-exchange-2013-help.md)。

若要瞭解執行程序或執行 Cmdlet 所需的權限，請執行以下操作：

1.  在下表中，尋找與您想要執行的程序或 Cmdlet 最為相關的功能。

2.  接著查看功能所需的權限。您必須獲指派其中一個角色群組、相等的自訂角色群組，或相等的管理角色。您也可以按一下角色群組，查看其管理角色。如果功能列出多個角色群組，您只需要獲指派其中一個角色群組，就能使用功能。如需角色群組和管理角色的詳細資訊，請參閱[了解角色型存取控制](understanding-role-based-access-control-exchange-2013-help.md)。

3.  現在，執行 **Get-ManagementRoleAssignment** Cmdlet，查看指派給您的角色群組或管理角色，以瞭解您是否有管理該功能所需的權限。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Bb124558.note(EXCHG.150).gif" title="注意事項" alt="注意事項" />注意事項：</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>您必須獲指派「角色管理」管理角色，才能執行 <strong>Get-ManagementRoleAssignment</strong> Cmdlet。如果您沒有執行 <strong>Get-ManagementRoleAssignment</strong> Cmdlet 的權限，請詢問您的 Exchange 系統管理員，以取得角色群組或是獲指派管理角色。</td>
    </tr>
    </tbody>
    </table>


如果您要將管理功能的能力委派給另一個使用者，請參閱[委派角色指派](delegate-role-assignments-exchange-2013-help.md)。

## 角色管理權限

您可以使用下表中的功能來管理管理角色群組、 角色、 指派原則、 工作分派、 定義可套用至系統管理員和使用者的權限的範圍。獲指派僅檢視管理角色群組的使用者，可以檢視下表中功能的組態。如需詳細資訊，請參閱[僅限檢視組織管理](view-only-organization-management-exchange-2013-help.md)。


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>功能</th>
<th>必要的權限</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>管理角色</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="even">
<td><p>未限定範圍的管理角色</p></td>
<td><p><a href="unscoped-role-management-role-exchange-2013-help.md">未限定範圍的角色管理角色</a>管理角色</p></td>
</tr>
<tr class="odd">
<td><p>角色群組</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="even">
<td><p>指派原則</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="odd">
<td><p>角色指派</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="even">
<td><p>管理範圍</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="odd">
<td><p>管理角色項目</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="even">
<td><p>舊版權限</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p></td>
</tr>
<tr class="odd">
<td><p>Active Directory 分割權限</p></td>
<td><p><a href="organization-management-exchange-2013-help.md">組織管理</a></p>
<table>
<thead>
<tr class="header">
<th><img src="images/Bb124558.important(EXCHG.150).gif" title="重要事項" alt="重要事項" />重要事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>若要搭配 <em>PrepareAD</em> 和 <em>ActiveDirectorySplitPermissions</em> 參數執行 <code>setup.exe</code> 命令，您使用的帳戶必須是 Schema Admins 和 Enterprise Administrators 群組的成員。</td>
</tr>
</tbody>
</table>

</td>
</tr>
</tbody>
</table>
