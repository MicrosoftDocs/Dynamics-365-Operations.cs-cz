---
title: Požadavky na údržbu
description: Toto téma obsahuje přehled správy požadavků na údržbu v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847429"
---
# <a name="maintenance-requests"></a><span data-ttu-id="8fd13-103">Požadavky na údržbu</span><span class="sxs-lookup"><span data-stu-id="8fd13-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8fd13-104">Požadavky na údržbu jsou poznámky nebo prohlášení, které jsou vytvořeny za účelem upozornění manažera nebo plánovače, že majetek může vyžadovat úlohu údržby nebo opravy, ale bez vytvoření pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="8fd13-105">Pokud je obsah požadavku na údržbu považován za platný, lze na základě požadavku na údržbu vytvořit pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="8fd13-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="8fd13-106">Požadavky na údržbu mohou být vytvořeny pro libovolný majetek v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="8fd13-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="8fd13-107">V závislosti na způsobu použití požadavků na údržbu vaší společností lze vytvářet různé typy požadavků na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="8fd13-108">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="8fd13-108">Here are some examples:</span></span>

- <span data-ttu-id="8fd13-109">Požadavky na údržbu</span><span class="sxs-lookup"><span data-stu-id="8fd13-109">Maintenance requests</span></span>
- <span data-ttu-id="8fd13-110">Poznámky</span><span class="sxs-lookup"><span data-stu-id="8fd13-110">Notes</span></span>
- <span data-ttu-id="8fd13-111">Opravy nebo vylepšení</span><span class="sxs-lookup"><span data-stu-id="8fd13-111">Corrections or enhancements</span></span>
- <span data-ttu-id="8fd13-112">Investice</span><span class="sxs-lookup"><span data-stu-id="8fd13-112">Investments</span></span>
- <span data-ttu-id="8fd13-113">Oprava skladu (Tento typ se používá, když obdržíte majetek z jiného místa, aby bylo možné provést úlohu údržby nebo opravy a poté majetek vrátit po dokončení úlohy.)</span><span class="sxs-lookup"><span data-stu-id="8fd13-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="8fd13-114">Zobrazení požadavků na údržbu</span><span class="sxs-lookup"><span data-stu-id="8fd13-114">View maintenance requests</span></span>

<span data-ttu-id="8fd13-115">Chcete-li zobrazit požadavky na údržbu, vyberte **Správa majetku** \> **Společné** \> **Požadavky na údržbu** \> **Všechny požadavky na údržbu**, **Aktivní požadavky na údržbu** nebo **Moje požadavky na údržbu funkčního místa**.</span><span class="sxs-lookup"><span data-stu-id="8fd13-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="8fd13-116">Na každé stránce se seznamem jsou uvedeny některé informace související s požadavkem na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Obrázek č. 1](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="8fd13-118">Použijte stránku se seznamem **Moje požadavky na údržbu funkčního místa** pro zobrazení seznamu požadavků na údržbu, které obsahují buď funkční místa, se kterými jste spojen jako pracovník, nebo majetek nainstalovaný ve funkčních místech, místěních, se kterým jste spojen jako pracovník</span><span class="sxs-lookup"><span data-stu-id="8fd13-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="8fd13-119">(Informace o tom, jak nastavit funkční místa nebo pracovníky údržby, naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="8fd13-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="8fd13-120">Ačkoli jsou informace o účtu odběratele k dispozici ve správě služby majetku (externí údržba), nejsou k dispozici ve správě majetku (interní údržba).</span><span class="sxs-lookup"><span data-stu-id="8fd13-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="8fd13-121">Chcete-li otevřít zobrazení podrobností záznamu, na stránce se seznamem **Všechny požadavky na údržbu** v zobrazení mřížky vyberte odkaz ve sloupci **Požadavek na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="8fd13-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Obrázek č. 2](media/02-manage-maintenance-requests.png)

<span data-ttu-id="8fd13-123">Tlačítka v podokně akcí jsou uspořádána na kartách.</span><span class="sxs-lookup"><span data-stu-id="8fd13-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="8fd13-124">Následující tabulka stručně popisuje tlačítka, která souvisejí se správou majetku.</span><span class="sxs-lookup"><span data-stu-id="8fd13-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="8fd13-125">Název tlačítka</span><span class="sxs-lookup"><span data-stu-id="8fd13-125">Button name</span></span>                      | <span data-ttu-id="8fd13-126">Popis</span><span class="sxs-lookup"><span data-stu-id="8fd13-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="8fd13-127">Úpravy</span><span class="sxs-lookup"><span data-stu-id="8fd13-127">Edit</span></span>                             | <span data-ttu-id="8fd13-128">Upravte vybraný požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-129">Nové</span><span class="sxs-lookup"><span data-stu-id="8fd13-129">New</span></span>                              | <span data-ttu-id="8fd13-130">Vytvořte nový požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="8fd13-131">Odstranit</span><span class="sxs-lookup"><span data-stu-id="8fd13-131">Delete</span></span>                           | <span data-ttu-id="8fd13-132">Odstraňte zvolený požadavek na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-133">Fond pracovních příkazů</span><span class="sxs-lookup"><span data-stu-id="8fd13-133">Work order pool</span></span>                  | <span data-ttu-id="8fd13-134">Připojte vybraný požadavek na údržbu k fondu pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="8fd13-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="8fd13-135">Pracovní příkaz</span><span class="sxs-lookup"><span data-stu-id="8fd13-135">Work order</span></span>                       | <span data-ttu-id="8fd13-136">Vytvořte pracovní příkaz na základě zvoleného požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-137">Závada majetku</span><span class="sxs-lookup"><span data-stu-id="8fd13-137">Asset fault</span></span>                      | <span data-ttu-id="8fd13-138">Klikněte na **Závada majetku**, kde můžete vytvořit registraci poruch na vybraném požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-139">Pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="8fd13-139">Work orders</span></span>                      | <span data-ttu-id="8fd13-140">Zobrazte seznam všech pracovních příkazů, které jsou připojeny k vybranému požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-141">Aktualizace stavu požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="8fd13-141">Update maintenance request state</span></span> | <span data-ttu-id="8fd13-142">Aktualizujte stav požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="8fd13-143">Protokol stavu životního cyklu</span><span class="sxs-lookup"><span data-stu-id="8fd13-143">Lifecycle state log</span></span>              | <span data-ttu-id="8fd13-144">Zobrazí protokol, který zobrazuje stavy životního cyklu vybraného požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-145">Podrobnosti požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="8fd13-145">Maintenance request details</span></span>      | <span data-ttu-id="8fd13-146">Vytiskněte sestavu, která zobrazuje podrobnosti vybraného požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-147">Odeslání zapůjčeného majetku</span><span class="sxs-lookup"><span data-stu-id="8fd13-147">Send loan asset</span></span>                  | <span data-ttu-id="8fd13-148">Vyberte zapůjčený majetek, který by měl být dočasnou náhradou majetku vybraného na zvoleném požadavku na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8fd13-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="8fd13-149">Vrácení vypůjčeného majetku</span><span class="sxs-lookup"><span data-stu-id="8fd13-149">Return loan asset</span></span>                | <span data-ttu-id="8fd13-150">Zaregistrujte zapůjčený majetek jako vrácený.</span><span class="sxs-lookup"><span data-stu-id="8fd13-150">Register the loan asset as returned.</span></span> |

