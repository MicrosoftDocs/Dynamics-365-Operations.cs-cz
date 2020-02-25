---
title: Nastavení parametrů správy zaměstnaneckých výhod
description: Nakonfigurujte parametry pro správu zaměstnaneckých výhod v Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008363"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="4c4dd-103">Nastavení parametrů správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="4c4dd-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="4c4dd-104">Před nastavením plánů pracovního volna v Microsoft Dynamics 365 Human Resources je nutné konfigurovat parametry správy zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="4c4dd-105">Tyto parametry nastaví výchozí hodnoty, kódy důvodů a další možnosti.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="4c4dd-106">Konfigurace všeobecných parametrů</span><span class="sxs-lookup"><span data-stu-id="4c4dd-106">Configure general parameters</span></span>

1. <span data-ttu-id="4c4dd-107">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="4c4dd-108">Na kartě **Obecné** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="4c4dd-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="4c4dd-109">Pole</span><span class="sxs-lookup"><span data-stu-id="4c4dd-109">Field</span></span> | <span data-ttu-id="4c4dd-110">Popis</span><span class="sxs-lookup"><span data-stu-id="4c4dd-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4c4dd-111">**Země nebo oblast**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-111">**Country/region**</span></span> | <span data-ttu-id="4c4dd-112">Pole **Země/oblast** určuje pořadí zobrazení PSČ / států.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="4c4dd-113">Vybraná země se v rozevíracím seznamu zobrazí jako první.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="4c4dd-114">**Kód důvodu registrace**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-114">**Enrollment reason code**</span></span> | <span data-ttu-id="4c4dd-115">Vyberte výchozí kód důvodu, který má být použit při vytvoření plánů zaměstnanců při otevřeném zpracování registrace.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="4c4dd-116">**Kód důvodu zrušení**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-116">**Cancellation reason code**</span></span> | <span data-ttu-id="4c4dd-117">Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="4c4dd-118">V průběhu procesu stornování se zobrazí dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="4c4dd-119">Uživatelé jej mohou v případě potřeby změnit v okně **Kód důvodu zrušení**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="4c4dd-120">**Znovu otevřít kód důvodu**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-120">**Reopen reason code**</span></span> | <span data-ttu-id="4c4dd-121">Kód důvodu, který má být použit při zrušení plánu zaměstnaneckých výhod, se znovu otevře.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="4c4dd-122">V průběhu procesu stornování se zobrazí dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="4c4dd-123">Uživatelé jej mohou v případě potřeby změnit v okně **Znovu otevřít kód důvodu zrušení**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="4c4dd-124">**Kód důvodu životní události**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-124">**Life event reason code**</span></span> | <span data-ttu-id="4c4dd-125">Kód důvodu, který má být použit při výskytu životní události.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="4c4dd-126">**Kód důvodu změny sazby**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-126">**Rate change reason code**</span></span> | <span data-ttu-id="4c4dd-127">Kód důvodu, který má být použit při zrušení a opětovném otevření plánu zaměstnaneckých výhod během procesu aktualizace změny sazby.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="4c4dd-128">Informuje o tom, které záznamy byly změněny procesem aktualizace změny sazby.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="4c4dd-129">**Nově přijatý zaměstnanec je způsobilý**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-129">**New hire eligible**</span></span> | <span data-ttu-id="4c4dd-130">Určuje, zda mají nově přijatí zaměstnanci nárok na podporu.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="4c4dd-131">**Období registrace nového zaměstnance**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-131">**New hire enrollment period**</span></span> | <span data-ttu-id="4c4dd-132">Časové období, kdy je povolena registrace nově přijatého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="4c4dd-133">**Poznámka**: Toto nastavení přepíše jakékoli období registrace nově přijatého zaměstnance, které je nastaveno pro pravidlo nároku na plán.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="4c4dd-134">**Rozšíření roční výplaty**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="4c4dd-135">Určuje, zda má být automaticky vypočtena částka **Roční výplaty zaměstnaneckých výhod** v poli **Podrobnosti o zaměstnanecké výhodě**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="4c4dd-136">Je založena na **fixní sazbě kompenzace** zaměstnance, **průměrné pracovní době** a **frekvenci plateb**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="4c4dd-137">**Průměrný počet hodin** x **Fixní sazba platby** x **Frekvence plateb** (počet platebních období) = **Roční výplata zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="4c4dd-138">Pokud se změní některá z hodnot v poli **Průměrný počet hodin**, **Fixní sazba platby kompenzace** nebo **Frekvence plateb**, systém automaticky přepočítá částku **roční výplaty zaměstnaneckých výhod** na základě změněných hodnot.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="4c4dd-139">Systém vytvoří záznam o **datu platnosti**, který určí přesné datum a čas, kdy došlo ke změně.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="4c4dd-140">V případě potřeby můžete v případě potřeby ručně upravit **roční výplatu zaměstnanecké výhody**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="4c4dd-141">**Životní události povoleny**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-141">**Life events enabled**</span></span> | <span data-ttu-id="4c4dd-142">Povolí životní události.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-142">Enables life events.</span></span> |
   | <span data-ttu-id="4c4dd-143">**Skrýt staré formuláře zaměstnaneckých výhod**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="4c4dd-144">Umožňuje skrýt starší formuláře zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="4c4dd-145">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="4c4dd-146">Konfigurace parametrů samoobsluhy zaměstnance</span><span class="sxs-lookup"><span data-stu-id="4c4dd-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="4c4dd-147">V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="4c4dd-148">Na kartě **Samoobsluha zaměstnance** zadejte hodnoty pro následující pole:</span><span class="sxs-lookup"><span data-stu-id="4c4dd-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="4c4dd-149">Pole</span><span class="sxs-lookup"><span data-stu-id="4c4dd-149">Field</span></span> | <span data-ttu-id="4c4dd-150">Popis</span><span class="sxs-lookup"><span data-stu-id="4c4dd-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="4c4dd-151">**Ověření zaměstnanecké výhody**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-151">**Benefit verification**</span></span> | <span data-ttu-id="4c4dd-152">Ověřovací text, který se má použít při rezervaci výhod samoobsluhy.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="4c4dd-153">**Automatický výběr pověřených osob**</span><span class="sxs-lookup"><span data-stu-id="4c4dd-153">**Auto select designees**</span></span> | <span data-ttu-id="4c4dd-154">Určuje, zda mají být automaticky zvoleni následníci a příjemci na základě jejich nároku na možnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="4c4dd-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4c4dd-155">Select **Save**.</span></span>
