---
title: Nastavení parametrů správy zaměstnaneckých výhod
description: Nakonfigurujte parametry pro správu zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229756"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="a88ef-103">Nastavení parametrů správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="a88ef-103">Set Benefits management parameters</span></span>

<span data-ttu-id="a88ef-104">Před nastavením plánů pracovního volna v Microsoft Dynamics 365 Human Resources musíte konfigurovat parametry správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="a88ef-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="a88ef-105">Tyto parametry nastaví výchozí hodnoty, kódy důvodů a další možnosti.</span><span class="sxs-lookup"><span data-stu-id="a88ef-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="a88ef-106">Konfigurace všeobecných parametrů</span><span class="sxs-lookup"><span data-stu-id="a88ef-106">Configure general parameters</span></span>

1. <span data-ttu-id="a88ef-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="a88ef-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="a88ef-108">Na kartě **Obecné** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="a88ef-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="a88ef-109">Pole</span><span class="sxs-lookup"><span data-stu-id="a88ef-109">Field</span></span> | <span data-ttu-id="a88ef-110">Popis</span><span class="sxs-lookup"><span data-stu-id="a88ef-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a88ef-111">**Země nebo oblast**</span><span class="sxs-lookup"><span data-stu-id="a88ef-111">**Country/region**</span></span> | <span data-ttu-id="a88ef-112">Pole **Země/oblast** určuje pořadí zobrazení PSČ / států.</span><span class="sxs-lookup"><span data-stu-id="a88ef-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="a88ef-113">Vybraná země se v rozevíracím seznamu zobrazí jako první.</span><span class="sxs-lookup"><span data-stu-id="a88ef-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="a88ef-114">**Kód důvodu registrace**</span><span class="sxs-lookup"><span data-stu-id="a88ef-114">**Enrollment reason code**</span></span> | <span data-ttu-id="a88ef-115">Vyberte výchozí kód důvodu, který má být použit při vytvoření plánů zaměstnanců při otevřeném zpracování registrace.</span><span class="sxs-lookup"><span data-stu-id="a88ef-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="a88ef-116">**Kód důvodu zrušení**</span><span class="sxs-lookup"><span data-stu-id="a88ef-116">**Cancellation reason code**</span></span> | <span data-ttu-id="a88ef-117">Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="a88ef-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="a88ef-118">V průběhu procesu stornování se zobrazí dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="a88ef-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="a88ef-119">Uživatelé jej mohou v případě potřeby změnit v okně **Kód důvodu zrušení**.</span><span class="sxs-lookup"><span data-stu-id="a88ef-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="a88ef-120">**Znovu otevřít kód důvodu**</span><span class="sxs-lookup"><span data-stu-id="a88ef-120">**Reopen reason code**</span></span> | <span data-ttu-id="a88ef-121">Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod, se znovu otevře.</span><span class="sxs-lookup"><span data-stu-id="a88ef-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="a88ef-122">V průběhu procesu stornování se zobrazí dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="a88ef-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="a88ef-123">Uživatelé jej mohou v případě potřeby změnit v okně **Znovu otevřít kód důvodu zrušení**.</span><span class="sxs-lookup"><span data-stu-id="a88ef-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="a88ef-124">**Kód důvodu životní události**</span><span class="sxs-lookup"><span data-stu-id="a88ef-124">**Life event reason code**</span></span> | <span data-ttu-id="a88ef-125">Kód důvodu, který má být použit při výskytu životní události.</span><span class="sxs-lookup"><span data-stu-id="a88ef-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="a88ef-126">**Kód důvodu změny sazby**</span><span class="sxs-lookup"><span data-stu-id="a88ef-126">**Rate change reason code**</span></span> | <span data-ttu-id="a88ef-127">Kód důvodu, který má být použit při zrušení a opětovném otevření plánu zaměstnaneckých výhod během procesu aktualizace změny sazby.</span><span class="sxs-lookup"><span data-stu-id="a88ef-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="a88ef-128">Informuje o tom, které záznamy byly změněny procesem aktualizace změny sazby.</span><span class="sxs-lookup"><span data-stu-id="a88ef-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="a88ef-129">**Nově přijatý zaměstnanec je způsobilý**</span><span class="sxs-lookup"><span data-stu-id="a88ef-129">**New hire eligible**</span></span> | <span data-ttu-id="a88ef-130">Určuje, zda mají nově přijatí zaměstnanci nárok na podporu.</span><span class="sxs-lookup"><span data-stu-id="a88ef-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="a88ef-131">**Období registrace nového zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="a88ef-131">**New hire enrollment period**</span></span> | <span data-ttu-id="a88ef-132">Časové období, kdy je povolena registrace nově přijatého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="a88ef-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="a88ef-133">**Poznámka**: Toto nastavení přepíše jakékoli období registrace nově přijatého zaměstnance, které je nastaveno pro pravidlo nároku na plán.</span><span class="sxs-lookup"><span data-stu-id="a88ef-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="a88ef-134">**Životní události povoleny**</span><span class="sxs-lookup"><span data-stu-id="a88ef-134">**Life events enabled**</span></span> | <span data-ttu-id="a88ef-135">Povolí životní události.</span><span class="sxs-lookup"><span data-stu-id="a88ef-135">Enables life events.</span></span> |
   | <span data-ttu-id="a88ef-136">**Skrýt staré formuláře zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="a88ef-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="a88ef-137">Umožňuje skrýt starší formuláře zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="a88ef-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="a88ef-138">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a88ef-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="a88ef-139">Konfigurace parametrů samoobsluhy zaměstnance</span><span class="sxs-lookup"><span data-stu-id="a88ef-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="a88ef-140">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="a88ef-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="a88ef-141">Na kartě **Samoobsluha zaměstnance** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="a88ef-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="a88ef-142">Pole</span><span class="sxs-lookup"><span data-stu-id="a88ef-142">Field</span></span> | <span data-ttu-id="a88ef-143">Popis</span><span class="sxs-lookup"><span data-stu-id="a88ef-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a88ef-144">**Ověření zaměstnanecké výhody**</span><span class="sxs-lookup"><span data-stu-id="a88ef-144">**Benefit verification**</span></span> | <span data-ttu-id="a88ef-145">Ověřovací text, který se má použít při rezervaci výhod samoobsluhy.</span><span class="sxs-lookup"><span data-stu-id="a88ef-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="a88ef-146">**Automatický výběr pověřených osob**</span><span class="sxs-lookup"><span data-stu-id="a88ef-146">**Auto select designees**</span></span> | <span data-ttu-id="a88ef-147">Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="a88ef-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="a88ef-148">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a88ef-148">Select **Save**.</span></span>
