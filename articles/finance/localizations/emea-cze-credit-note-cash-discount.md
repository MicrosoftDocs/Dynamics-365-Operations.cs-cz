---
title: Dobropis u hotovostní slevy
description: Toto téma obsahuje informace, které pomohou právnickým osobám v rámci České republiky vytvořit, zaúčtovat a tisknout dobropisy pro hotovostní slevy, které jsou přiřazeny odběratelům.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, PrintMgmtSetupUIMain, Reasons
audience: Application User
ms.reviewer: kfend
ms.custom: 273063
ms.search.region: Czech Republic
ms.author: kfend
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c2b0ba2c4db1a4cb80560fc7fd42f6a9e42f4f21
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975354"
---
# <a name="credit-note-on-cash-discount"></a><span data-ttu-id="c8652-103">Dobropis u hotovostní slevy</span><span class="sxs-lookup"><span data-stu-id="c8652-103">Credit note on cash discount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8652-104">Toto téma obsahuje informace, které pomohou právnickým osobám v rámci České republiky vytvořit, zaúčtovat a tisknout dobropisy pro hotovostní slevy, které jsou přiřazeny odběratelům.</span><span class="sxs-lookup"><span data-stu-id="c8652-104">This topic provides information that will help legal entities in the Czech Republic create, post, and print credit notes for cash discounts that are given to customers.</span></span>

<span data-ttu-id="c8652-105">Společnosti v rámci České republiky musí vydávat dobropisy pro hotovostní slevy, které jsou přiřazeny odběratelům.</span><span class="sxs-lookup"><span data-stu-id="c8652-105">Companies in the Czech Republic must issue credit notes for cash discounts that are given to customers.</span></span> <span data-ttu-id="c8652-106">Tyto dobropisy musí obsahovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="c8652-106">These credit notes must include the following information:</span></span>

-   <span data-ttu-id="c8652-107">Číslo faktury</span><span class="sxs-lookup"><span data-stu-id="c8652-107">Invoice number</span></span>
-   <span data-ttu-id="c8652-108">Daň z přidané hodnoty (DPH) a částka z původního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c8652-108">Value-added tax (VAT) base and amount from the original document</span></span>
-   <span data-ttu-id="c8652-109">Důvod opravy</span><span class="sxs-lookup"><span data-stu-id="c8652-109">Reason for a correction</span></span>

<a name="prerequisites"></a><span data-ttu-id="c8652-110">Požadavky</span><span class="sxs-lookup"><span data-stu-id="c8652-110">Prerequisites</span></span>
-------------

### <a name="set-up-number-sequences"></a><span data-ttu-id="c8652-111">Nastavit číselné řady</span><span class="sxs-lookup"><span data-stu-id="c8652-111">Set up number sequences</span></span>

<span data-ttu-id="c8652-112">Vytvořte souvislou číselnou řadu pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="c8652-112">Create a continuous number sequence for a legal entity.</span></span> <span data-ttu-id="c8652-113">Další informace naleznete v tématu [Přehled číselných řad](../../fin-and-ops/organization-administration/number-sequence-overview.md). Na stránce **Parametry pohledávek** vyberte číselnou řadu, kterou jste vytvořili pro **prodejní dobropis**.</span><span class="sxs-lookup"><span data-stu-id="c8652-113">For more information, see [Number sequences overview](../../fin-and-ops/organization-administration/number-sequence-overview.md) On the **Accounts receivable parameters** page, select the number sequence that you created for **Sales credit note**.</span></span> <span data-ttu-id="c8652-114">Dále byste nastavte číselnou řadu pro **prodejní doklad dobropisu**.</span><span class="sxs-lookup"><span data-stu-id="c8652-114">Additionally, set up a number sequencevfor **Sales credit note voucher**.</span></span> <span data-ttu-id="c8652-115">Můžete použít stejnou číselnou řadu, jakou jste použili **prodejní dobropis**.</span><span class="sxs-lookup"><span data-stu-id="c8652-115">You can use the same number sequence that you used for **Sales credit note**.</span></span>

### <a name="set-up-sales-tax-codes"></a><span data-ttu-id="c8652-116">Nastavit kódy DPH</span><span class="sxs-lookup"><span data-stu-id="c8652-116">Set up sales tax codes</span></span>

<span data-ttu-id="c8652-117">Další informace naleznete v tématu [Přehled o DPH](../general-ledger/indirect-taxes-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8652-117">For more information, see [Sales tax overview](../general-ledger/indirect-taxes-overview.md).</span></span>

### <a name="set-up-report-formats-for-documents"></a><span data-ttu-id="c8652-118">Nastavení formátů sestavy pro dokumenty</span><span class="sxs-lookup"><span data-stu-id="c8652-118">Set up report formats for documents</span></span>

1.  <span data-ttu-id="c8652-119">Přejděte do nabídky **Pohledávky** \> **Nastavení** \> **Formuláře** \> **Nastavení formuláře**.</span><span class="sxs-lookup"><span data-stu-id="c8652-119">Go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup**.</span></span>

2.  <span data-ttu-id="c8652-120">Na kartě **Obecné** v části **Nastavit možnosti pro formuláře odběratelů** klikněte na **Správa tisku**.</span><span class="sxs-lookup"><span data-stu-id="c8652-120">On the **General** tab, under **Set up options for customer forms**, click **Print management**.</span></span>

3.  <span data-ttu-id="c8652-121">Ve stromu rozbalte položky **Modul – pohledávky** \> **Dokumenty** \> **Faktura odběratele**.</span><span class="sxs-lookup"><span data-stu-id="c8652-121">In the tree, expand **Module - accounts receivable** \> **Documents** \> **Customer invoice**.</span></span> <span data-ttu-id="c8652-122">V poli **Název sestavy** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8652-122">In the **Report format** field, enter or select a value.</span></span>

4.  <span data-ttu-id="c8652-123">Ve stromové struktuře pod uzlem **Faktura odběratele** vyberte **Původní**.</span><span class="sxs-lookup"><span data-stu-id="c8652-123">In the tree, under the **Customer invoice** node, select **Original**.</span></span> <span data-ttu-id="c8652-124">V poli **Název sestavy** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8652-124">In the **Report format** field, enter or select a value.</span></span>

5.  <span data-ttu-id="c8652-125">Ve stromu rozbalte položky **Modul – pohledávky** \> **Dokumenty** \> **Volné faktury**.</span><span class="sxs-lookup"><span data-stu-id="c8652-125">In the tree, expand **Module - accounts receivable** \> **Documents** \> **Free text invoice**.</span></span> <span data-ttu-id="c8652-126">V poli **Název sestavy** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8652-126">In the **Report format** field, enter or select a value.</span></span>

6.  <span data-ttu-id="c8652-127">Ve stromové struktuře pod uzlem **Volná faktura** vyberte **Původní**.</span><span class="sxs-lookup"><span data-stu-id="c8652-127">In the tree, under the **Free text invoice** node, select **Original**.</span></span> <span data-ttu-id="c8652-128">V poli **Název sestavy** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8652-128">In the **Report format** field, enter or select a value.</span></span>

### <a name="set-up-customer-reason-codes"></a><span data-ttu-id="c8652-129">Nastavte kódy důvodů odběratele.</span><span class="sxs-lookup"><span data-stu-id="c8652-129">Set up customer reason codes.</span></span>

<span data-ttu-id="c8652-130">Na stránce **Kódy důvodů odběratele** (**Pohledávky** \> **Nastavení** \> **Kódy důvodů odběratele**) vytvořte nebo upravte kódy důvodů, které se používají pro opravné daňové doklady.</span><span class="sxs-lookup"><span data-stu-id="c8652-130">On the **Customer reason codes** page (**Accounts receivable** \> **Setup** \> **Customer reason codes**), create or edit the reason codes that are used for tax corrective documents.</span></span>

### <a name="set-up-accounts-receivable-parameters"></a><span data-ttu-id="c8652-131">Nastavení parametrů pohledávek</span><span class="sxs-lookup"><span data-stu-id="c8652-131">Set up Accounts receivable parameters</span></span>

<span data-ttu-id="c8652-132">Na stránce **Parametry pohledávek** (**Pohledávky** \> **Nastavení** \> **Parametry pohledávek**) na kartě **Vyrovnání** na pevné záložce **Možnosti** nastavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="c8652-132">On the **Accounts receivable parameters** page (**Accounts receivable** \> **Setup** \> **Accounts receivable parameters**), on **Settlement** tab, on the **Options** FastTab, set up the following parameters:</span></span>

-   <span data-ttu-id="c8652-133">Zaškrtněte políčko **Vyžadovat kódy důvodu pro dobropisy**.</span><span class="sxs-lookup"><span data-stu-id="c8652-133">Select the **Require reason codes for credit notes** check box.</span></span>

-   <span data-ttu-id="c8652-134">Zaškrtněte políčko **Zaúčtovat dobropis pro platební slevu**.</span><span class="sxs-lookup"><span data-stu-id="c8652-134">Select the **Post credit note for cash discount** check box.</span></span>

<span data-ttu-id="c8652-135">V poli **Kód důvodu pro platební slevy** vyberte výchozí kód důvodu pro opravné daňové doklady.</span><span class="sxs-lookup"><span data-stu-id="c8652-135">In the **Reason code for cash discounts** field, select a default reason code to use for tax corrective documents.</span></span>

## <a name="credit-notes-for-cash-discounts"></a><span data-ttu-id="c8652-136">Dobropisy pro platební slevy</span><span class="sxs-lookup"><span data-stu-id="c8652-136">Credit notes for cash discounts</span></span>

<span data-ttu-id="c8652-137">Dobropisy pro hotovostní slevy se automaticky zaúčtují při vyrovnání otevřených transakcí odběratele (faktury odběratele a platbu odběratele).</span><span class="sxs-lookup"><span data-stu-id="c8652-137">Credit notes for cash discounts are posted automatically when open customer transactions (customer invoice and customer payment) are settled.</span></span> <span data-ttu-id="c8652-138">Při zaúčtování dobropisů pro hotovostní slevy jsou zahrnuty kódy důvodů, které nastavíte v parametrech pohledávek, a odkaz na původní fakturu.</span><span class="sxs-lookup"><span data-stu-id="c8652-138">When credit notes for cash discounts are posted, they include the reason codes that you set up in Account receivable parameters, and a reference to the original invoice.</span></span>
<span data-ttu-id="c8652-139">Dobropisy pro platební slevy jsou číslovány podle číselné řady nastavené pro dobropisy.</span><span class="sxs-lookup"><span data-stu-id="c8652-139">Credit notes for cash discounts are numbered by using the number sequence that you set up for credit notes.</span></span> <span data-ttu-id="c8652-140">Výtisk dokumentu je nazván **Opravný dokument daně**.</span><span class="sxs-lookup"><span data-stu-id="c8652-140">The document printout is named **Tax corrective document**.</span></span> <span data-ttu-id="c8652-141">Obsahuje původní číslo faktury, základ a částku DPH a důvod, proč byla vytištěna oprava.</span><span class="sxs-lookup"><span data-stu-id="c8652-141">It includes the original invoice number, the VAT base and amount, and the reason why a correction was printed.</span></span>

