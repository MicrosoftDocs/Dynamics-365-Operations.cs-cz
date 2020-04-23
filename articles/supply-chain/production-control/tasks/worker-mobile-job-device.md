---
title: Konfigurace pracovníka s použitím mobilního pracovního zařízení
description: Toto téma popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1086a88c341b95d6af03adc81c4e3e5d76adc69
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210196"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="496c1-103">Konfigurace pracovníka s použitím mobilního pracovního zařízení</span><span class="sxs-lookup"><span data-stu-id="496c1-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="496c1-104">Toto téma popisuje způsob přiřazení správných rolí uživatelskému účtu pracovníka a následného povolení pracovníkovi provádět registrace v dílenském řízení.</span><span class="sxs-lookup"><span data-stu-id="496c1-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="496c1-105">Ověření, zda je pracovníkovi přiřazena určitá role</span><span class="sxs-lookup"><span data-stu-id="496c1-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="496c1-106">V tomto příkladu ověřte, zda je uživateli "SHANNON" přiřazena role operátora stroje před konfigurací účtu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="496c1-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="496c1-107">Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="496c1-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="496c1-108">Vyhledejte uživatele v rychlém filtru.</span><span class="sxs-lookup"><span data-stu-id="496c1-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="496c1-109">V tomto příkladu zadejte `shannon`.</span><span class="sxs-lookup"><span data-stu-id="496c1-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="496c1-110">Vyberte odkaz ve sloupci **ID uživatele** uživatelského účtu, který se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="496c1-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="496c1-111">Ve stromovém zobrazení **Uživatelské role** vyberte **Role > Operátor stroje**.</span><span class="sxs-lookup"><span data-stu-id="496c1-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="496c1-112">Zavřete **Podrobnosti uživatele** a stránky **uživatelů** a vraťte se na domovskou stránku.</span><span class="sxs-lookup"><span data-stu-id="496c1-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="496c1-113">Nastavte konfiguraci účtu pracovníka</span><span class="sxs-lookup"><span data-stu-id="496c1-113">Configure worker account</span></span>
1. <span data-ttu-id="496c1-114">Přejděte na **Navigační podokno > Moduly > Lidské zdroje > Pracovníci > Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="496c1-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="496c1-115">Vyhledejte uživatele v rychlém filtru.</span><span class="sxs-lookup"><span data-stu-id="496c1-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="496c1-116">V tomto příkladu zadejte `shannon`.</span><span class="sxs-lookup"><span data-stu-id="496c1-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="496c1-117">Vyberte odkaz ve sloupci **Název** uživatelského účtu, který se zobrazí.</span><span class="sxs-lookup"><span data-stu-id="496c1-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="496c1-118">Vyberte záložku **Registrace času**.</span><span class="sxs-lookup"><span data-stu-id="496c1-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="496c1-119">Vyberte **Aktivovat na terminálech registrace**.</span><span class="sxs-lookup"><span data-stu-id="496c1-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="496c1-120">V následujících polích zadejte hodnoty:</span><span class="sxs-lookup"><span data-stu-id="496c1-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="496c1-121">**Skupina výpočtu**</span><span class="sxs-lookup"><span data-stu-id="496c1-121">**Calculation group**</span></span>  
    - <span data-ttu-id="496c1-122">**Výchozí skupina výpočtu**</span><span class="sxs-lookup"><span data-stu-id="496c1-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="496c1-123">**Skupina schválení**</span><span class="sxs-lookup"><span data-stu-id="496c1-123">**Approval group**</span></span>  
    - <span data-ttu-id="496c1-124">**Standardní profil**</span><span class="sxs-lookup"><span data-stu-id="496c1-124">**Standard profile**</span></span>  
    - <span data-ttu-id="496c1-125">**Skupina profilu**</span><span class="sxs-lookup"><span data-stu-id="496c1-125">**Profile group**</span></span>  

7. <span data-ttu-id="496c1-126">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="496c1-126">Select **OK**.</span></span>
8. <span data-ttu-id="496c1-127">Vyberte tlačítko **Upravit** zadejte číslo znaku pro novou registraci pracovníka.</span><span class="sxs-lookup"><span data-stu-id="496c1-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="496c1-128">V poli **ID znaku** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="496c1-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="496c1-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="496c1-129">Select **Save**.</span></span>
10. <span data-ttu-id="496c1-130">Zavřete stránky **Podrobnosti o pracovníkovi** a **Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="496c1-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="496c1-131">Přiřaďte pracovníka ke skupině zařízení</span><span class="sxs-lookup"><span data-stu-id="496c1-131">Assign worker to device group</span></span>
1. <span data-ttu-id="496c1-132">Přejděte do nabídky **Řízení výroby > Nastavení > Provádění výroby > Konfigurovat úkolový lístek pro zařízení**.</span><span class="sxs-lookup"><span data-stu-id="496c1-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="496c1-133">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="496c1-133">Select **Add**.</span></span>
3. <span data-ttu-id="496c1-134">Vyberte požadovaného pracovníka v seznamu.</span><span class="sxs-lookup"><span data-stu-id="496c1-134">In the list, select the desired worker.</span></span> <span data-ttu-id="496c1-135">V tomto příkladu vyberte **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="496c1-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="496c1-136">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="496c1-136">Select **OK**.</span></span>
5. <span data-ttu-id="496c1-137">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="496c1-137">Select **Edit**.</span></span>
6. <span data-ttu-id="496c1-138">V poli **Výrobní jednotka** lze nastavit výchozí filtr pro pracovníka.</span><span class="sxs-lookup"><span data-stu-id="496c1-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="496c1-139">Tím bude zajištěno, že pouze výrobní práce pro vybrané výrobní jednotky se zobrazí v případě, že se pracovník přihlásí k zařízení.</span><span class="sxs-lookup"><span data-stu-id="496c1-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="496c1-140">Zadejte požadovanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="496c1-140">Enter the desired value.</span></span>
7. <span data-ttu-id="496c1-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="496c1-141">Close the page.</span></span>

