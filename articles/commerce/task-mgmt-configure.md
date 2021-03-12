---
title: Konfigurace správy úkolů
description: Tohle téma popisuje, jak konfigurovat funkce správy úkolů v aplikaci Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e880305d02fd9f10464fe3f65a2774a44da258c6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006228"
---
# <a name="configure-task-management"></a><span data-ttu-id="9ebfb-103">Konfigurace správy úkolů</span><span class="sxs-lookup"><span data-stu-id="9ebfb-103">Configure task management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9ebfb-104">Tohle téma popisuje, jak konfigurovat funkce správy úkolů v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-104">This topic describes how to configure task management features in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9ebfb-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="9ebfb-105">Overview</span></span>

<span data-ttu-id="9ebfb-106">Než budou moci manažeři a zaměstnanci používat funkce správy úkolů v Dynamics 365 Commerce, nejprve musí být nakonfigurována správa úkolů.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-106">Before Dynamics 365 Commerce managers and employees can use the task management features in Commerce, task management must be configured.</span></span> <span data-ttu-id="9ebfb-107">Konfigurace zahrnuje udělení oprávnění manažerům a zaměstnancům, distribuci oprávnění klientům v pokladním místě (POS), nastavení oznámení POS a konfiguraci dlaždice **Úkoly** na domovské stránce aplikace POS.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-107">Configuration steps include granting permissions to managers and employees, distributing permissions to point of sale (POS) clients, setting up POS notifications, and configuring the **Tasks** tile on the home page of a POS application.</span></span>

## <a name="configure-permissions-for-store-managers"></a><span data-ttu-id="9ebfb-108">Konfigurace oprávnění pro manažery obchodů</span><span class="sxs-lookup"><span data-stu-id="9ebfb-108">Configure permissions for store managers</span></span>

<span data-ttu-id="9ebfb-109">Každý pracovník v daném obchodě může zobrazit všechny úkoly, které jsou k tomuto obchodu přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-109">Every worker in a given store can view all tasks that are assigned to that store.</span></span> <span data-ttu-id="9ebfb-110">Může také aktualizovat stav úkolů, které jsou mu přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-110">They can also update the status of the tasks that are assigned to them.</span></span> <span data-ttu-id="9ebfb-111">Nicméně osoby jako manažeři obchodu musí mít oprávnění ke správě úkolů, aby mohli spravovat úkoly, které jsou přiřazeny k obchodu, a vytvářet jednoúčelové úkoly.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-111">However, personas such as store managers must have task management permissions to manage tasks that are assigned to the store and to create single-purpose tasks.</span></span>

<span data-ttu-id="9ebfb-112">Chcete-li nakonfigurovat oprávnění pro správu úkolů pro manažery obchodů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-112">To configure task management permissions for store managers, follow these steps.</span></span>

1. <span data-ttu-id="9ebfb-113">Přejděte na **Retail a Commerce \> Zaměstnanci \> Skupiny oprávnění**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-113">Go to **Retail and Commerce \> Employees \> Permission groups**.</span></span>
1. <span data-ttu-id="9ebfb-114">Vyberte určitou skupinu oprávnění ( například **Manažer**) a poté vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-114">Select a specific permission group (for example, **Manager**), and then select **Edit**.</span></span>
1. <span data-ttu-id="9ebfb-115">Na pevné záložce **Oprávnění** nastavte možnost **Povolit správu úkolů** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-115">On the **Permissions** FastTab, set the **Allow task management** option to **Yes**.</span></span>
1. <span data-ttu-id="9ebfb-116">Na pevné záložce **Oznámění** přidejte operaci **Správa úloh** a zadejte hodnotu do pole **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-116">On the **Notifications** FastTab, add the **Task management** operation, and enter a value in the **Display order** field.</span></span> <span data-ttu-id="9ebfb-117">Například zadejte **2**, pokud operace **Plnění objednávek** již má hodnotu **1** pro **Pořadí zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-117">For example, enter **2** if the **Order fulfillment** operation already has a **Display order** value of **1**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="9ebfb-118">Pokud uživatel, který není manažerem, musí mít v POS oprávnění ke správě úkolů, můžete dané osobě udělit oprávnění.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-118">If a non-manager persona must have task management permissions in the POS, you can grant permission to the individual.</span></span> <span data-ttu-id="9ebfb-119">Alternativně můžete vytvořit novou skupinu oprávnění pro nemanažery a nastavit možnost **Povolit správu úkolů** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-119">Alternatively, you can create a new permission group for non-managers and set the **Allow task management** option to **Yes**.</span></span>

<span data-ttu-id="9ebfb-120">Následující obrázek znázorňuje, jak nakonfigurovat oprávnění pro správu úkolů pro manažery obchodů.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-120">The following illustration shows how to configure task management permissions for store managers.</span></span>

![Konfigurace oprávnění pro správu úkolů pro manažery obchodů](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a><span data-ttu-id="9ebfb-122">Konfigurace oprávnění pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="9ebfb-122">Configure permissions for employees</span></span>

<span data-ttu-id="9ebfb-123">Zaměstnanci musí mít oprávnění k vytváření seznamů úkolů, ke správě kritérií přiřazení a ke konfiguraci opakování všech seznamů úkolů.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-123">Employees must have permissions to create task lists, manage assignment criteria, and configure the recurrence of any task list.</span></span> <span data-ttu-id="9ebfb-124">Chcete-li tato oprávnění konfigurovat, přiřaďte zaměstnance k roli **Manažer maloobchodních úkolů**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-124">To configure these permissions, you assign employees to the **Retail task manager** role.</span></span>

<span data-ttu-id="9ebfb-125">Chcete-li konfigurovat oprávnění pro zaměstnance, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-125">To configure permissions for an employee, follow these steps.</span></span>

1. <span data-ttu-id="9ebfb-126">Přejděte na **Retail a Commerce \> Zaměstnanci \> Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-126">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="9ebfb-127">Vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-127">Select an employee.</span></span>
1. <span data-ttu-id="9ebfb-128">Na pevné záložce **Role uživatele** vyberte možnost **Přiřadit role**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-128">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="9ebfb-129">V dialogovém okně **Přiřadit uživateli role** vyberte roli **Manažer maloobchodních úkolů** a pak tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-129">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

## <a name="distribute-permissions-to-pos-clients"></a><span data-ttu-id="9ebfb-130">Distribuce oprávnění klientům POS</span><span class="sxs-lookup"><span data-stu-id="9ebfb-130">Distribute permissions to POS clients</span></span>

<span data-ttu-id="9ebfb-131">Aby mohli zaměstnanci používat klienty POS, musí být oprávnění distribuována a synchronizována s těmito klienty.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-131">Before employees can use POS clients, permissions must be distributed and synced to those clients.</span></span>

<span data-ttu-id="9ebfb-132">Chcete-li oprávnění distribuovat klientům POS, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-132">To distribute permissions to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="9ebfb-133">Přejděte na **Retail and Commerce \> IT pro Retail and Commerce \> Plán distribuce**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-133">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="9ebfb-134">Vyberte plán distribuce **1060** (**Personál**) a poté vyberte možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-134">Select the **1060** (**Staff**) distribution schedule, and then select **Run now**.</span></span>
1. <span data-ttu-id="9ebfb-135">Vyberte plán distribuce **1070** (**Konfigurace kanálu**) a poté vyberte možnost **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-135">Select the **1070** (**Channel configuration**) distribution schedule, and then select **Run now**.</span></span>

## <a name="configure-pos-notifications-for-tasks"></a><span data-ttu-id="9ebfb-136">Konfigurace oznámení POS pro úkoly</span><span class="sxs-lookup"><span data-stu-id="9ebfb-136">Configure POS notifications for tasks</span></span>

<span data-ttu-id="9ebfb-137">Správa úkolů musí být nakonfigurována tak, aby v aplikaci POS byla k dispozici oznámení.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-137">Task management must be configured so that notifications are available in the POS application.</span></span>

<span data-ttu-id="9ebfb-138">Chcete-li konfigurovat oznámení POS pro úkoly, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-138">To configure POS notifications for tasks, follow these steps.</span></span>

1. <span data-ttu-id="9ebfb-139">Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Operace POS**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-139">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS operations**.</span></span>
1. <span data-ttu-id="9ebfb-140">Vyhledejte operaci **1400** (**Správa úkolů**) a zaškrtněte u ní políčko **Povolit oznámení**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-140">Find operation **1400** (**Task management**), and select the **Enable notifications** check box for it.</span></span>

<span data-ttu-id="9ebfb-141">Následující obrázek znázorňuje operaci **Správa úkolů** na stránce **Operace POS**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-141">The following illustration shows the **Task management** operation on the **POS operations** page.</span></span>

![Operace správy úkolů na stránce Operace POS](media/HQ-POS-Tasks-Notifications.png)

<span data-ttu-id="9ebfb-143">Další informace o konfiguraci oznámení POS naleznete v tématu [Zobrazení oznámení objednávek v pokladním místě (POS)](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="9ebfb-143">For more information about how to configure POS notifications, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a><span data-ttu-id="9ebfb-144">Konfigurace dlaždice Úkoly na domovské stránce aplikace POS</span><span class="sxs-lookup"><span data-stu-id="9ebfb-144">Configure the Tasks tile on a POS application home page</span></span>

<span data-ttu-id="9ebfb-145">Před konfigurací dlaždice **Úkoly** na domovské stránce aplikace POS si přečtěte téma [Rozložení obrazovky pokladního místa (POS)](pos-screen-layouts.md), které obsahuje informace o konfiguraci a přidání nových tlačítek do rozložení obrazovky POS.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-145">Before you configure the **Tasks** tile on the home page of a POS application, see [Screen layouts for the point of sale (POS)](pos-screen-layouts.md) for information about how to configure and add new buttons to a POS screen layout.</span></span>

<span data-ttu-id="9ebfb-146">Chcete-li konfigurovat dlaždici **Úkoly** na domovské stránce aplikace POS, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-146">To configure the **Tasks** tile on a POS application home page, follow these steps.</span></span>

1. <span data-ttu-id="9ebfb-147">Přejděte do nabídky **Retail a Commerce \> Instalace kanálu \> Nastavení POS \> POS \> Rozložení obrazovky**.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-147">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
1. <span data-ttu-id="9ebfb-148">Vyberte rozložení obrazovky, vyberte velikost rozvržení a vyberte mřížku tlačítek.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-148">Select a screen layout, select a layout size, and select a button grid.</span></span>
1. <span data-ttu-id="9ebfb-149">Na pevné záložce **Mřížky tlačítek** vyberte možnost **Návrhář**, chcete-li upravit vybranou mřížku tlačítek.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-149">On the **Button grids** FastTab, select **Designer** to edit the selected button grid.</span></span>
1. <span data-ttu-id="9ebfb-150">Přidejte dlaždici **Úkoly** do příslušné části domovské stránky.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-150">Add a **Tasks** tile to the appropriate section of the home page.</span></span>

<span data-ttu-id="9ebfb-151">Následující obrázek znázorňuje příklad dlaždice **Úkoly** na domovské stránce POS.</span><span class="sxs-lookup"><span data-stu-id="9ebfb-151">The following illustration shows an example of a **Tasks** tile on a POS home page.</span></span>

![Dlaždice Úkoly na domovské stránce POS](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a><span data-ttu-id="9ebfb-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9ebfb-153">Additional resources</span></span>

[<span data-ttu-id="9ebfb-154">Přehled správy úkolů</span><span class="sxs-lookup"><span data-stu-id="9ebfb-154">Task management overview</span></span>](task-mgmt-overview.md)

[<span data-ttu-id="9ebfb-155">Vytvoření seznamů úkolů a přidání úkolů</span><span class="sxs-lookup"><span data-stu-id="9ebfb-155">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="9ebfb-156">Přiřazení seznamů úkolů k obchodům nebo zaměstnancům</span><span class="sxs-lookup"><span data-stu-id="9ebfb-156">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="9ebfb-157">Správa úkolů v POS</span><span class="sxs-lookup"><span data-stu-id="9ebfb-157">Task management in POS</span></span>](task-mgmt-POS.md)
