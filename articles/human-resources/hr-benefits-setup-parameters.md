---
title: Nastavení parametrů správy zaměstnaneckých výhod a samoobslužných parametrů zaměstnanců pro všechny společnosti
description: Konfigurace parametrů správy zaměstnaneckých výhod a samoobsluhy zaměstnanců v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "4962433"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="36f9f-103">Nastavení parametrů správy zaměstnaneckých výhod a samoobslužných parametrů zaměstnanců pro všechny společnosti</span><span class="sxs-lookup"><span data-stu-id="36f9f-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="36f9f-104">Před nastavením plánů zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources musíte konfigurovat parametry správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="36f9f-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="36f9f-105">Tyto parametry nastaví výchozí hodnoty, kódy důvodů a další možnosti.</span><span class="sxs-lookup"><span data-stu-id="36f9f-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="36f9f-106">Konfigurace všeobecných parametrů</span><span class="sxs-lookup"><span data-stu-id="36f9f-106">Configure general parameters</span></span>

1. <span data-ttu-id="36f9f-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Sdílené parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="36f9f-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="36f9f-108">Na kartě **Správa zaměstnaneckých výhod** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="36f9f-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="36f9f-109">Pole</span><span class="sxs-lookup"><span data-stu-id="36f9f-109">Field</span></span> | <span data-ttu-id="36f9f-110">popis</span><span class="sxs-lookup"><span data-stu-id="36f9f-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="36f9f-111">**Země nebo oblast**</span><span class="sxs-lookup"><span data-stu-id="36f9f-111">**Country/region**</span></span> | <span data-ttu-id="36f9f-112">Pole **Země/oblast** určuje pořadí zobrazení PSČ / států.</span><span class="sxs-lookup"><span data-stu-id="36f9f-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="36f9f-113">Vybraná země se v rozevíracím seznamu zobrazí jako první.</span><span class="sxs-lookup"><span data-stu-id="36f9f-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="36f9f-114">**Kód důvodu registrace**</span><span class="sxs-lookup"><span data-stu-id="36f9f-114">**Enrollment reason code**</span></span> | <span data-ttu-id="36f9f-115">Vyberte výchozí kód důvodu, který má být použit při vytvoření plánů zaměstnanců při otevřeném zpracování registrace.</span><span class="sxs-lookup"><span data-stu-id="36f9f-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="36f9f-116">**Kód důvodu zrušení**</span><span class="sxs-lookup"><span data-stu-id="36f9f-116">**Cancellation reason code**</span></span> | <span data-ttu-id="36f9f-117">Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="36f9f-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="36f9f-118">V průběhu procesu stornování se zobrazí dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="36f9f-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="36f9f-119">Uživatelé jej mohou v případě potřeby změnit v okně **Kód důvodu zrušení**.</span><span class="sxs-lookup"><span data-stu-id="36f9f-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="36f9f-120">**Znovu otevřít kód důvodu**</span><span class="sxs-lookup"><span data-stu-id="36f9f-120">**Reopen reason code**</span></span> | <span data-ttu-id="36f9f-121">Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod, se znovu otevře.</span><span class="sxs-lookup"><span data-stu-id="36f9f-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="36f9f-122">V průběhu procesu stornování se zobrazí dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="36f9f-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="36f9f-123">Uživatelé jej mohou v případě potřeby změnit v okně **Znovu otevřít kód důvodu zrušení**.</span><span class="sxs-lookup"><span data-stu-id="36f9f-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="36f9f-124">**Kód důvodu životní události**</span><span class="sxs-lookup"><span data-stu-id="36f9f-124">**Life event reason code**</span></span> | <span data-ttu-id="36f9f-125">Kód důvodu, který má být použit při výskytu životní události.</span><span class="sxs-lookup"><span data-stu-id="36f9f-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="36f9f-126">**Kód důvodu změny sazby**</span><span class="sxs-lookup"><span data-stu-id="36f9f-126">**Rate change reason code**</span></span> | <span data-ttu-id="36f9f-127">Kód důvodu, který má být použit při zrušení a opětovném otevření plánu zaměstnaneckých výhod během procesu aktualizace změny sazby.</span><span class="sxs-lookup"><span data-stu-id="36f9f-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="36f9f-128">Informuje o tom, které záznamy byly změněny procesem aktualizace změny sazby.</span><span class="sxs-lookup"><span data-stu-id="36f9f-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="36f9f-129">**Roční výplata zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="36f9f-129">**Benefits annual salary**</span></span> | <span data-ttu-id="36f9f-130">Umožňuje nastavit a částku **Roční výplata benefitů** pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="36f9f-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="36f9f-131">Human Resources budou využívat částku **Roční výplata benefitů** při určování částek krytí, namísto pevné roční náhrady.</span><span class="sxs-lookup"><span data-stu-id="36f9f-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="36f9f-132">**Nově přijatý zaměstnanec je způsobilý**</span><span class="sxs-lookup"><span data-stu-id="36f9f-132">**New hire eligible**</span></span> | <span data-ttu-id="36f9f-133">Určuje, zda mají nově přijatí zaměstnanci nárok na podporu.</span><span class="sxs-lookup"><span data-stu-id="36f9f-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="36f9f-134">**Období registrace nového zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="36f9f-134">**New hire enrollment period**</span></span> | <span data-ttu-id="36f9f-135">Časové období, kdy je povolena registrace nově přijatého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="36f9f-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="36f9f-136">**Poznámka**: Toto nastavení přepíše jakékoli období registrace nově přijatého zaměstnance, které je nastaveno pro pravidlo nároku na plán.</span><span class="sxs-lookup"><span data-stu-id="36f9f-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="36f9f-137">**Výchozí frekvence plateb**</span><span class="sxs-lookup"><span data-stu-id="36f9f-137">**Default pay frequency**</span></span> | <span data-ttu-id="36f9f-138">Výchozí frekvence výplaty, která se použije při přidávání nových pracovníků.</span><span class="sxs-lookup"><span data-stu-id="36f9f-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="36f9f-139">**Životní události povoleny**</span><span class="sxs-lookup"><span data-stu-id="36f9f-139">**Life events enabled**</span></span> | <span data-ttu-id="36f9f-140">Povolí životní události.</span><span class="sxs-lookup"><span data-stu-id="36f9f-140">Enables life events.</span></span> |
   | <span data-ttu-id="36f9f-141">**Skrýt staré formuláře zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="36f9f-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="36f9f-142">Umožňuje skrýt starší formuláře zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="36f9f-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="36f9f-143">**Ověření zaměstnanecké výhody**</span><span class="sxs-lookup"><span data-stu-id="36f9f-143">**Benefit verification**</span></span> | <span data-ttu-id="36f9f-144">Ověřovací text, který se má použít při rezervaci výhod samoobsluhy.</span><span class="sxs-lookup"><span data-stu-id="36f9f-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="36f9f-145">**Automatický výběr pověřených osob**</span><span class="sxs-lookup"><span data-stu-id="36f9f-145">**Auto select designees**</span></span> | <span data-ttu-id="36f9f-146">Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="36f9f-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="36f9f-147">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="36f9f-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="36f9f-148">Konfigurace parametrů samoobsluhy zaměstnance</span><span class="sxs-lookup"><span data-stu-id="36f9f-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="36f9f-149">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="36f9f-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="36f9f-150">Na kartě **Správa zaměstnaneckých výhod** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="36f9f-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="36f9f-151">Pole</span><span class="sxs-lookup"><span data-stu-id="36f9f-151">Field</span></span> | <span data-ttu-id="36f9f-152">popis</span><span class="sxs-lookup"><span data-stu-id="36f9f-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="36f9f-153">**Ověření zaměstnanecké výhody**</span><span class="sxs-lookup"><span data-stu-id="36f9f-153">**Benefit verification**</span></span> | <span data-ttu-id="36f9f-154">Ověřovací text, který se má použít při rezervaci výhod samoobsluhy.</span><span class="sxs-lookup"><span data-stu-id="36f9f-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="36f9f-155">**Automatický výběr pověřených osob**</span><span class="sxs-lookup"><span data-stu-id="36f9f-155">**Auto select designees**</span></span> | <span data-ttu-id="36f9f-156">Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="36f9f-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="36f9f-157">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="36f9f-157">Select **Save**.</span></span>


