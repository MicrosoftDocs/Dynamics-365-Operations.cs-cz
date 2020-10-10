---
title: Rozvrh údržby
description: Tohle téma popisuje rozvrh údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 351e088ece0512fee1bb5f9dad020f32f7728fe4
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888994"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="4f293-103">Rozvrh údržby</span><span class="sxs-lookup"><span data-stu-id="4f293-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4f293-104">Rozvrh údržby obsahuje seznam všech očekávaných plánů preventivní údržby, požadavků na údržbu a pořadí údržby, které mají být provedeny. Některé řádky rozvrhu mohly být převedeny na pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="4f293-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="4f293-105">Čtyři zobrazení rozvrhu údržby se mírně liší v závislosti na řádcích rozvrhu údržby, které chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="4f293-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="4f293-106">Položka nabídky</span><span class="sxs-lookup"><span data-stu-id="4f293-106">Menu item</span></span>                  | <span data-ttu-id="4f293-107">Popis obsahu</span><span class="sxs-lookup"><span data-stu-id="4f293-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f293-108">Rozvrh kompletní údržby</span><span class="sxs-lookup"><span data-stu-id="4f293-108">All maintenance schedule</span></span>       | <span data-ttu-id="4f293-109">Zobrazí se všechny řádky rozvrhu údržby.</span><span class="sxs-lookup"><span data-stu-id="4f293-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="4f293-110">Můj plán majetku</span><span class="sxs-lookup"><span data-stu-id="4f293-110">My asset schedule</span></span>        | <span data-ttu-id="4f293-111">V tomto seznamu jsou uvedeny všechny řádky rozvrhu údržby obsahující majetek instalovaný ve funkčních místech, ke kterému se vztahujete coby pracovník (nastavení v části [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="4f293-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="4f293-112">Otevřít řádky rozvrhu údržby</span><span class="sxs-lookup"><span data-stu-id="4f293-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="4f293-113">Řádky rozvrhu údržby se stavem „Vytvořeno“ jsou zobrazeny v tomto seznamu, což znamená, že dosud nebyly převedeny na pracovní příkaz, nebo byly zrušeny.</span><span class="sxs-lookup"><span data-stu-id="4f293-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="4f293-114">Otevřít skupiny rozvrhu údržby</span><span class="sxs-lookup"><span data-stu-id="4f293-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="4f293-115">V tomto seznamu jsou uvedeny řádky rozvrhu údržby související s fondem pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="4f293-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="4f293-116">Pokud je v několika fondech pracovních příkazů uveden řádek rozvrhu údržby (viz [Fondy pracovních příkazů](../work-orders/work-order-pools.md)), zobrazí se jeden záznam pro každý fond v části **Otevřené fondy rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="4f293-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="4f293-117">To je provedeno za účelem optimalizace možností filtrování ve fondech pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="4f293-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="4f293-118">Otevření rozvrhu údržby:</span><span class="sxs-lookup"><span data-stu-id="4f293-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="4f293-119">Klikněte na položky v částech **Správa majetku** > **Společné** > **Rozvrh údržby** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby** nebo **Otevřené fondy rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="4f293-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="4f293-120">Chcete-li aktualizovat rozvrh údržby, klikněte na možnost **Plán údržby** nebo **Pořadí údržby**.</span><span class="sxs-lookup"><span data-stu-id="4f293-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="4f293-121">Řádek rozvrhu údržby můžete upravit tak, že jej vyberete a kliknete na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="4f293-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="4f293-122">Můžete například snadno aktualizovat úroveň služeb nebo pracovníka odpovědného za práci.</span><span class="sxs-lookup"><span data-stu-id="4f293-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="4f293-123">Upravit lze pouze řádky rozvrhu údržby, které ještě nebyly připojeny k pracovnímu příkazu.</span><span class="sxs-lookup"><span data-stu-id="4f293-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="4f293-124">Řádek rozvrhu údržby můžete odstranit tak, že jej vyberete na stránce seznamu a kliknete na tlačítko **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="4f293-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="4f293-125">Řádek rozvrhu údržby můžete zahodit tak, že jej vyberete na stránce seznamu a kliknete na tlačítko **Zahodit**.</span><span class="sxs-lookup"><span data-stu-id="4f293-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="4f293-126">Tato funkce je užitečná, pokud má například majetek jeden plán údržby 2 000 km a druhý plán údržby 10 000 km.</span><span class="sxs-lookup"><span data-stu-id="4f293-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="4f293-127">Poté může být vhodné zahodit řádek vytvořený z plánu údržby 2 000 km, pokud se shoduje s 10 000 km, 20 000 km, 30 000 km atd.</span><span class="sxs-lookup"><span data-stu-id="4f293-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="4f293-128">Pokud zahodíte řádek rozvrhu údržby související s plánem údržby, tento řádek se po naplánování plánu údržby již nikdy nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="4f293-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="4f293-129">Chcete-li, aby byly všechny vybrané řádky zahrnuty do stejného fondu pracovních příkazů , můžete vybrat počet řádků rozvrhu údržby v části **Všechny rozvrhy údržby** a kliknout na položku **Fond pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="4f293-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="4f293-130">Můžete vybrat počet řádků rozvrhu údržby v části **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvhu** údržby nebo **Otevřené fondy rozvrhu údržby** a kliknout na **Upravit plán**, chcete-li provést stejné úpravy na několika řádcích.</span><span class="sxs-lookup"><span data-stu-id="4f293-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="4f293-131">Můžete změnit očekávaná počáteční a koncová data, úroveň služeb a skupinu zodpovědných pracovníků údržby nebo zodpovědného pracovníka údržby související s vybranými řádky rozvrhu údržby.</span><span class="sxs-lookup"><span data-stu-id="4f293-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="4f293-132">Pokud řádek rozvrhu údržby souvisí s pracovním příkazem, v poli **Pracovní příkaz** se zobrazí ID pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="4f293-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="4f293-133">V zobrazení podrobností **Všechen majetek** > na záložce s náhledem **Plány údržby majetku** můžete vybrat plány údržby pro majetek.</span><span class="sxs-lookup"><span data-stu-id="4f293-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="4f293-134">Později, pokud odstraníte řádek plánu údržby související s majetkem v části **Všechen majetek**, automaticky odstraníte také všechny řádky rozvrhu údržby se stavem „Vytvořeno“, které byly vytvořeny na základě plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="4f293-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="4f293-135">Viz také [Vytvoření majetku](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="4f293-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="4f293-136">Na následujícím obrázku je uvedena stránka seznamu **Všechny rozvrhy údržby**.</span><span class="sxs-lookup"><span data-stu-id="4f293-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Obrázek č. 1](media/16-preventive-maintenance.png)

