---
title: Konfigurace pracovníka s použitím mobilního pracovního zařízení
description: Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "327382"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="335ba-103">Konfigurace pracovníka s použitím mobilního pracovního zařízení</span><span class="sxs-lookup"><span data-stu-id="335ba-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="335ba-104">Tento postup popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.</span><span class="sxs-lookup"><span data-stu-id="335ba-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="335ba-105">Přiřadit role uživatelskému účtu</span><span class="sxs-lookup"><span data-stu-id="335ba-105">Assign roles to user account</span></span>
1. <span data-ttu-id="335ba-106">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="335ba-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="335ba-107">Použití rychlého filtru umožňuje filtrovat jméno pracovníka, u kterého je uživatelský účet přidružen k roli operátor stroje.</span><span class="sxs-lookup"><span data-stu-id="335ba-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="335ba-108">V ukázkových datech by toto jméno bylo Shannon.</span><span class="sxs-lookup"><span data-stu-id="335ba-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="335ba-109">Vyberte záznam uživatelského účtu.</span><span class="sxs-lookup"><span data-stu-id="335ba-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="335ba-110">V seznamu klepněte na odkaz "Název" k zobrazení podrobností o uživatelském účtu na vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="335ba-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="335ba-111">Ve stromovém zobrazení vyberte „Role\Operátor stroje“.</span><span class="sxs-lookup"><span data-stu-id="335ba-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="335ba-112">Zavřete stránku s podrobnostmi o uživatelském účtu.</span><span class="sxs-lookup"><span data-stu-id="335ba-112">Close the user account details page.</span></span>
7. <span data-ttu-id="335ba-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="335ba-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="335ba-114">Nastavte konfiguraci účtu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="335ba-114">Configure worker account.</span></span>
1. <span data-ttu-id="335ba-115">Přejděte k nabídce Lidské zdroje > Pracovníci > Pracovníci.</span><span class="sxs-lookup"><span data-stu-id="335ba-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="335ba-116">Použití rychlého filtru umožňuje filtrovat jméno pracovníka, u kterého je uživatelský účet přidružen k roli operátor stroje.</span><span class="sxs-lookup"><span data-stu-id="335ba-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="335ba-117">V ukázkových datech by toto jméno bylo Shannon.</span><span class="sxs-lookup"><span data-stu-id="335ba-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="335ba-118">Vyberte záznam uživatelského účtu.</span><span class="sxs-lookup"><span data-stu-id="335ba-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="335ba-119">V seznamu klepněte na odkaz "Název" k zobrazení podrobností o uživatelském účtu na vybraném řádku.</span><span class="sxs-lookup"><span data-stu-id="335ba-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="335ba-120">Klikněte na kartu Zaměstnání.</span><span class="sxs-lookup"><span data-stu-id="335ba-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="335ba-121">Rozbalte pevnou záložku Registrace času a klikněte na tlačítko Aktivovat na terminálech registrace.</span><span class="sxs-lookup"><span data-stu-id="335ba-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="335ba-122">Klikněte na terminálech registrace na Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="335ba-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="335ba-123">V poli Skupina výpočtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="335ba-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="335ba-124">V poli Výchozí skupina výpočtu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="335ba-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="335ba-125">V poli Skupina schválení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="335ba-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="335ba-126">V poli Standardní profil zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="335ba-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="335ba-127">V poli Skupina profilu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="335ba-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="335ba-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="335ba-128">Click OK.</span></span>
14. <span data-ttu-id="335ba-129">Kliknutím na tlačítko Upravit zadejte číslo znaku pro novou registraci pracovníka.</span><span class="sxs-lookup"><span data-stu-id="335ba-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="335ba-130">Zadejte hodnotu do pole ID znaku.</span><span class="sxs-lookup"><span data-stu-id="335ba-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="335ba-131">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="335ba-131">Click Save.</span></span>
17. <span data-ttu-id="335ba-132">Použijte zástupce SaveRecord.</span><span class="sxs-lookup"><span data-stu-id="335ba-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="335ba-133">Zavřete stránku s podrobnostmi o pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="335ba-133">Close the worker details page.</span></span>
19. <span data-ttu-id="335ba-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="335ba-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="335ba-135">Přiřaďte pracovníka ke skupině zařízení.</span><span class="sxs-lookup"><span data-stu-id="335ba-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="335ba-136">Přejděte do nabídky Řízení výroby > Nastavení > Provádění výroby > Konfigurovat úkolový lístek pro zařízení.</span><span class="sxs-lookup"><span data-stu-id="335ba-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="335ba-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="335ba-137">Click Add.</span></span>
3. <span data-ttu-id="335ba-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="335ba-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="335ba-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="335ba-139">Click OK.</span></span>
5. <span data-ttu-id="335ba-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="335ba-140">Click Edit.</span></span>
6. <span data-ttu-id="335ba-141">V poli Výrobní jednotka lze nastavit výchozí filtr pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="335ba-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="335ba-142">Tím bude zajištěno, že pouze výrobní práce pro vybrané výrobní jednotky se zobrazí v případě, že se pracovník přihlásí k zařízení.</span><span class="sxs-lookup"><span data-stu-id="335ba-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="335ba-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="335ba-143">Close the page.</span></span>

