---
title: Konfigurace srážek
description: Srážky v Microsoft Dynamics 365 Human Resources slouží k určení toho, jak často má být provedena srážka z výplaty zaměstnance u každé výhody.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c59fa09e83ca91e0ad866e5875ff06370b7491d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417549"
---
# <a name="configure-deductions"></a><span data-ttu-id="8dc64-103">Konfigurace srážek</span><span class="sxs-lookup"><span data-stu-id="8dc64-103">Configure deductions</span></span>

<span data-ttu-id="8dc64-104">Srážky v Microsoft Dynamics 365 Human Resources slouží k určení toho, jak často má být provedena srážka z výplaty zaměstnance u každé výhody.</span><span class="sxs-lookup"><span data-stu-id="8dc64-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="8dc64-105">Srážky jsou efektivní podle data, takže je možné uchovat historický záznam informací o srážce.</span><span class="sxs-lookup"><span data-stu-id="8dc64-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="8dc64-106">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Srážky**.</span><span class="sxs-lookup"><span data-stu-id="8dc64-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="8dc64-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8dc64-107">Select **New**.</span></span>

3. <span data-ttu-id="8dc64-108">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="8dc64-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="8dc64-109">Pole</span><span class="sxs-lookup"><span data-stu-id="8dc64-109">Field</span></span> | <span data-ttu-id="8dc64-110">Popis</span><span class="sxs-lookup"><span data-stu-id="8dc64-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="8dc64-111">**Odpočet**</span><span class="sxs-lookup"><span data-stu-id="8dc64-111">**Deduction**</span></span> | <span data-ttu-id="8dc64-112">Jedinečné ID, které se používá k identifikaci srážky ze zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="8dc64-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="8dc64-113">**Popis**</span><span class="sxs-lookup"><span data-stu-id="8dc64-113">**Description**</span></span> | <span data-ttu-id="8dc64-114">Popis srážky.</span><span class="sxs-lookup"><span data-stu-id="8dc64-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="8dc64-115">**Účinné:**</span><span class="sxs-lookup"><span data-stu-id="8dc64-115">**Effective**</span></span> | <span data-ttu-id="8dc64-116">Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="8dc64-116">The start date.</span></span> <span data-ttu-id="8dc64-117">Výchozí hodnotou je aktuální systémové datum.</span><span class="sxs-lookup"><span data-stu-id="8dc64-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="8dc64-118">**Vypršení platnosti**</span><span class="sxs-lookup"><span data-stu-id="8dc64-118">**Expiration**</span></span> | <span data-ttu-id="8dc64-119">Koncové datum.</span><span class="sxs-lookup"><span data-stu-id="8dc64-119">The end date.</span></span> <span data-ttu-id="8dc64-120">Výchozí hodnota je 12/31/2154, což znamená nikdy.</span><span class="sxs-lookup"><span data-stu-id="8dc64-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="8dc64-121">**Záhlaví**</span><span class="sxs-lookup"><span data-stu-id="8dc64-121">**Heading**</span></span> | <span data-ttu-id="8dc64-122">Kód záhlaví ze systému mezd, který bude použit pro část srážky pro zaměstnance při zpracování zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="8dc64-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="8dc64-123">Používá se v případě, že používáte poskytovatele mezd od třetí strany.</span><span class="sxs-lookup"><span data-stu-id="8dc64-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="8dc64-124">**Odkaz srážky ze mzdy zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="8dc64-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="8dc64-125">Kód srážky z mzdového systému, který tato srážka použije pro část zaměstnance srážky při zpracování zaměstnaneckých výhod do mzdy.</span><span class="sxs-lookup"><span data-stu-id="8dc64-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="8dc64-126">**Záhlaví částky**</span><span class="sxs-lookup"><span data-stu-id="8dc64-126">**Amount heading**</span></span> | <span data-ttu-id="8dc64-127">Kód záhlaví ze systému mezd, který bude použit pro část srážky pro zaměstnance při zpracování zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="8dc64-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="8dc64-128">Běžně se používá v případě, že používáte poskytovatele mezd od třetí strany.</span><span class="sxs-lookup"><span data-stu-id="8dc64-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="8dc64-129">**Lze odstranit**</span><span class="sxs-lookup"><span data-stu-id="8dc64-129">**Can delete**</span></span> | <span data-ttu-id="8dc64-130">Určuje, zda může exportovaná hodnota z Dynamics 365 for Finance and Operations způsobit odstranění hodnoty v systému mezd.</span><span class="sxs-lookup"><span data-stu-id="8dc64-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="8dc64-131">**Spárované sloupce**</span><span class="sxs-lookup"><span data-stu-id="8dc64-131">**Paired columns**</span></span> | <span data-ttu-id="8dc64-132">Určuje, zda má být exportována částka záhlaví a srážky ve spárováných sousedících sloupcích do mzdového systému.</span><span class="sxs-lookup"><span data-stu-id="8dc64-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="8dc64-133">**Datum platnosti změny**</span><span class="sxs-lookup"><span data-stu-id="8dc64-133">**Change effective date**</span></span> | <span data-ttu-id="8dc64-134">Datum, kdy změna srážky zaměstnanecké výhody vstoupí v platnost.</span><span class="sxs-lookup"><span data-stu-id="8dc64-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="8dc64-135">K tomuto datu systém automaticky změní srážku zaměstnanecké výhody a aktualizuje všechny plány zaměstnaneckých výhod spojené s touto srážkou, pokud spustíte zpracování **Aktualizace změny srážky**.</span><span class="sxs-lookup"><span data-stu-id="8dc64-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="8dc64-136">**Změna srážek dokončena**</span><span class="sxs-lookup"><span data-stu-id="8dc64-136">**Deduction change completed**</span></span> | <span data-ttu-id="8dc64-137">Jakmile budou dokončeny změny srážky v procesu aktualizace změny srážky, bude automaticky zaškrtnuto políčko **Změna srážky dokončena**.</span><span class="sxs-lookup"><span data-stu-id="8dc64-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="8dc64-138">Chcete-li sledovat a spravovat změny v nastavení sazby zaměstnaneckých výhod, vyberte **Akce** a potom vyberte **Spravovat verze**.</span><span class="sxs-lookup"><span data-stu-id="8dc64-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="8dc64-139">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8dc64-139">Select **Save**.</span></span> 
