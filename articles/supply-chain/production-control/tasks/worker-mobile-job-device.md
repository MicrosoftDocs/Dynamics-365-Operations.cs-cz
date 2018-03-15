--- 
title: "Konfigurace pracovníka s použitím mobilního pracovního zařízení"
description: "Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: cs-cz
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="0a4fc-103">Konfigurace pracovníka s použitím mobilního pracovního zařízení</span><span class="sxs-lookup"><span data-stu-id="0a4fc-103">Configure a worker using the mobile job device</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a4fc-104">Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="0a4fc-105">Přiřadit role uživatelskému účtu</span><span class="sxs-lookup"><span data-stu-id="0a4fc-105">Assign roles to user account</span></span>
1. <span data-ttu-id="0a4fc-106">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="0a4fc-107">Použití rychlého filtru umožňuje filtrovat jméno pracovníka, u kterého je uživatelský účet přidružen k roli operátor stroje.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="0a4fc-108">V ukázkových datech by toto jméno bylo Shannon.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="0a4fc-109">Vyberte záznam uživatelského účtu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="0a4fc-110">V seznamu klepněte na odkaz "Název" k zobrazení podrobností o uživatelském účtu na vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="0a4fc-111">Ve stromovém zobrazení vyberte „Role\Operátor stroje“.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="0a4fc-112">Zavřete stránku s podrobnostmi o uživatelském účtu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-112">Close the user account details page.</span></span>
7. <span data-ttu-id="0a4fc-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="0a4fc-114">Nastavte konfiguraci účtu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-114">Configure worker account.</span></span>
1. <span data-ttu-id="0a4fc-115">Přejděte k nabídce Lidské zdroje > Pracovníci > Pracovníci.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="0a4fc-116">Použití rychlého filtru umožňuje filtrovat jméno pracovníka, u kterého je uživatelský účet přidružen k roli operátor stroje.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="0a4fc-117">V ukázkových datech by toto jméno bylo Shannon.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="0a4fc-118">Vyberte záznam uživatelského účtu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="0a4fc-119">V seznamu klepněte na odkaz "Název" k zobrazení podrobností o uživatelském účtu na vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="0a4fc-120">Klikněte na kartu Zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="0a4fc-121">Rozbalte pevnou záložku Registrace času a klikněte na tlačítko Aktivovat na terminálech registrace.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="0a4fc-122">Klikněte na terminálech registrace na Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="0a4fc-123">V poli Skupina výpočtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="0a4fc-124">V poli Výchozí skupina výpočtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="0a4fc-125">V poli Skupina schválení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="0a4fc-126">V poli Standardní profil zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="0a4fc-127">V poli Skupina profilu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="0a4fc-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-128">Click OK.</span></span>
14. <span data-ttu-id="0a4fc-129">Kliknutím na tlačítko Upravit zadejte číslo znaku pro novou registraci pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="0a4fc-130">Zadejte hodnotu do pole ID znaku.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="0a4fc-131">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-131">Click Save.</span></span>
17. <span data-ttu-id="0a4fc-132">Použijte zástupce SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="0a4fc-133">Zavřete stránku s podrobnostmi o pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-133">Close the worker details page.</span></span>
19. <span data-ttu-id="0a4fc-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="0a4fc-135">Přiřaďte pracovníka ke skupině zařízení.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="0a4fc-136">Přejděte do nabídky Řízení výroby > Nastavení > Provádění výroby > Konfigurovat úkolový lístek pro zařízení.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="0a4fc-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-137">Click Add.</span></span>
3. <span data-ttu-id="0a4fc-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0a4fc-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-139">Click OK.</span></span>
5. <span data-ttu-id="0a4fc-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-140">Click Edit.</span></span>
6. <span data-ttu-id="0a4fc-141">V poli Výrobní jednotka lze nastavit výchozí filtr pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="0a4fc-142">Tím bude zajištěno, že pouze výrobní práce pro vybrané výrobní jednotky se zobrazí v případě, že se pracovník přihlásí k zařízení.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="0a4fc-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a4fc-143">Close the page.</span></span>

