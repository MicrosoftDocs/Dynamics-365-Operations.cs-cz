---
title: Výchozí protiúčty pro deníky faktur dodavatele a deníky schvalování faktur
description: Toto téma vám pomůže s rozhodnutím, kam chcete přiřadit výchozí účty pro deníky faktur.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cf772a0f0f9f99519322be1f37f961dc0ab2500
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/25/2019
ms.locfileid: "896757"
---
# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="65083-103">Výchozí protiúčty pro deníky faktur dodavatele a deníky schvalování faktur</span><span class="sxs-lookup"><span data-stu-id="65083-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65083-104">Výchozí protiúčty se používají v následující stránkách deníku faktury dodavatele:</span><span class="sxs-lookup"><span data-stu-id="65083-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="65083-105">Deník faktur</span><span class="sxs-lookup"><span data-stu-id="65083-105">Invoice journal</span></span>
-   <span data-ttu-id="65083-106">Deník schválených faktur</span><span class="sxs-lookup"><span data-stu-id="65083-106">Invoice approval journal</span></span>

<span data-ttu-id="65083-107">Podle následující tabulky se rozhodněte, kam chcete přiřadit výchozí účty pro deníky faktur.</span><span class="sxs-lookup"><span data-stu-id="65083-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65083-108">Zde nastavte výchozí účty</span><span class="sxs-lookup"><span data-stu-id="65083-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="65083-109">Kde jsou zadávány výchozí účty</span><span class="sxs-lookup"><span data-stu-id="65083-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="65083-110">Jaký má tato možnost vliv na zpracování</span><span class="sxs-lookup"><span data-stu-id="65083-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="65083-111">Kdy použít tuto možnost</span><span class="sxs-lookup"><span data-stu-id="65083-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65083-112"><strong>Skupina dodavatelů</strong> – nastavte kódů na výchozí protiúčty pro skupiny dodavatelů na stránce <strong>Výchozí nastavení účtu</strong>, kterou lze otevřít ze stránky <strong>Skupiny dodavatelů</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="65083-113">Účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="65083-113">Vendor account</span></span></li>
<li><span data-ttu-id="65083-114">Položky deníku pro účty dodavatele ve skupině dodavatelů, nejsou-li účty uvedeny pro účty dodavatelů</span><span class="sxs-lookup"><span data-stu-id="65083-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="65083-115">Výchozí protiúčty pro skupiny dodavatelů se zobrazí jako na výchozí protiúčty pro dodavatele na stránce <strong>Výchozí nastavení účtu</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="65083-116">Můžete otevřít tuto stránku na stránce se seznamem <strong>Všichni dodavatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="65083-117">Tuto možnost použijte, pokud obvykle platíte za stejné typy věcí ze stejné skupiny dodavatelů během času.</span><span class="sxs-lookup"><span data-stu-id="65083-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65083-118"><strong>Účet dodavatele</strong> – nastavte kódů na výchozí účty pro účty dodavatelů na stránce <strong>Výchozí nastavení účtu</strong>, kterou lze otevřít ze stránky <strong>Dodavatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="65083-119">Položky deníku pro účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="65083-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="65083-120">Výchozí protiúčty pro účty dodavatele jsou zobrazeny jako výchozí protiúčty pro položky deníku pro účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="65083-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="65083-121">Tuto možnost použijte, pokud obvykle platíte za stejné typy věcí od stejných dodavatelů během času.</span><span class="sxs-lookup"><span data-stu-id="65083-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65083-122"><strong>Názvy deníků</strong> – nastavte výchozí protiúčty pro deníky na stránce <strong>Názvy deníků</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="65083-123">Vyberte možnost <strong>Pevný protiúčet</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="65083-124">Poznámka: není možné zadat výchozí protiúčty pro názvy deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="65083-125">Záhlaví deínku používajícího název deníku</span><span class="sxs-lookup"><span data-stu-id="65083-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="65083-126">Položky deníku v denících, které používají název deníku</span><span class="sxs-lookup"><span data-stu-id="65083-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="65083-127">Pokud je vybrána možnost <strong>Pevný protiúčet</strong> na stránce <strong>Názvy deníků</strong>, bude protiúčet pro název deníku mít přednost před výchozím protiúčtem pro dodavatele nebo skupinu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="65083-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="65083-128">Tato možnost slouží k nastavení deníků pro specifické výdaje a náklady, které jsou účtovány na konkrétní účty, bez ohledu na to, kdo je dodavatelem nebo které skupiny dodavatelů je součástí.</span><span class="sxs-lookup"><span data-stu-id="65083-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65083-129"><strong>Názvy deníků</strong> – nastavte výchozí protiúčty pro deníky na stránce <strong>Názvy deníků</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="65083-130">Zrušte výběr možnosti <strong>Pevný protiúčet</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="65083-131">Poznámka: není možné zadat výchozí protiúčty pro názvy deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="65083-132">Záhlaví deníku</span><span class="sxs-lookup"><span data-stu-id="65083-132">Journal header</span></span></li>
<li><span data-ttu-id="65083-133">Položky deníku v denících, které používají název deníku</span><span class="sxs-lookup"><span data-stu-id="65083-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="65083-134">Tyto výchozí položky se používají na stránkách pro záhlaví deníku a protiúčet na stránce pro záhlaví deníku se používá jako výchozí položka na stránkách pro doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="65083-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="65083-135">Výchozí účty na stránce <strong>Názvy deníku </strong>se používají pouze v případě, že nejsou nastaveny výchozí účty pro účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="65083-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="65083-136">Tato možnost slouží k vytvoření výchozích účtů, které použijete, pokud protiúčet dodavatele není přiřazen.</span><span class="sxs-lookup"><span data-stu-id="65083-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65083-137"><strong>Záhlaví deníku</strong> – Nastavte výchozí protiúčet pro deník, který má být použit jako výchozí položka na stránkách pro doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="65083-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="65083-138">Mějte na paměti, že není možné zadat výchozí protiúčty pro záhlaví deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</span><span class="sxs-lookup"><span data-stu-id="65083-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="65083-139">Položky deníku v deníku</span><span class="sxs-lookup"><span data-stu-id="65083-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="65083-140">Výchozí protiúčet pro deník se používá jako výchozí položka na stránkách pro doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="65083-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="65083-141">Tato možnost slouží k urychlení zadávání dat, pokud většina položek v deníku má stejný protiúčet.</span><span class="sxs-lookup"><span data-stu-id="65083-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>





