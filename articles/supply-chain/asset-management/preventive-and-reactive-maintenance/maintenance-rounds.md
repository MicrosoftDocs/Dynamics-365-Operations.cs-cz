---
title: Pořadí údržby
description: Toto téma popisuje pořadí údržby v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a3a64593a2155d35e78b0d854c7367fa65d1c5c8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018539"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="8ec3e-103">Pořadí údržby</span><span class="sxs-lookup"><span data-stu-id="8ec3e-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8ec3e-104">V modulu **Správa majetku** můžete vytvořit pořadí údržby pro různé položky majetku, u kterých je třeba v pravidelných intervalech provádět podobné úkoly.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="8ec3e-105">Například úlohy namazání nebo úlohy bezpečnostní prohlídky, které je třeba provést na několika strojích ve stejných intervalech.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="8ec3e-106">Prvním krokem je vytvoření pořadí údržby, včetně majetku, který vyžaduje stejný formulář práce údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="8ec3e-107">Dále naplánujete pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="8ec3e-108">Po vytvoření rozvrhu pořadí údržby můžete zobrazit všechny záznamy úloh, které se týkají pořadí, v částech **Všechny rozvrhy údržby** a **Otevřené řádky rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="8ec3e-109">Pořadí úržby lze vytvořit i ve funkčních místech pro dokončení pro položky majetku instalované ve funkčních místech v čase vytvoření pracovního příkazu na základě pořadí.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="8ec3e-110">Další informace o nastavení pořadí údržby pro funkční místa naleznete v tématu [Vytvoření funkčních míst](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="8ec3e-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="8ec3e-111">Nastavení pořadí údržby</span><span class="sxs-lookup"><span data-stu-id="8ec3e-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="8ec3e-112">Klikněte na **Správa majetku** > **Nastavení** > **Preventivní údržba** > **Pořadí údržby**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="8ec3e-113">Nové pořadí údržby vytvoříte klepnutím na položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="8ec3e-114">Do pole **Pořadí údržby** zadejte ID a do pole **Název** zadejte název pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="8ec3e-115">V poli **Počáteční datum** vyberte počáteční datum pořadí.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="8ec3e-116">Do polí **Dokončit v řádu dnů** a **Dokončit v řádu hodin** můžete zadat očekávané koncové datum ve dnech nebo hodinách.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="8ec3e-117">Očekávané koncové datum je vypočítáno relativně k datu zahájení, které je vypočítáno při vytvoření řádků rozvrhu údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="8ec3e-118">Chcete-li například určit, že související úloha má být dokončena do týdne od počátečního data, můžete do pole **Dokončit v řádu dnů** vložit hodnotu „7“.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="8ec3e-119">Chcete-li automaticky vytvořit pracovní příkazy z řádků rozvrhu údržby vytvořených z tohoto pořadí údržby, vyberte možnost „Ano“ na přepínači **Automaticky vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="8ec3e-120">V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu, který se použije pro pracovní příkazy vytvořené z tohoto pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="8ec3e-121">V poli **Úroveň služeb** vyberte úroveň služeb pracovního příkazu, který se použije pro pracovní příkazy vytvořené z tohoto pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="8ec3e-122">Na záložce s náhledem **Řádky majetku** kliknutím na **Přidat** přidáte majetek do plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="8ec3e-123">Číslo řádku se automaticky vloží do pole **Číslo řádku** a označuje posloupnost položek majetku v pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="8ec3e-124">V poli **Majetek** vyberte majetek.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="8ec3e-125">V poli **Typ práce údržby** vyberte typ práce údržby pro majetek.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="8ec3e-126">V případě potřeby vyberte **Vyrianta typu práce údržby** a **Obor** související s typem práce údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="8ec3e-127">Vyberte opakování (den, týden atd.) v poli **Typ období**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="8ec3e-128">Do pole **Frekvence období** zadejte počet opakování pro plán údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="8ec3e-129">Příklad: Pokud jste v poli **Typ období** vybrali možnost „Den“ a do tohoto pole zadáte číslo „7“, budou během plánování preventivní údržby jednou týdně vytvořeny nové řádky pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="8ec3e-130">V poli **Počáteční datum** vyberte počáteční datum majetku, který má být součástí pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="8ec3e-131">Toto datum se může lišit od počátečního data pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="8ec3e-132">Chcete-li přidat více položek majetku do pořadí údržby, zopakujte kroky 9 až 16.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="8ec3e-133">Na záložce s náhledem **Řádky funkčních míst** kliknutím na **Přidat** přidáte funkční místo do plánu údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="8ec3e-134">Viz popis souvisejících polí výše.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="8ec3e-135">Stejná pole jsou k dispozici jako pro vytvoření řádku majetku, ale v případě potřeby můžete také vybrat možnost **Výrobce** a **Model** pro funkční místo.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="8ec3e-136">Pokud jste vybrali pouze funkční místo na řádku, ale nevytvoříte žádný výběr pro **Typ majetku**, **Výrobce**, **Model**, **Typ práce údržby**, **Varianta typu práce údržby** a **Obor**, veškerý majetek související s tímto funkčním místem v době plánování údržby bude zahrnut do pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="8ec3e-137">Na záložce s náhledem **Fondy** klikněte na tlačítko **Přidat** a vyberte fond pracovních příkazů, který má být zahrnut do pořadí údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="8ec3e-138">K jednomu pořadí údržby lze připojit několik fondů pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="8ec3e-139">Uložte provedené nastavení.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="8ec3e-140">Pole **Majetek** a **Řádky** umístěné ve skupině **Podrobnosti** na záložce s náhledem **Záhlaví** zobrazují celkový počet položek majetku a řádků souvisejících s vybraným pořadím údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="8ec3e-141">Následující obrázek znázorňuje ukázku a příklad pořadí údržby obsahující tři aktiva.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Obrázek č. 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="8ec3e-143">Naplánovat pořadí údržby</span><span class="sxs-lookup"><span data-stu-id="8ec3e-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="8ec3e-144">Když nastavíte pořadí údržby, spusťte úlohu plánu, která plánuje všechny úlohy související s pořadím údržby.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="8ec3e-145">Klikněte na **Správa majetku** > **Pravidelně** > **Preventivní údržba** > **Rozvrhnout pořadí údržby** nebo **Správa majetku** > **Společné** > **Rozvrh údržby** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby** nebo **Otevřené fondy rozvrhu údržby** > v seznamu vyberte řádek rozvrhu údržby > tlačítko **Plány údržby**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="8ec3e-146">V poli **Období** vyberte typ období, které se má použít pro úlohu plánování.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="8ec3e-147">V poli **Frekvence období** zadejte počet období, která mají být zahrnuta do úlohy plánování.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="8ec3e-148">Zahájení plánování je aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="8ec3e-149">Chcete-li, aby byla na základě plánu údržby zaokrouhlení automaticky vytvořen pracovní příkaz, vyberte možnost „Ano“ na přepínači **Automaticky vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="8ec3e-150">Je-li toto přepínací tlačítko nastaveno na hodnotu „Ano“ a přepínač **Automaticky vytvořit** je nastaven na „Ano“ pro plán údržby ve formuláři **Pořadí údržby**, budou vytvořeny pracovní příkazy na základě řádků pořadí údržby a budou vytvořeny také řádky plánu údržby se stavem „Pracovní příkaz vytvořen“.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="8ec3e-151">Je-li v tomto rozevíracím seznamu nebo ve formuláři **Pořadí údržby** nastaveno pouze jedno z přepínacích tlačítek **Automaticky vytvořit**, budou vytvořeny pouze řádky rozvrhu údržby ve stavu „Vytvořeno“.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="8ec3e-152">V takovém případě se žádné pracovní příkazy nevytvoří.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="8ec3e-153">Je-li to nutné, můžete vybrat konkrétní pořadí nebo jiné počáteční datum pro úlohu plánu.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="8ec3e-154">Klikněte namožnost **Filtr** a přidejte pořadí.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="8ec3e-155">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-155">Click **OK**.</span></span>

7. <span data-ttu-id="8ec3e-156">Nyní můete zobrazit úlohy pořadí údržby v částech **Správa majetku** > **Společné** > **Rozvrh údržby** > **Všechny rozvrhy údržby** nebo **Otevřené řádky rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="8ec3e-157">Jsou-li pořadí údržby připojena k fondu pracovních příkazů, zobrazí se také řádky rozrvhu údržby v části **Otevřené fondy rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="8ec3e-158">Řádky rozvrhu údržby vytvořené z pořadí mají typ odkazu „Rozvrhy údržby“.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="8ec3e-159">Následující dvě ilustrace zobrazují **úlohu plánování v** dialogovém okně Naplánovat pořadí údržby a řádky plánu údržby vytvořené ve **všech plánech** údržby na základě této úlohy plánu.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Obrázek č. 2](media/14-preventive-maintenance.png)

![Obrázek č. 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="8ec3e-162">Pokud jsou pro majetek, na který se vztahuje záruka dodavatele, vytvořeny pracovní příkazy ručně, zobrazí se dialogové okno, které uživatele upozorní na záruku.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="8ec3e-163">Vytvoření pracovního příkazu lze v tuto chvíli zrušit.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="8ec3e-164">Kontrola vztahu záruky je vynechána pro automaticky vytvořené pracovní příkazy.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="8ec3e-165">Na záložce s náhledem **Spustit na pozadí** můžete nastavit dávkovou úlohu pro plánování pořadí v pravidelných intervalech.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="8ec3e-166">Pokud je v několika fondech pracovních příkazů uvedeno pořadí (viz [Fondy pracovních příkazů](../work-orders/work-order-pools.md)), zobrazí se jeden záznam pro každý fond v části **Otevřené fondy rozvrhu údržby**.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="8ec3e-167">To je provedeno za účelem optimalizace možností filtrování pro fondy pracovních příkazů.</span><span class="sxs-lookup"><span data-stu-id="8ec3e-167">This is done to optimize the filtering options for work order pools.</span></span>

