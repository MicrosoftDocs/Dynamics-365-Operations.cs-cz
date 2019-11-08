---
title: Ručně vytvořené pracovní příkazy
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy ručně v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a8494bdefcf11dc331be18bfe02e0df1e39d602
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626240"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="9471b-103">Ručně vytvořené pracovní příkazy</span><span class="sxs-lookup"><span data-stu-id="9471b-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="9471b-104">Pracovní příkazy lze vytvořit ručně dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="9471b-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="9471b-105">Na stránce **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**</span><span class="sxs-lookup"><span data-stu-id="9471b-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="9471b-106">Ze stránky **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** nebo **Požadavky na údržbu v mém funkčním místě**.</span><span class="sxs-lookup"><span data-stu-id="9471b-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="9471b-107">Vytvořit pracovní příkaz</span><span class="sxs-lookup"><span data-stu-id="9471b-107">Create work order</span></span>

1. <span data-ttu-id="9471b-108">Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="9471b-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9471b-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9471b-109">Select **New**.</span></span>

3. <span data-ttu-id="9471b-110">V dialogovém okně **Vytvořit pracovní příkaz** vyberte typ pracovního příkazu v poli **Typ pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="9471b-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="9471b-111">Pokud je to nutné, vyberte **popis**.</span><span class="sxs-lookup"><span data-stu-id="9471b-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="9471b-112">V poli **Majetek** vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="9471b-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="9471b-113">Vyberete-li majetek, mohou být v rozevíracím seznamu **Majetek** k dispozici tři karty:</span><span class="sxs-lookup"><span data-stu-id="9471b-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="9471b-114">**Aktivní majetek** - obsahuje seznam všech datových zdrojů, které jsou aktivní pro stav životnosti majetku.</span><span class="sxs-lookup"><span data-stu-id="9471b-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="9471b-115">**Zobrazení majetku** - zobrazuje stromové zobrazení funkčních míst a datových zdrojů nainstalovaných v těchto umístěních.</span><span class="sxs-lookup"><span data-stu-id="9471b-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="9471b-116">**Můj majetek** – Tato karta obsahuje majetek související s funkčními místy, ke kterým může být přiřazen (pracovník, který je přihlášený do systému).</span><span class="sxs-lookup"><span data-stu-id="9471b-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="9471b-117">(Informace o nastavení naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).) Pokud pro pracovníka nejsou nastavena žádná funkční místa v části [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md), karta **Můj majetek** není dostupná.</span><span class="sxs-lookup"><span data-stu-id="9471b-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="9471b-118">V poli **Typ práce údržby** vyberte typ práce údržby pro pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="9471b-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="9471b-119">V případě potřeby vyberte **Varianta typu práce údržby** a **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="9471b-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="9471b-120">V případě potřeby lze úroveň služeb pracovního příkazu v poli **Úroveň služeb** změnit.</span><span class="sxs-lookup"><span data-stu-id="9471b-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="9471b-121">V příslušných polích vyberte **Očekávané počáteční** a **očekávané koncové** datum.</span><span class="sxs-lookup"><span data-stu-id="9471b-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="9471b-122">Kliknutím na **OK** vytvořte pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="9471b-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="9471b-123">Na stránce se seznamem **Všechny pracovní příkazy** můžete podle potřeby upravit požadovaný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="9471b-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="9471b-124">Mějte na paměti následující body:</span><span class="sxs-lookup"><span data-stu-id="9471b-124">Note the following points:</span></span>

- <span data-ttu-id="9471b-125">V podrobném zobrazení na stránce **Všechny pracovní příkazy** můžete přidat několik majetků do pracovního příkazu v zobrazení Podrobností přidáním řádků na pevné záložce **Práce údržby pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="9471b-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="9471b-126">U majetku můžete vybrat pouze typy prací údržby, které jsou definovány v typu majetku vybraném pro daný majetek.</span><span class="sxs-lookup"><span data-stu-id="9471b-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="9471b-127">Změníte-li v tomto nastavení kritičnost majetku poté, co jste jej již použili v pracovním příkazu, nebude tato servisní úroveň kritičnost v pracovním příkazu odpovídajícím způsobem aktualizována.</span><span class="sxs-lookup"><span data-stu-id="9471b-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="9471b-128">Další informace o úrovních servisu a závažností naleznete v tématu [Úrovně servisu majetku](../setup-for-objects/object-priorities.md) a [Závažnosti majetku](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="9471b-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="9471b-129">Závažnost v pracovním příkazu je přepočítána pokaždé, když je v pracovním příkazu přidán nebo odstraněn řádek.</span><span class="sxs-lookup"><span data-stu-id="9471b-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="9471b-130">V podrobném zobrazení **Všechny pracovní příkazy** > karta **Záhlaví** > pevná záložka **Plán** ve skupině **Zodpovědná osoba** nebo v poli **Zodopovědná osoba** můžete vybrat skupinu odpovědného pracovníka údržby nebo odpovědného pracovníka údržby.</span><span class="sxs-lookup"><span data-stu-id="9471b-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="9471b-131">Tato nastavení lze změnit, pokud je pracovní příkaz aktivní.</span><span class="sxs-lookup"><span data-stu-id="9471b-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="9471b-132">Lze je například změnit, když se změní stav životního cyklu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="9471b-133">Automatický výběr provedený při vytvoření pracovního příkazu je založen na nastavení na stránce **Odpovědní pracovníci údržby**.</span><span class="sxs-lookup"><span data-stu-id="9471b-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="9471b-134">Pokud přidáte nebo odeberete úlohy pracovní objednávky po vytvoření pracovní objednávky a pole **Odpovědná skupina** a pole **Odpovědný** jsou při aktualizaci pracovního příkazu prázdné, vyhledá Správa majetku možné párování ve formuláři nastavení pro skupinu odpovědných pracovníků údržby nebo odpovědného pracovníka údržby pro možnou shodu na stránce nastavení.</span><span class="sxs-lookup"><span data-stu-id="9471b-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="9471b-135">Pokud je pole **Odpovědná skupina** nebo **Odpovědný pracovník** po aktualizaci pracovního příkazu už nastaveno, nebudou provedeny žádné změny.</span><span class="sxs-lookup"><span data-stu-id="9471b-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="9471b-136">Další informace o tom, jak nastavit zodpovědné pracovníky pdržby a skupiny pracovníků, naleznete v tématu [Zodpovědní pracovníci údržby](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="9471b-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="9471b-137">Ze stránky [Stav údržby](../controlling-and-reporting/maintenance-status.md) můžete provést výpočet pro získání přehledu pracovního vytížení, které se týkají příchozích a dokončených pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="9471b-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="9471b-138">V zobrazení podrobností na stránce **Všechny pracovní příkazy** na pevné záložce **Podrobnosti řádku** můžete pomocí polí **Zeměpisná šířka** a **Zeměpisná délka** přidat zeměpisné souřadnice majetku vybraného v úloze pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="9471b-139">Vytvořit související pracovní příkaz</span><span class="sxs-lookup"><span data-stu-id="9471b-139">Create related work order</span></span>

<span data-ttu-id="9471b-140">Můžete vytvořit pracovní příkaz na základě stávajícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="9471b-141">To je užitečné třeba v případě, že chcete registrovat primární a sekundární pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="9471b-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="9471b-142">Nový pracovní příkaz je založen na úloze pracovního příkazu z existujícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="9471b-143">Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="9471b-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9471b-144">Vyberte pracovní příkaz, pro který chcete vytvořit související pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="9471b-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="9471b-145">V podokně akcí na kartě **Pracovní příkaz** ve skupině **Nový** vyberte **Související pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="9471b-146">V dialogovém okně **Vytvořit související pracovní příkaz** vyberte úlohu pracovního příkazu, pro kterou chcete vytvořit související pracovní příkaz v poli **Úloha pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="9471b-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="9471b-147">V poli **Typ práce údržby** vyberte typ práce údržby.</span><span class="sxs-lookup"><span data-stu-id="9471b-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="9471b-148">V polích **Varianta typu práce údržby** a **Obor** vyberte pro typ práce údržby související variantu typu práce údržby a obor.</span><span class="sxs-lookup"><span data-stu-id="9471b-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="9471b-149">Je-li tento pracovní příkaz první související pracovní příkaz, který byl vytvořen pro vybraný pracovní příkaz, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="9471b-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="9471b-150">Vyberte možnost **Nový pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="9471b-151">V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="9471b-152">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="9471b-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="9471b-153">V případě potřeby změňte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.</span><span class="sxs-lookup"><span data-stu-id="9471b-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="9471b-154">V polích **Očekávaný začátek** a **Očekávaný konec** vyberte počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="9471b-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="9471b-155">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9471b-155">Select **OK**.</span></span> <span data-ttu-id="9471b-156">Nový související pracovní příkaz se zobrazí na stránce seznamu **Všechny pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="9471b-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="9471b-157">Pokud se jedná o pracovní příkaz, pro který vytváříte tent související pracovní příkaz, pro již existují související pracovní příkazy, přidejte pomocí následujících kroků novou úlohu pracovního příkazu do existujícího souvisejícího pracovního příkazu:</span><span class="sxs-lookup"><span data-stu-id="9471b-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="9471b-158">Vyberte možnost **Přidat do souvisejícího pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="9471b-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="9471b-159">Pak v poli **pracovní příkaz** vyberte související pracovní příkaz, ke kterému chcete přidat novou úlohu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="9471b-160">V případě potřeby změňte úroveň služeb pracovního příkazu v poli **Úroveň služeb**.</span><span class="sxs-lookup"><span data-stu-id="9471b-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="9471b-161">V polích **Očekávaný začátek** a **Očekávaný konec** změňte podle potřeby očekávané počáteční a koncové datum.</span><span class="sxs-lookup"><span data-stu-id="9471b-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="9471b-162">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9471b-162">Select **OK**.</span></span> <span data-ttu-id="9471b-163">Úloha pracovního příkazu se přidá do existujícího souvisejícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="9471b-164">Na následujícím obrázku je uveden příklad dialogu **Vytvořit související pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Obrázek č. 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="9471b-166">Pokud jste nastavili související masku pracovního příkazu na kartě **Parametry správy majetku** > **Pracovní příkazy** > **Související maska pracovního příkazu**, budou v souladu s nastavením masky vytvořena ID pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="9471b-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="9471b-167">Není-li nastavena žádná související maska pracovního příkazu, bude pro související pracovní příkazy použito další dostupné ID pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="9471b-168">Zkopírování pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="9471b-168">Copy a work order</span></span>

<span data-ttu-id="9471b-169">Nový pracovní příkaz lze rychle vytvořit z existujícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="9471b-170">Tento postup práce s pracovními příkazy se liší od vytváření pracovních příkazů na základě [plánů údržby](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="9471b-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="9471b-171">To je užitečné například v případě, že máte pracovní příkaz obsahující mnoho úloh pracovního příkazu s různými úlohami v různých majetcích, které by měly být v pravidelných intervalech dokončeny.</span><span class="sxs-lookup"><span data-stu-id="9471b-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="9471b-172">Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="9471b-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="9471b-173">Vyberte pracovní příkaz, ze kterého chcete kopírovat obsah.</span><span class="sxs-lookup"><span data-stu-id="9471b-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="9471b-174">V podokně akcí na kartě > **Pracovní příkaz** ve skupině > **Nový** vyberte **Kopírovat pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="9471b-175">Zobrazí se nastavení pracovního příkazu z vybraného pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="9471b-176">V případě potřeby můžete některá pole upravit.</span><span class="sxs-lookup"><span data-stu-id="9471b-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="9471b-177">Výběrem **OK** vytvořte nový pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="9471b-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="9471b-178">Na stránce se seznamem **Všechny pracovní příkazy** můžete podle potřeby upravit požadovaný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="9471b-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="9471b-179">Při vytvoření nového pracovního příkazu se některé informace zkopírují přímo z existujícího pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="9471b-180">Informace o prognózách, nástrojích, kontrolních seznamech údržby, funkčním místě, adresách a plánování nejsou kopírovány.</span><span class="sxs-lookup"><span data-stu-id="9471b-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="9471b-181">Místo toho je inicializován z aktuálního nastavení v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="9471b-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="9471b-182">Proto, pokud byly tyto informace změněny mezi časem vytvoření prvního pracovního příkazu a časem, kdy jste provedli kopii pracovní objednávky, budou změny zahrnuty do nového pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="9471b-183">Příkladem jsou změny v prognózách nebo aktualizace kontrolních seznamů údržby.</span><span class="sxs-lookup"><span data-stu-id="9471b-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="9471b-184">Na následujícím obrázku je uveden příklad dialogového okna **Kopírovat pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Obrázek č. 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="9471b-186">Vytvoření pracovního příkazu na základě požadavku na údržbu</span><span class="sxs-lookup"><span data-stu-id="9471b-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="9471b-187">Vyberte **Správa majetku** > **Společné** > **Požadavky na údržbu** > **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu**.</span><span class="sxs-lookup"><span data-stu-id="9471b-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="9471b-188">Vyberte požadavek na údržbu, pro který chcete vytvořit pracovní příkaz, a klikněte na tlačítko **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="9471b-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="9471b-189">V podokně akcí na kartě > **Požadavek na údržbu** ve skupině > **Nový** vyberte **Pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="9471b-190">V dialogovém okně **Pracovní příkaz** nastavte pole.</span><span class="sxs-lookup"><span data-stu-id="9471b-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="9471b-191">Pokud byl v požadavku na údržbu vybrán typ úlohy údržby, můžete v případě potřeby vybrat jiný typ úlohy údržby při vytvoření pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="9471b-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="9471b-192">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9471b-192">Select **OK**.</span></span> <span data-ttu-id="9471b-193">Zpráva vás informuje o tom, že byl pracovní příkaz vytvořen.</span><span class="sxs-lookup"><span data-stu-id="9471b-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="9471b-194">Chcete-li zobrazit, které pracovní příkazy jsou spojeny s požadavkem na údržbu, vyberte požadavek na údržbu v seznamech **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** a klikněte na tlačítko Pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="9471b-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="9471b-195">Pak v podokně akcí na kartě **Požadavek na údržbu** ve skupině **Zobrazit** vyberte **Pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="9471b-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="9471b-196">Na následujícím obrázku je uveden příklad dialogového okna **Vytvořit pracovní příkaz**.</span><span class="sxs-lookup"><span data-stu-id="9471b-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Obrázek č. 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="9471b-198">Pokud chcete, aby se pracovní příkazy vytvářely automaticky, můžete naplánovat úlohy plánu údržby nebo nastavit automatické vytvoření [plánů údržby](../preventive-and-reactive-maintenance/maintenance-plans.md) nebo [pořadí údržby](../preventive-and-reactive-maintenance/maintenance-rounds.md) u majetku.</span><span class="sxs-lookup"><span data-stu-id="9471b-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="9471b-199">Pracovní příkazy vytvořené z požadavků na údržbu na stránce se seznamem **Rozvrh veškeré údržby** jsou vytvořeny s typy úloh údržby vybranými v požadavcích na údržbu.</span><span class="sxs-lookup"><span data-stu-id="9471b-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>

