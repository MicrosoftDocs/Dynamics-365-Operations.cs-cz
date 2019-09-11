---
title: Ručně vytvořené pracovní příkazy
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy ručně v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875545"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="8d19e-103">Ručně vytvořené pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="8d19e-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="8d19e-104">Pracovní příkazy lze vytvořit ručně dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="8d19e-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="8d19e-105">ve **Všech pracovních příkazech** nebo **Aktivních pracovních příkazech**</span><span class="sxs-lookup"><span data-stu-id="8d19e-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="8d19e-106">ve **Všech požadavcích na údržbu** nebo **Aktivních požadavcích na údržbu** nebo **Požadavcích na údržbu v mém funkčním místě**</span><span class="sxs-lookup"><span data-stu-id="8d19e-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="8d19e-107">Vytvořit pracovní příkaz</span><span class="sxs-lookup"><span data-stu-id="8d19e-107">Create work order</span></span>

1. <span data-ttu-id="8d19e-108">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8d19e-109">Klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-109">Click the **New** button.</span></span>

3. <span data-ttu-id="8d19e-110">V rozevíracím seznamu **Vytvořit pracovní příkaz** vyberte typ pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="8d19e-111">Pokud je to nutné, vyberte popis.</span><span class="sxs-lookup"><span data-stu-id="8d19e-111">If required, select a description.</span></span>

5. <span data-ttu-id="8d19e-112">Vyberte majetek pro pracovní příkaz a typ práce údržby.</span><span class="sxs-lookup"><span data-stu-id="8d19e-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="8d19e-113">Když vyberete majetek, jsou k dispozici tři karty: karta **Můj majetek** obsahuje majetek související s funkčními místy, do kterých můžete být přidělení (pracovník údržby, který je přihlášen k systému) (nastavení v [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="8d19e-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="8d19e-114">Nejsou-li u pracovníka údržby ve formuláři [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md) nastavena žádná funkční umístění, nebude karta **můj majetek** viditelná.</span><span class="sxs-lookup"><span data-stu-id="8d19e-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="8d19e-115">Karta **Aktivní majetek** obsahuje seznam všech datových zdrojů, které jsou aktivní pro stav životnosti majetku.</span><span class="sxs-lookup"><span data-stu-id="8d19e-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="8d19e-116">Karta **Zobrazení majetku** zobrazuje stromové zobrazení funkčních míst a datových zdrojů nainstalovaných v těchto umístěních.</span><span class="sxs-lookup"><span data-stu-id="8d19e-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="8d19e-117">V případě potřeby vyberte **Varianta typu práce údržby** a **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="8d19e-118">V případě potřeby lze úroveň služeb pracovního příkazu v poli **Úroveň služeb** změnit.</span><span class="sxs-lookup"><span data-stu-id="8d19e-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="8d19e-119">V souvisejících polích vyberte očekávaná počáteční a koncová data.</span><span class="sxs-lookup"><span data-stu-id="8d19e-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="8d19e-120">Klepnutím na **OK** vytvořte nový pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="8d19e-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="8d19e-121">Upravte pracovní příkaz ve **Všech pracovních příkazech**, je-li to vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="8d19e-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="8d19e-122">Ve **Všech pracovních příkazech** můžete přidat několik majetků do pracovního příkazu v zobrazení Podrobností přidáním řádků na pevné záložce **Práce údržby pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="8d19e-123">U majetku můžete vybrat pouze typy prací údržby, které jsou definovány v typu majetku vybraném pro daný majetek.</span><span class="sxs-lookup"><span data-stu-id="8d19e-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="8d19e-124">Pokud jste změnili úroveň služby Majetek nebo kritičnost majetku po jejich použití v pracovním příkazu (viz informace [Úrovně služby Majetek](../setup-for-objects/object-priorities.md) a [Kritičnosti majetku](../setup-for-objects/object-criticalities.md)), nebude se úroveň služeb nebo kritičnost v pracovním příkazu odpovídajícím způsobem aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="8d19e-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="8d19e-125">Kritičnost na pracovním příkazu je přepočítána pokaždé, když je v pracovním příkazu přidán nebo odstraněn řádek.</span><span class="sxs-lookup"><span data-stu-id="8d19e-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="8d19e-126">V zobrazení podrobností **Všechny pracovní příkazy** > zobrazení **Záhlaví** > pevné záložce **Plán** můžete vybrat skupinu odpovědného pracovníka údržby nebo odpovědného pracovníka údržby v poli **Odpovědná skupina** nebo **Odpovědný**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="8d19e-127">Toto nastavení lze změnit, pokud je pracovní příkaz aktivní, například při změně stavu životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="8d19e-128">Automatický výběr provedený při vytvoření pracovního příkazu je založen na nastavení v položce **Odpovědní pracovníci údržby**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="8d19e-129">Pokud přidáte nebo odeberete úlohy pracovní objednávky po vytvoření pracovní objednávky a pole **Odpovědná skupina** a pole **Odpovědný** jsou při aktualizaci pracovního příkazu prázdné, vyhledá Správa majetku možné párování ve formuláři nastavení pro skupinu odpovědných pracovníků údržby nebo odpovědného pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="8d19e-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="8d19e-130">Pokud je pole **Odpovědná skupina** nebo **Odpovědný** po aktualizaci pracovního příkazu vyplněno, nebudou provedeny žádné změny.</span><span class="sxs-lookup"><span data-stu-id="8d19e-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="8d19e-131">Ve **Stavu údržby** můžete provést výpočet pro získání přehledu pracovního vytížení, které se týkají příchozích a dokončených pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="8d19e-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="8d19e-132">Na pevné záložce **Podrobnosti řádku** použijte pole **Zeměpisná šířka** a **Zeměpisná délka** k přidání geografických souřadnic pro majetek vybraný na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="8d19e-133">Vytvořit související pracovní příkaz</span><span class="sxs-lookup"><span data-stu-id="8d19e-133">Create related work order</span></span>

<span data-ttu-id="8d19e-134">Související pracovní příkaz můžete vytvořit pro existující pracovní příkaz, pokud například chcete pracovat s primárními a sekundárními pracovními příkazy.</span><span class="sxs-lookup"><span data-stu-id="8d19e-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="8d19e-135">Nový pracovní příkaz je založen na úloze pracovního příkazu z existujícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="8d19e-136">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8d19e-137">Vyberte pracovní příkaz, pro který chcete vytvořit související pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="8d19e-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="8d19e-138">Klikněte na **Související pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="8d19e-139">V rozevíracím dialogovém okně **Vytvořit související pracovní příkaz** vyberte úlohu pracovního příkazu, pro kterou chcete vytvořit související pracovní příkaz v poli **Úloha pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="8d19e-140">Vyberte typ úlohy údržby v poli **Typ úlohy údržby** a v případě potřeby i související variantu typu úlohy údržby a obchod v polích **Varianta typu práce údržby** a **Oobchod**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="8d19e-141">Pokud se jedná o první související pracovní příkaz, klikněte na přepínač **Nový pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="8d19e-142">V souvisejících polích vyberte **Typ pracovního příkazu** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="8d19e-143">V případě potřeby změňte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="8d19e-144">Vložte očekávaná počáteční a koncová data v souvisejících polích.</span><span class="sxs-lookup"><span data-stu-id="8d19e-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="8d19e-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-145">Click **OK**.</span></span> <span data-ttu-id="8d19e-146">Nový související pracovní příkaz se zobrazí v seznamu **Všechny pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="8d19e-147">Pokud vytvoříte související pracovní příkaz na pracovním příkazu, který již obsahuje související pracovní příkazy, můžete úlohu pracovního příkazu přidat do již souvisejícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="8d19e-148">To lze provést kliknutím na přepínač **Přidat k souvisejícímu pracovnímu příkazu** v kroku 6.</span><span class="sxs-lookup"><span data-stu-id="8d19e-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="8d19e-149">Poté vyberte související pracovní příkaz, ke kterému chcete přidat novou úlohu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="8d19e-150">Podle potřeby upravte pole **Úroveň služeb**, **Očekávané zahájení** a **Očekávaný konec** a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="8d19e-151">Úloha pracovního příkazu se přidá do existujícího souvisejícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-151">The work order job is added to the existing related work order.</span></span>


![Obrázek č. 1](media/03-work-orders.png)

<span data-ttu-id="8d19e-153">**Poznámka:** Pokud jste nastavili související masku pracovního příkazu v **Parametry správy majetku** > **Pracovní příkazy** > **Související maska pracovního příkazu**, budou v souladu s nastavením masky vytvořeny ID pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="8d19e-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="8d19e-154">Není-li nastavena žádná související maska pracovního příkazu, bude pro související pracovní příkazy použito další dostupné ID pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="8d19e-155">Zkopírovat pracovní příkaz</span><span class="sxs-lookup"><span data-stu-id="8d19e-155">Copy work order</span></span>

<span data-ttu-id="8d19e-156">Nový pracovní příkaz lze rychle vytvořit z existujícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="8d19e-157">Tento postup práce s pracovními příkazy se liší od vytváření pracovních příkazů na základě plánů údržby.</span><span class="sxs-lookup"><span data-stu-id="8d19e-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="8d19e-158">To je užitečné například v případě, že máte pracovní příkaz obsahující mnoho úloh pracovního příkazu s různými úlohami v různých majetcích, které by měly být v pravidelných intervalech dokončeny.</span><span class="sxs-lookup"><span data-stu-id="8d19e-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="8d19e-159">Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="8d19e-160">Vyberte pracovní příkaz, ze kterého chcete kopírovat obsah.</span><span class="sxs-lookup"><span data-stu-id="8d19e-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="8d19e-161">Klikněte na **Kopírovat pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-161">Click **Copy work order**.</span></span> <span data-ttu-id="8d19e-162">Zobrazí se nastavení pracovního příkazu z vybraného pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="8d19e-163">V případě potřeby můžete některá pole upravit.</span><span class="sxs-lookup"><span data-stu-id="8d19e-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="8d19e-164">Klepnutím na **OK** vytvořte nový pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="8d19e-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="8d19e-165">Upravte pracovní příkaz ve **Všech pracovních příkazech**, je-li to vyžadováno.</span><span class="sxs-lookup"><span data-stu-id="8d19e-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="8d19e-166">Při vytvoření nového pracovního příkazu se některé informace zkopírují přímo z existujícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="8d19e-167">Informace týkající se prognóz, nástrojů, kontrolních seznamů údržby, funkčního umístění, adres a plánování nejsou zkopírovány, ale inicializovány z aktuálního nastavení v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="8d19e-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="8d19e-168">To znamená, že pokud byly změny provedeny v datech od vytvoření prvního pracovního příkazu až po dobu jeho kopie, budou tyto změny zahrnuty do nově vytvořeného pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="8d19e-169">Příkladem jsou změny v prognózách nebo aktualizované kontrolní seznamy údržby.</span><span class="sxs-lookup"><span data-stu-id="8d19e-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Obrázek č. 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="8d19e-171">Vytvoření pracovního příkazu na základě požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="8d19e-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="8d19e-172">Klikněte na **Správa majetku** > **Společné** > **Požadavky na údržbu** > **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="8d19e-173">Vyberte požadavek na údržbu, pro který chcete vytvořit pracovní příkaz, a klikněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="8d19e-174">Ve **Všech požadavcích** klikněte na **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="8d19e-175">Vyplňte rozevírací nabídku **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="8d19e-176">Pokud byl v požadavku na údržbu vybrán typ úlohy údržby, můžete v případě potřeby vybrat jiný typ úlohy údržby při vytvoření pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="8d19e-177">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-177">Click **OK**.</span></span> <span data-ttu-id="8d19e-178">Zobrazí se zpráva s informacemi o tom, že byl vytvořen daný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="8d19e-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="8d19e-179">Chcete-li zobrazit, které pracovní příkazy jsou spojeny s požadavkem na údržbu, vyberte požadavek na údržbu v seznamech **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** a klikněte na tlačítko **Pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="8d19e-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Obrázek č. 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="8d19e-181">Pracovní příkazy lze vytvářet také automaticky úlohami plánu údržby, nebo nastavením "automatického vytváření" plánů údržby nebo pořadí údržby majetku.</span><span class="sxs-lookup"><span data-stu-id="8d19e-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="8d19e-182">Pracovní příkazy vytvořené z požadavků na údržbu v **Rozvrhu údržby** jsou vytvořeny s typy úloh údržby vybranými v požadavcích na údržbu.</span><span class="sxs-lookup"><span data-stu-id="8d19e-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

