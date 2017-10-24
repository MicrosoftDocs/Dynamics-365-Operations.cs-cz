---
title: "Výchozí protiúčty pro deníky pro faktury dodavatele a pro deníky pro schvalování faktur"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="7e8f2-102">Výchozí protiúčty pro deníky pro faktury dodavatele a pro deníky pro schvalování faktur</span><span class="sxs-lookup"><span data-stu-id="7e8f2-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="7e8f2-103">Výchozí protiúčty se používají v následující stránkách deníku faktury dodavatele:</span><span class="sxs-lookup"><span data-stu-id="7e8f2-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="7e8f2-104">Deník faktur</span><span class="sxs-lookup"><span data-stu-id="7e8f2-104">Invoice journal</span></span>
-   <span data-ttu-id="7e8f2-105">Deník schválených faktur</span><span class="sxs-lookup"><span data-stu-id="7e8f2-105">Invoice approval journal</span></span>

<span data-ttu-id="7e8f2-106">Podle následující tabulky se rozhodněte, kam chcete přiřadit výchozí účty pro deníky faktur.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e8f2-107">Zde nastavte výchozí účty</span><span class="sxs-lookup"><span data-stu-id="7e8f2-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="7e8f2-108">Kde jsou zadávány výchozí účty</span><span class="sxs-lookup"><span data-stu-id="7e8f2-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="7e8f2-109">Jaký má tato možnost vliv na zpracování</span><span class="sxs-lookup"><span data-stu-id="7e8f2-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="7e8f2-110">Kdy použít tuto možnost</span><span class="sxs-lookup"><span data-stu-id="7e8f2-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e8f2-111"><strong>Skupina dodavatelů</strong> – nastavte kódů na výchozí protiúčty pro skupiny dodavatelů na stránce <strong>Výchozí nastavení účtu</strong>, kterou lze otevřít ze stránky <strong>Skupiny dodavatelů</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="7e8f2-112">Účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="7e8f2-112">Vendor account</span></span></li>
<li><span data-ttu-id="7e8f2-113">Položky deníku pro účty dodavatele ve skupině dodavatelů, nejsou-li účty uvedeny pro účty dodavatelů</span><span class="sxs-lookup"><span data-stu-id="7e8f2-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="7e8f2-114">Výchozí protiúčty pro skupiny dodavatelů se zobrazí jako na výchozí protiúčty pro dodavatele na stránce <strong>Výchozí nastavení účtu</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="7e8f2-115">Můžete otevřít tuto stránku na stránce se seznamem <strong>Všichni dodavatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="7e8f2-116">Tuto možnost použijte, pokud obvykle platíte za stejné typy věcí ze stejné skupiny dodavatelů během času.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8f2-117"><strong>Účet dodavatele</strong> – nastavte kódů na výchozí účty pro účty dodavatelů na stránce <strong>Výchozí nastavení účtu</strong>, kterou lze otevřít ze stránky <strong>Dodavatelé</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="7e8f2-118">Položky deníku pro účet dodavatele</span><span class="sxs-lookup"><span data-stu-id="7e8f2-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="7e8f2-119">Výchozí protiúčty pro účty dodavatele jsou zobrazeny jako výchozí protiúčty pro položky deníku pro účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="7e8f2-120">Tuto možnost použijte, pokud obvykle platíte za stejné typy věcí od stejných dodavatelů během času.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8f2-121"><strong>Názvy deníků</strong> – nastavte výchozí protiúčty pro deníky na stránce <strong>Názvy deníků</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="7e8f2-122">Vyberte možnost <strong>Pevný protiúčet</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="7e8f2-123">Poznámka: není možné zadat výchozí protiúčty pro názvy deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="7e8f2-124">Záhlaví deínku používajícího název deníku</span><span class="sxs-lookup"><span data-stu-id="7e8f2-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="7e8f2-125">Položky deníku v denících, které používají název deníku</span><span class="sxs-lookup"><span data-stu-id="7e8f2-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="7e8f2-126">Pokud je vybrána možnost <strong>Pevný protiúčet</strong> na stránce <strong>Názvy deníků</strong>, bude protiúčet pro název deníku mít přednost před výchozím protiúčtem pro dodavatele nebo skupinu dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="7e8f2-127">Tato možnost slouží k nastavení deníků pro specifické výdaje a náklady, které jsou účtovány na konkrétní účty, bez ohledu na to, kdo je dodavatelem nebo které skupiny dodavatelů je součástí.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e8f2-128"><strong>Názvy deníků</strong> – nastavte výchozí protiúčty pro deníky na stránce <strong>Názvy deníků</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="7e8f2-129">Zrušte výběr možnosti <strong>Pevný protiúčet</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="7e8f2-130">Poznámka: není možné zadat výchozí protiúčty pro názvy deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="7e8f2-131">Záhlaví deníku</span><span class="sxs-lookup"><span data-stu-id="7e8f2-131">Journal header</span></span></li>
<li><span data-ttu-id="7e8f2-132">Položky deníku v denících, které používají název deníku</span><span class="sxs-lookup"><span data-stu-id="7e8f2-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="7e8f2-133">Tyto výchozí položky se používají na stránkách pro záhlaví deníku a protiúčet na stránce pro záhlaví deníku se používá jako výchozí položka na stránkách pro doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="7e8f2-134">Výchozí účty na stránce <strong>Názvy deníku </strong>se používají pouze v případě, že nejsou nastaveny výchozí účty pro účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="7e8f2-135">Tato možnost slouží k vytvoření výchozích účtů, které použijete, pokud protiúčet dodavatele není přiřazen.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e8f2-136"><strong>Záhlaví deníku</strong> – Nastavte výchozí protiúčet pro deník, který má být použit jako výchozí položka na stránkách pro doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="7e8f2-137">Poznámka: není možné zadat výchozí protiúčty pro záhlaví deníků, pokud je typ deníku u názvů deníků <strong>Registr faktur</strong> nebo <strong>Schválení</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="7e8f2-138">Položky deníku v deníku</span><span class="sxs-lookup"><span data-stu-id="7e8f2-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="7e8f2-139">Výchozí protiúčet pro deník se používá jako výchozí položka na stránkách pro doklad deníku.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="7e8f2-140">Tato možnost slouží k urychlení zadávání dat, pokud většina položek v deníku má stejný protiúčet.</span><span class="sxs-lookup"><span data-stu-id="7e8f2-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






