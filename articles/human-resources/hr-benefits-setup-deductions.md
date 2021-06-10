---
title: Konfigurace srážek
description: Srážky v Microsoft Dynamics 365 Human Resources slouží k určení toho, jak často má být provedena srážka z výplaty zaměstnance u každé výhody.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055549"
---
# <a name="configure-deductions"></a><span data-ttu-id="2bbb7-103">Konfigurace srážek</span><span class="sxs-lookup"><span data-stu-id="2bbb7-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2bbb7-104">Srážky v Microsoft Dynamics 365 Human Resources slouží k určení toho, jak často má být provedena srážka z výplaty zaměstnance u každé výhody.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="2bbb7-105">Srážky jsou efektivní podle data, takže je možné uchovat historický záznam informací o srážce.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="2bbb7-106">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Srážky**.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="2bbb7-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-107">Select **New**.</span></span>

3. <span data-ttu-id="2bbb7-108">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="2bbb7-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="2bbb7-109">Pole</span><span class="sxs-lookup"><span data-stu-id="2bbb7-109">Field</span></span> | <span data-ttu-id="2bbb7-110">Popis</span><span class="sxs-lookup"><span data-stu-id="2bbb7-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2bbb7-111">**Odpočet**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-111">**Deduction**</span></span> | <span data-ttu-id="2bbb7-112">Jedinečné ID, které se používá k identifikaci srážky ze zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="2bbb7-113">**Popis**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-113">**Description**</span></span> | <span data-ttu-id="2bbb7-114">Popis srážky.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="2bbb7-115">**Účinné:**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-115">**Effective**</span></span> | <span data-ttu-id="2bbb7-116">Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-116">The start date.</span></span> <span data-ttu-id="2bbb7-117">Výchozí hodnotou je aktuální systémové datum.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="2bbb7-118">**Vypršení platnosti**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-118">**Expiration**</span></span> | <span data-ttu-id="2bbb7-119">Koncové datum.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-119">The end date.</span></span> <span data-ttu-id="2bbb7-120">Výchozí hodnota je 12/31/2154, což znamená nikdy.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="2bbb7-121">**Záhlaví**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-121">**Heading**</span></span> | <span data-ttu-id="2bbb7-122">Kód záhlaví ze systému mezd, který bude použit pro část srážky pro zaměstnance při zpracování zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="2bbb7-123">Používá se v případě, že používáte poskytovatele mezd od třetí strany.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="2bbb7-124">**Odkaz srážky ze mzdy zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="2bbb7-125">Kód srážky z mzdového systému, který tato srážka použije pro část zaměstnance srážky při zpracování zaměstnaneckých výhod do mzdy.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="2bbb7-126">**Záhlaví částky**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-126">**Amount heading**</span></span> | <span data-ttu-id="2bbb7-127">Kód záhlaví ze systému mezd, který bude použit pro část srážky pro zaměstnance při zpracování zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="2bbb7-128">Běžně se používá v případě, že používáte poskytovatele mezd od třetí strany.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="2bbb7-129">**Lze odstranit**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-129">**Can delete**</span></span> | <span data-ttu-id="2bbb7-130">Určuje, zda může exportovaná hodnota z Dynamics 365 for Finance and Operations způsobit odstranění hodnoty v systému mezd.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="2bbb7-131">**Spárované sloupce**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-131">**Paired columns**</span></span> | <span data-ttu-id="2bbb7-132">Určuje, zda má být exportována částka záhlaví a srážky ve spárováných sousedících sloupcích do mzdového systému.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="2bbb7-133">**Datum platnosti změny**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-133">**Change effective date**</span></span> | <span data-ttu-id="2bbb7-134">Datum, kdy změna srážky zaměstnanecké výhody vstoupí v platnost.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="2bbb7-135">K tomuto datu systém automaticky změní srážku zaměstnanecké výhody a aktualizuje všechny plány zaměstnaneckých výhod spojené s touto srážkou, pokud spustíte zpracování **Aktualizace změny srážky**.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="2bbb7-136">**Změna srážek dokončena**</span><span class="sxs-lookup"><span data-stu-id="2bbb7-136">**Deduction change completed**</span></span> | <span data-ttu-id="2bbb7-137">Jakmile budou dokončeny změny srážky v procesu aktualizace změny srážky, bude automaticky zaškrtnuto políčko **Změna srážky dokončena**.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="2bbb7-138">Chcete-li sledovat a spravovat změny v nastavení sazby zaměstnaneckých výhod, vyberte **Akce** a potom vyberte **Spravovat verze**.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="2bbb7-139">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2bbb7-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]