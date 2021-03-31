---
title: Kontrola kvality
description: Toto téma obsahuje informace o funkci Kontrola kvality. Tato funkce umožňuje pracovníkům skladu provádět rychlé namátkové kontroly kvality, zatímco přijímají položky do oblasti příchozího doku.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSQualityCheckTemplate, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSQualityCheckResult
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 31afcfcb9d8dbb91f4ea4e3e7a7282c2a87328d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228458"
---
# <a name="quality-check"></a><span data-ttu-id="5f20e-104">Kontrola kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-104">Quality check</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f20e-105">Funkce *Kontrola kvality* umožňuje pracovníkům skladu provádět rychlé namátkové kontroly kvality, zatímco přijímají položky do oblasti příchozího doku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-105">The *Quality check* feature lets warehouse workers do quick spot checks for quality while they receive items to the inbound dock area.</span></span> <span data-ttu-id="5f20e-106">Tyto namátkové kontroly jsou výhodné, když pracovníci kontrolují obaly nebo jiné snadno rozpoznatelné části položky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-106">These spot checks are beneficial when workers inspect packaging or other easily recognizable parts of an item.</span></span> <span data-ttu-id="5f20e-107">Tato funkce vede pracovníky, aby se rychle podívali a zjistili, zda je něco zjevně vadné nebo poškozené před tím, než doplní zásoby ve skladovém místě po výdeji.</span><span class="sxs-lookup"><span data-stu-id="5f20e-107">The feature guides workers to take a quick look to see whether anything is obviously faulty or damaged before they stock the inventory in its putaway location.</span></span>

<span data-ttu-id="5f20e-108">Tato funkce je alternativou ke standardnímu procesu kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-108">This feature is an alternative to the standard quality check process.</span></span> <span data-ttu-id="5f20e-109">Nabízí větší flexibilitu a rychlejší zpracování.</span><span class="sxs-lookup"><span data-stu-id="5f20e-109">It offers more flexibility and faster processing.</span></span>

<span data-ttu-id="5f20e-110">Při použití této funkce dojde ke kontrole příjezdu a kvality následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="5f20e-110">When you use this feature, the arrival and quality check occur in the following way:</span></span>

1. <span data-ttu-id="5f20e-111">Když dorazí zásilka, pracovník skladu zaznamená příchod.</span><span class="sxs-lookup"><span data-stu-id="5f20e-111">When a shipment arrives, a warehouse worker registers the arrival.</span></span> <span data-ttu-id="5f20e-112">Pracovník také naskenuje registrační značku a zaregistruje místo.</span><span class="sxs-lookup"><span data-stu-id="5f20e-112">The worker also scans a license plate to register the location.</span></span>
1. <span data-ttu-id="5f20e-113">Pracovník provede rychlou kontrolu kvality a zaznamená výsledek (úspěšný nebo neúspěšný) dané registrační značky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-113">The worker does a quick quality check and records the result (pass or fail) for that license plate.</span></span>
1. <span data-ttu-id="5f20e-114">Nastane jedna z následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="5f20e-114">One of the following actions occurs:</span></span>

    - <span data-ttu-id="5f20e-115">Pokud je kontrola kvality úspěšná, je registrační značka přijata a navedena obvyklým způsobem na přijímací místo.</span><span class="sxs-lookup"><span data-stu-id="5f20e-115">If the quality check is passed, the license plate is accepted and guided to a receiving location, as usual.</span></span>
    - <span data-ttu-id="5f20e-116">Pokud se kontrola kvality nezdaří, je registrační značka odmítnuta a stávající práce výdeje pro ni je přesměrována na alternativní místo k další kontrole.</span><span class="sxs-lookup"><span data-stu-id="5f20e-116">If the quality check is failed, the license plate is rejected, and existing putaway work for it is redirected to an alternate location for further inspection.</span></span> <span data-ttu-id="5f20e-117">Je vytvořena nová objednávka kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-117">A new quality order is created.</span></span> <span data-ttu-id="5f20e-118">Chcete-li zobrazit objednávku kvality vytvořenou při kontrole kvality, která se nezdařila, přejděte na **Řízení zásob \> Periodické úkoly \> Řízení kvality \> Objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-118">To view the quality order that is created from the failed quality check, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="5f20e-119">Tento proces lze také nastavit tak, aby všechny naskenované registrační značky byly okamžitě přesměrovány na místo kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-119">This process can also be set up so that all scanned license plates are immediately diverted to the quality check location.</span></span>

## <a name="turn-on-the-quality-check-feature"></a><span data-ttu-id="5f20e-120">Zapnutí funkce kontroly kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-120">Turn on the Quality check feature</span></span>

<span data-ttu-id="5f20e-121">Než můžete použít funkci *Kontrola kvality*, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="5f20e-121">Before you can use the *Quality check* feature, it must be turned on in your system.</span></span> <span data-ttu-id="5f20e-122">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="5f20e-122">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5f20e-123">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="5f20e-123">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5f20e-124">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="5f20e-124">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5f20e-125">**Název funkce:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-125">**Feature name:** *Quality check*</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="5f20e-126">Nastavení funkce pro tento vzorový scénář</span><span class="sxs-lookup"><span data-stu-id="5f20e-126">Set up the feature for the example scenario</span></span>

<span data-ttu-id="5f20e-127">Tato část obsahuje pokyny a příklad, který ukazuje, jak nastavit funkci *Kontrola kvality* a připravit ukázková data pro příkladový scénář, který je uveden dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-127">This section provides guidelines and an example that shows how to set up the *Quality check* feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="5f20e-128">Příprava ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="5f20e-128">Make sample data available</span></span>

<span data-ttu-id="5f20e-129">Chcete-li s [příkladovým scénářem](#example-scenario) pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-129">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="5f20e-130">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-130">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="quality-check-template"></a><a name="quality-template"></a><span data-ttu-id="5f20e-131">Šablona kontroly kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-131">Quality check template</span></span>

<span data-ttu-id="5f20e-132">Šablona kontroly kvality definuje pravidla pro provádění rychlých přímých kontrol kvality v době přijetí.</span><span class="sxs-lookup"><span data-stu-id="5f20e-132">The quality check template defines the rules for doing quick spot checks for quality at the time of receiving.</span></span>

1. <span data-ttu-id="5f20e-133">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Šablona kontroly kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-133">Go to **Warehouse management \> Setup \> Work \> Quality check template**.</span></span>
1. <span data-ttu-id="5f20e-134">Chcete-li přidat šablonu do mřížky, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-134">Select **New** to add a template to the grid.</span></span>
1. <span data-ttu-id="5f20e-135">Definujte novou šablonu nastavením následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="5f20e-135">Set the following values to define the new template:</span></span>

    - <span data-ttu-id="5f20e-136">**Název šablony kontroly kvality:** *Dock check*</span><span class="sxs-lookup"><span data-stu-id="5f20e-136">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="5f20e-137">Zadejte název, který identifikuje zásady použité pro tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-137">Enter a name that identifies the policies applied for this template.</span></span>

    - <span data-ttu-id="5f20e-138">**Zásady přijímání:** *Vyzvat uživatele*</span><span class="sxs-lookup"><span data-stu-id="5f20e-138">**Acceptance policy:** *Prompt user*</span></span>

        <span data-ttu-id="5f20e-139">Určete, zda by uživatelé měli být při zpracování práce vyzváni k přijetí nebo odmítnutí kvality zásob, nebo zda by kvalita měla být automaticky odmítnuta.</span><span class="sxs-lookup"><span data-stu-id="5f20e-139">Specify whether users should be prompted to accept or reject the quality of the inventory while they process the work, or whether the quality should automatically be rejected.</span></span> <span data-ttu-id="5f20e-140">Dostupné možnosti jsou *Automatické odmítnutí* a *Vyzvat uživatele*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-140">The available options are *Auto reject* and *Prompt user*.</span></span>

    - <span data-ttu-id="5f20e-141">**Zásady zpracování kvality:** *Vytvořte objednávku kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-141">**Quality processing policy:** *Create quality order*</span></span>

        <span data-ttu-id="5f20e-142">Vyberte zásady, které by měly být použity při odmítnutí kvality zásob.</span><span class="sxs-lookup"><span data-stu-id="5f20e-142">Select the policy that should be used when the quality of the inventory is rejected.</span></span> <span data-ttu-id="5f20e-143">Existují tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="5f20e-143">The following options are available:</span></span>

        - <span data-ttu-id="5f20e-144">*Vytvořit pouze práci* - Jednoduše vytvořte práci, která usnadní pohyb zásob.</span><span class="sxs-lookup"><span data-stu-id="5f20e-144">*Create work only* – Just create work to facilitate inventory movement.</span></span>
        - <span data-ttu-id="5f20e-145">*Vytvořit objednávku kvality* - Vytvořte objednávku kvality, která usnadní zkoušky kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-145">*Create quality order* – Create a quality order to facilitate quality tests.</span></span>

    - <span data-ttu-id="5f20e-146">**Testovací skupina:** *Příloha*</span><span class="sxs-lookup"><span data-stu-id="5f20e-146">**Test group:** *Enclosure*</span></span>

        <span data-ttu-id="5f20e-147">Určete testovací skupinu, která by měla být použita ve vytvořené objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-147">Specify the test group that should be used in the quality order that is created.</span></span> <span data-ttu-id="5f20e-148">Testovací skupiny jsou nastaveny v rámci modulu **Řízení zásob**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-148">Test groups are set up in the **Inventory management** module.</span></span>

        <span data-ttu-id="5f20e-149">Nechte možnost **Destruktivní text** pro testovací skupinu vypnutou.</span><span class="sxs-lookup"><span data-stu-id="5f20e-149">Leave the **Destructive text** option turned off for the test group.</span></span> <span data-ttu-id="5f20e-150">Tato možnost definuje, zda při testech v testovací skupině dojde ke zničení vzorku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-150">This option defines whether the sample will be destroyed as part of the tests in the test group.</span></span> <span data-ttu-id="5f20e-151">Pokud je použit destruktivní test, systém generuje transakci, když je pro položku vytvořena objednávka kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-151">If a destructive test is used, the system generates an inventory transaction when a quality order is created for an item.</span></span> <span data-ttu-id="5f20e-152">Nová skladová transakce odhadne snížení zásob pro testované množství.</span><span class="sxs-lookup"><span data-stu-id="5f20e-152">The new inventory transaction predicts the inventory reduction for the test quantity.</span></span> <span data-ttu-id="5f20e-153">Dokončení objednávky kvality v kroku ověření způsobí snížení zásob.</span><span class="sxs-lookup"><span data-stu-id="5f20e-153">The inventory reduction occurs when the quality order is completed through the validation step.</span></span> <span data-ttu-id="5f20e-154">Skladová transakce je označena jako objednávka kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-154">The inventory transaction is identified as a quality order.</span></span>

### <a name="work-class--quality-check"></a><a name="work-class"></a><span data-ttu-id="5f20e-155">Třída práce - kontrola kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-155">Work class – Quality check</span></span>

<span data-ttu-id="5f20e-156">Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních příkazů, které pracovníci skladu může v mobilním zařízení zpracovat.</span><span class="sxs-lookup"><span data-stu-id="5f20e-156">Work classes are used to direct and/or limit the type of work order lines that warehouse workers can process on a mobile device.</span></span>

1. <span data-ttu-id="5f20e-157">Přejděte na **Řízení skladu \> Nastavení \> Práce \> Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-157">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="5f20e-158">Zvolte **Nová** pro vytvoření třídy práce.</span><span class="sxs-lookup"><span data-stu-id="5f20e-158">Select **New** to create a work class.</span></span>
1. <span data-ttu-id="5f20e-159">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-159">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f20e-160">**ID pracovní třídy:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-160">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="5f20e-161">Zadejte název, který identifikuje pracovní třídu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-161">Enter a name that identifies the work class.</span></span>

    - <span data-ttu-id="5f20e-162">**Popis:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-162">**Description:** *QC Check*</span></span>

        <span data-ttu-id="5f20e-163">Zadejte krátký popis, který označuje, k čemu je pracovní třída používána.</span><span class="sxs-lookup"><span data-stu-id="5f20e-163">Enter a short description that indicates what the work class is used for.</span></span>

    - <span data-ttu-id="5f20e-164">**Typ pracovního příkazu:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-164">**Work order type:** *Quality in quality check*</span></span>

        <span data-ttu-id="5f20e-165">Vyberte typ pracovního příkazu vytvořeného pracovní třídou.</span><span class="sxs-lookup"><span data-stu-id="5f20e-165">Select the type of work order that is created by the work class.</span></span> <span data-ttu-id="5f20e-166">Při nastavování kontroly kvality vždy vyberte *Kontrola kvality*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-166">When you set up quality control work, always select *Quality in quality check*.</span></span>

1. <span data-ttu-id="5f20e-167">Na pevné záložce **Platné typy umístění** nechte pole **Typ místa** prázdné.</span><span class="sxs-lookup"><span data-stu-id="5f20e-167">On the **Valid put location types** FastTab, leave the **Location type** field blank.</span></span>

    <span data-ttu-id="5f20e-168">Pokud vyberete typ umístění, omezíte umístění, kam lze položky po jejich výběru umístit.</span><span class="sxs-lookup"><span data-stu-id="5f20e-168">If you select a location type, you limit the locations where items can be put after they are picked.</span></span> <span data-ttu-id="5f20e-169">Toto pole se používá, když se směrnice umístění pokusí o překlad umístění nebo když pracovník skladu ručně zadá umístění pro položku nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f20e-169">This field is used when a location directive tries to resolve the location, or when a warehouse worker manually specifies the location for the mobile device menu item.</span></span>

<span data-ttu-id="5f20e-170">Další informace o pracovních třídách a o tom, jak je vytvořit, viz [Vytvoření pracovní třídy](tasks/create-work-class.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-170">For more information about work classes and how to create them, see [Create a work class](tasks/create-work-class.md).</span></span>

### <a name="work-template"></a><span data-ttu-id="5f20e-171">Šablona práce</span><span class="sxs-lookup"><span data-stu-id="5f20e-171">Work template</span></span>

<span data-ttu-id="5f20e-172">Šablony práce umožňují definovat pracovní operace, které musí být provedeny ve skladu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-172">Work templates let you define the work operations that must be performed in the warehouse.</span></span> <span data-ttu-id="5f20e-173">Obvykle pracovní operace ve skladu sestávají z páru akcí: skladoví pracovníci vyskladní zásoby na skladě na jednom místě a převedou vyskladněné zásoby v jiném skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="5f20e-173">Typically, warehouse work operations consist of a pair of actions: a warehouse worker picks on-hand inventory up in one location and then puts the picked inventory down in another location.</span></span> <span data-ttu-id="5f20e-174">Pracovní šablona pro kontrolu kvality definuje pracovní operace pro provádění kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-174">A work template for quality control defines the work operations for doing quality checks.</span></span>

#### <a name="purchase-orders"></a><span data-ttu-id="5f20e-175">Nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="5f20e-175">Purchase orders</span></span>

1. <span data-ttu-id="5f20e-176">Přejděte do **Řízení skladu \> Nastavení \> Práce \> Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-176">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="5f20e-177">V záhlaví nastavte pole **Typ pracovního příkazu** na *Nákupní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-177">In the header, set the **Work order type** field to *Purchase orders*.</span></span>
1. <span data-ttu-id="5f20e-178">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-178">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5f20e-179">Vyberte pracovní šablonu, která by měla zahrnovat krok kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-179">Select a work template that should include a quality check step.</span></span> <span data-ttu-id="5f20e-180">V části **Přehled** v poli **Šablona práce** vyberte *Příjemka NO 51*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-180">In the **Overview** section, in the **Work template** field, select *51 PO Receipt*.</span></span>
1. <span data-ttu-id="5f20e-181">V části **Podrobnosti pracovní šablony** si všimněte, že mřížka má dva existující řádky: jeden pro *Výběr* a jeden pro *Vložení*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-181">In the **Work template details** section, notice that the grid has two existing lines: one for *Pick* and one for *Put*.</span></span>
1. <span data-ttu-id="5f20e-182">V části **Podrobnosti pracovní šablony** vyberte **Nový** pro přidání řádku pro kontrolu kvality do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-182">In the **Work template details** section, select **New** to add a row for quality control to the grid.</span></span> <span data-ttu-id="5f20e-183">Všimněte si, že pole **Číslo řádku** pro nový řádek je nastaveno na *3*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-183">Notice that the **Line number** field for the new line is set to *3*.</span></span>
1. <span data-ttu-id="5f20e-184">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="5f20e-184">On the new line, set the following values.</span></span> <span data-ttu-id="5f20e-185">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="5f20e-185">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="5f20e-186">**Typ práce:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-186">**Work type:** *Quality check*</span></span>
    - <span data-ttu-id="5f20e-187">**ID pracovní třídy:** *Nákup*</span><span class="sxs-lookup"><span data-stu-id="5f20e-187">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="5f20e-188">**Název šablony kontroly kvality:** *Dock check*</span><span class="sxs-lookup"><span data-stu-id="5f20e-188">**Quality check template name:** *Dock check*</span></span>

        <span data-ttu-id="5f20e-189">Vyberte jedinečný identifikátor pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="5f20e-189">Select the unique ID for the work class.</span></span> <span data-ttu-id="5f20e-190">Tato hodnota umožňuje konfiguraci položek nabídky mobilního zařízení a typů práce, které tyto položky nabídky mohou zpracovat.</span><span class="sxs-lookup"><span data-stu-id="5f20e-190">You use this value to configure the menu items on the mobile device and the types of work that those menu items can process.</span></span>

1. <span data-ttu-id="5f20e-191">V podokně Akce vyberte **Uložit** pro uložení dosavadní práce.</span><span class="sxs-lookup"><span data-stu-id="5f20e-191">On the Action Pane, select **Save** to save your work so far.</span></span>

    <span data-ttu-id="5f20e-192">Obdržíte informační zprávu, která uvádí: „Neplatné - kontrola kvality musí přijít ihned po vyzvednutí.“</span><span class="sxs-lookup"><span data-stu-id="5f20e-192">You receive an informational message that states, "Invalid - Quality check must come directly after a pick."</span></span> <span data-ttu-id="5f20e-193">Proto musíte změnit hodnotu **Číslo řádku** pro řádek, který jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="5f20e-193">Therefore, you must change the **Line number** value for the line that you just added.</span></span>

1. <span data-ttu-id="5f20e-194">Postupujte podle těchto kroků a změňte hodnotu **Číslo řádku** pro nový řádek:</span><span class="sxs-lookup"><span data-stu-id="5f20e-194">Follow these steps to change the **Line number** value for the new line:</span></span>

    1. <span data-ttu-id="5f20e-195">V části **Podrobnosti pracovní šablony** vyberte řádek, na kterém je pole **Typ práce** nastaveno na *Kontrola kvality*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-195">In the **Work template details** section, select the line where the **Work type** field is set to *Quality check*.</span></span>
    2. <span data-ttu-id="5f20e-196">Vyberte tlačítko **Posunout nahoru** nebo **Posunout dolů** pro přesunutí řádku *Kontrola kvality* za řádek *Vyzvednout*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-196">Select the **Move up** or **Move down** button to move the *Quality check* line so that it's after the *Pick* line.</span></span>

1. <span data-ttu-id="5f20e-197">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-197">On the Action Pane, select **Save**.</span></span>

#### <a name="quality-in-quality-check"></a><span data-ttu-id="5f20e-198">Kvalita v kontrole kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-198">Quality in quality check</span></span>

<span data-ttu-id="5f20e-199">Dále vytvořte pracovní šablonu pro kontrolu kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-199">Next, create a work template for the quality check.</span></span>

1. <span data-ttu-id="5f20e-200">V záhlaví **Pracovní šablony** změňte hodnotu pole **Typ pracovního příkazu** na *Kontrola kvality*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-200">In the header of the **Work templates** page, change the value of the **Work order type** field to *Quality in quality check*.</span></span>
1. <span data-ttu-id="5f20e-201">V podokně Akce vyberte možnost **Nový** pro přidání řádku do mřížky v části **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-201">On the Action Pane, select **New** to add a row to the grid in the **Overview** section.</span></span>
1. <span data-ttu-id="5f20e-202">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-202">In the new row, set the following values:</span></span>

    - <span data-ttu-id="5f20e-203">**Šablona práce:** *51 Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-203">**Work template:** *51 Quality Check*</span></span>

        <span data-ttu-id="5f20e-204">Zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="5f20e-204">Enter a name for the template.</span></span>

    - <span data-ttu-id="5f20e-205">**Popis šablony práce:** *51 Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-205">**Work template description:** *51 Quality Check*</span></span>

1. <span data-ttu-id="5f20e-206">Chcete-li, aby byla dostupná část **Podrobnosti šablony práce**, klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-206">On the Action Pane, select **Save** to make the **Work template details** section available.</span></span>
1. <span data-ttu-id="5f20e-207">Zatímco nová šablona je stále vybrána v části **Přehled**, vyberte **Nový** v části **Podrobnosti pracovní šablony** pro přidání řádku do mřížky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-207">While the new template is still selected in the **Overview** section, select **New** in the **Work template details** section to add a row to the grid there.</span></span>
1. <span data-ttu-id="5f20e-208">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-208">In the new row, set the following values:</span></span>

    - <span data-ttu-id="5f20e-209">**Typ práce:** *Výdej*</span><span class="sxs-lookup"><span data-stu-id="5f20e-209">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="5f20e-210">**ID pracovní třídy:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-210">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="5f20e-211">Vyberte název [pracovní třídy](#work-class), který jste dříve vytvořili pro práci s kontrolou kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-211">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="5f20e-212">V části **Podrobnosti pracovní šablony** vyberte znovu **Nový** pro přidání jiného řádku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-212">In the **Work template details** section, select **New** again to add another row.</span></span>
1. <span data-ttu-id="5f20e-213">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-213">In the new row, set the following values:</span></span>

    - <span data-ttu-id="5f20e-214">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="5f20e-214">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5f20e-215">**ID pracovní třídy:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-215">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="5f20e-216">Vyberte název [pracovní třídy](#work-class), který jste dříve vytvořili pro práci s kontrolou kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-216">Select the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

1. <span data-ttu-id="5f20e-217">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-217">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="5f20e-218">Další informace týkající se šablon práce naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic umístění](control-warehouse-location-directives.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-218">For more information about work templates, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md)</span></span>

### <a name="location-directive--quality-failures"></a><span data-ttu-id="5f20e-219">Směrnice o umístění - selhání kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-219">Location directive – Quality failures</span></span>

<span data-ttu-id="5f20e-220">Směrnice skladového místa jsou pravidla, která pomáhají identifikovat místa vyskladnění a umístění pro pohyb zásob.</span><span class="sxs-lookup"><span data-stu-id="5f20e-220">Location directives are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="5f20e-221">V transakce prodejní objednávky například směrnice skladového místa určuje, které zboží bude vydáno a kam bude umístěno.</span><span class="sxs-lookup"><span data-stu-id="5f20e-221">For example, in a sales order transaction, a location directive determines where the items will be picked and where the picked items will be put.</span></span> <span data-ttu-id="5f20e-222">Musíte definovat pravidlo směrnice o umístění, abyste určili, jak budou prováděny kontroly kvality, které selhaly.</span><span class="sxs-lookup"><span data-stu-id="5f20e-222">You must configure a location directive rule to define how failed quality checks will be handled.</span></span>

1. <span data-ttu-id="5f20e-223">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-223">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="5f20e-224">V levém podokně nastavte pole **Typ pracovního příkazu** na *Nákupní objednávky* na práci se směrnicemi místa tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-224">In the left pane, set the **Work order type** field to *Purchase orders* to work with location directives of that type.</span></span>
1. <span data-ttu-id="5f20e-225">V podokně Akce vyberte možnost **Nová** k vytvoření direktivy místa pro kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-225">On the Action Pane, select **New** to create a location directive for quality checks.</span></span>
1. <span data-ttu-id="5f20e-226">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-226">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f20e-227">**Pořadové číslo:** Přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-227">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="5f20e-228">**Název:** *51 do kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-228">**Name:** *51 To Quality*</span></span>

1. <span data-ttu-id="5f20e-229">Na záložce s náhledem **Směrnice skladového místa** natavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="5f20e-229">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="5f20e-230">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="5f20e-230">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="5f20e-231">**Typ práce:** *Vložit*</span><span class="sxs-lookup"><span data-stu-id="5f20e-231">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5f20e-232">**Lokalita:** *5*</span><span class="sxs-lookup"><span data-stu-id="5f20e-232">**Site:** *5*</span></span>
    - <span data-ttu-id="5f20e-233">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="5f20e-233">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="5f20e-234">V podokně akcí kliknutím na **Uložit** uložte direktivu a zpřístupněte pevnou záložku **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-234">On the Action Pane select **Save** to save your directive and make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="5f20e-235">Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-235">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="5f20e-236">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="5f20e-236">On the new line, set the following values.</span></span> <span data-ttu-id="5f20e-237">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="5f20e-237">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="5f20e-238">**Od množství:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f20e-238">**From quantity:** *1*</span></span>
    - <span data-ttu-id="5f20e-239">**Do množství:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="5f20e-239">**To quantity:** *1000000*</span></span>

1. <span data-ttu-id="5f20e-240">V podokně akcí kliknutím na **Uložit** uložte nový řádek a zpřístupněte pevnou záložku **Akce direktivy místa**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-240">On the Action Pane, select **Save** to save the new line and make the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="5f20e-241">Když je na pevné záložce **Řádky** vybrán nový řádek, vyberte **Nový** na pevné záložce **Akce směrování polohy** pro přidání řádku do mřížky, abyste mohli nastavit akci pro linku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-241">While the new line is still selected on the **Lines** FastTab, select **New** on the **Location directive actions** FastTab to add a row to the grid there, so that you can set up an action for the line.</span></span>
1. <span data-ttu-id="5f20e-242">V novém řádku nastavte pole **Název** na *Kvalita*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-242">In the new row, set the **Name** field to *Quality*.</span></span> <span data-ttu-id="5f20e-243">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="5f20e-243">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="5f20e-244">V podokně akcí vyberte možnost **Uložit**, chcete-li, aby bylo tlačítko **Upravit dotaz** dostupné na pevné záložce **Akce direktivy umístění**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-244">On the Action Pane, select **Save** to make the **Edit query** button on the **Location directive actions** FastTab available.</span></span>
1. <span data-ttu-id="5f20e-245">V době, kdy je řádek, který jste právě přidali, stále vybrán na pevné záložce **Akce směrování polohy**, vyberte **Upravit dotaz** pro otevření dialogového okna, ve kterém můžete upravit dotaz pro akci.</span><span class="sxs-lookup"><span data-stu-id="5f20e-245">While the line that you just added is still selected on the **Location directive actions** FastTab, select **Edit query** to open a dialog box where you can edit the query for the action.</span></span>
1. <span data-ttu-id="5f20e-246">Na kartě **Oblast** přidejte řádek do dotazu výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-246">On the **Range** tab, select **Add** to add a row to the query.</span></span>
1. <span data-ttu-id="5f20e-247">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-247">In the new row, set the following values:</span></span>

    - <span data-ttu-id="5f20e-248">**Tabulka:** *umístění*</span><span class="sxs-lookup"><span data-stu-id="5f20e-248">**Table:** *Locations*</span></span>
    - <span data-ttu-id="5f20e-249">**Odvozená tabulka:** *Skladová místa*</span><span class="sxs-lookup"><span data-stu-id="5f20e-249">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="5f20e-250">**Pole:** *Skladové místo*</span><span class="sxs-lookup"><span data-stu-id="5f20e-250">**Field:** *Location*</span></span>
    - <span data-ttu-id="5f20e-251">**Kritéria:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="5f20e-251">**Criteria:** *QMS*</span></span>

    <span data-ttu-id="5f20e-252">Umístění *QMS* je umístění skladu pro kvalitu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-252">The *QMS* location is a warehouse location for quality.</span></span>

1. <span data-ttu-id="5f20e-253">Zvolte **OK** a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5f20e-253">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5f20e-254">Nyní je nutné změnit pořadí existujících direktiv umístění pro sklad *51*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-254">You must now change the sequence of purchase order location directives for warehouse *51*.</span></span> <span data-ttu-id="5f20e-255">Uložte novou direktivu umístění *51 do kvality*, aktualizujte stránku a v seznamu vyberte direktivu o umístění.</span><span class="sxs-lookup"><span data-stu-id="5f20e-255">Save the new *51 To Quality* location directive, refresh the page, and select the location directive in the list.</span></span> <span data-ttu-id="5f20e-256">Potom v podokně akcí pomocí tlačítka **posunout nahoru** a **Posunout dolů** umístěte direktivu umístění pro sklad *51* v následujícím pořadí.</span><span class="sxs-lookup"><span data-stu-id="5f20e-256">Then use the **Move up** and **Move down** buttons on the Action Pane to put the location directive for warehouse *51* in the following order.</span></span> <span data-ttu-id="5f20e-257">(Před výběrem **Posunout nahoru** nebo **Posunout dolů** musíte v seznamu vybrat direktivu o umístění.)</span><span class="sxs-lookup"><span data-stu-id="5f20e-257">(Before you select **Move up** or **Move down**, you must select a location directive in the list.)</span></span>

    1. <span data-ttu-id="5f20e-258">51 Do kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-258">51 To Quality</span></span>
    2. <span data-ttu-id="5f20e-259">51 PO Direct</span><span class="sxs-lookup"><span data-stu-id="5f20e-259">51 PO Direct</span></span>
    3. <span data-ttu-id="5f20e-260">51 QMS</span><span class="sxs-lookup"><span data-stu-id="5f20e-260">51 QMS</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="5f20e-261">Položky nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="5f20e-261">Mobile device menu items</span></span>

<span data-ttu-id="5f20e-262">Nakonfigurujte položku nabídky tak, aby mobilní zařízení mohla provádět funkci **Kontrola kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-262">Configure a menu item so that mobile devices can perform the **Quality Check** function.</span></span>

#### <a name="purchase-putaway"></a><span data-ttu-id="5f20e-263">Výdej nákupu</span><span class="sxs-lookup"><span data-stu-id="5f20e-263">Purchase putaway</span></span>

1. <span data-ttu-id="5f20e-264">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-264">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5f20e-265">V seznamu vyberte položku nabídky mobilního zařízení **Nákupní vyskladnění**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-265">In the list, select the **Purchase put-away** menu item.</span></span>
1. <span data-ttu-id="5f20e-266">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-266">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5f20e-267">V části **Pracovní třídy** přidejte řádek do mřížky výběrem možnosti **Nová**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-267">In the **Work classes** section, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="5f20e-268">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-268">In the new row, set the following values:</span></span>

    - <span data-ttu-id="5f20e-269">**ID pracovní třídy:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-269">**Work class ID:** *QC Check*</span></span>

        <span data-ttu-id="5f20e-270">Zadejte název [pracovní třídy](#work-class), který jste dříve vytvořili pro práci s kontrolou kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-270">Enter the name of the [work class](#work-class) that you created earlier for quality control work.</span></span>

    - <span data-ttu-id="5f20e-271">**Typ pracovního příkazu:** *Kontrola kvality*</span><span class="sxs-lookup"><span data-stu-id="5f20e-271">**Work order type:** *Quality in quality check*</span></span>

1. <span data-ttu-id="5f20e-272">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-272">On the Action Pane, select **Save**.</span></span>

#### <a name="purchase-order-line-receiving"></a><span data-ttu-id="5f20e-273">Přijetí řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="5f20e-273">Purchase order line receiving</span></span>

1. <span data-ttu-id="5f20e-274">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-274">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5f20e-275">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-275">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f20e-276">V záhlaví nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-276">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f20e-277">**Název položky nabídky:** *Příjem řádku PO*</span><span class="sxs-lookup"><span data-stu-id="5f20e-277">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="5f20e-278">**Název:** *Příjem řádku PO*</span><span class="sxs-lookup"><span data-stu-id="5f20e-278">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="5f20e-279">**Režim:** *Práce*</span><span class="sxs-lookup"><span data-stu-id="5f20e-279">**Mode:** *Work*</span></span>
    - <span data-ttu-id="5f20e-280">**Použít existující práci:** *Ne*</span><span class="sxs-lookup"><span data-stu-id="5f20e-280">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="5f20e-281">Na záložce s náhledem **Obecné** nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="5f20e-281">On the **General** FastTab, set the following values.</span></span> <span data-ttu-id="5f20e-282">Potvrďte výchozí hodnoty ve všech zbývajících polích.</span><span class="sxs-lookup"><span data-stu-id="5f20e-282">Accept the default values for the remaining fields.</span></span>

    - <span data-ttu-id="5f20e-283">**Proces tvorby práce:** *Příjem a vyskladnění řádku nákupní objednávky*</span><span class="sxs-lookup"><span data-stu-id="5f20e-283">**Work creation process:** *Purchase order line receiving and put away*</span></span>
    - <span data-ttu-id="5f20e-284">**Generovat registrační značky:** *Ano*</span><span class="sxs-lookup"><span data-stu-id="5f20e-284">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="5f20e-285">**Pracovní šablona:** *51 Příjemka NO*</span><span class="sxs-lookup"><span data-stu-id="5f20e-285">**Work template:** *51 PO Receipt*</span></span>

1. <span data-ttu-id="5f20e-286">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-286">On the Action Pane, select **Save**.</span></span>

#### <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="5f20e-287">Přidání položky nabídky do nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="5f20e-287">Add the menu item to a mobile device menu</span></span>

1. <span data-ttu-id="5f20e-288">Přejděte do **Řízení skladu \> Nastavení \> Mobilní zařízení \> Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-288">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="5f20e-289">V levém podokně vyberte nabídku **Příchozí**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-289">In the left pane, select the **Inbound** menu.</span></span>
1. <span data-ttu-id="5f20e-290">V podokně akcí vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-290">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5f20e-291">Ve sloupci **Dostupné nabídky a položky nabídky** najděte a vyberte novou položku nabídky **Příjem řádku PO**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-291">In the **Available menus and menu items** column, select the new **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="5f20e-292">Stisknutím tlačítka se šipkou doprava přesuňte **Příjem řádku NO** do sloupce **Struktura nabídky**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-292">Select the right arrow button to move **PO line receiving** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="5f20e-293">Ve sloupci **Struktura nabídky** vyberte **Příjem řádku PO** a poté pomocí tlačítka se šipkou nahoru nebo dolů přesuňte položku nabídky na požadovanou pozici v nabídce mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="5f20e-293">In the **Menu structure** column, select **PO line receiving**, and then select the up arrow or down arrow button to move the menu item to the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="5f20e-294">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-294">On the Action Pane, select **Save**.</span></span>

## <a name="example-scenario"></a><a name="example-scenario"></a><span data-ttu-id="5f20e-295">Příklad</span><span class="sxs-lookup"><span data-stu-id="5f20e-295">Example scenario</span></span>

<span data-ttu-id="5f20e-296">Po zpřístupnění a nastavení všech výše popsaných vzorových dat můžete v rámci tohoto scénáře vyzkoušet funkci *Kontrola kvality*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-296">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Quality check* feature.</span></span> <span data-ttu-id="5f20e-297">Hodnoty zobrazené v tomto scénáři předpokládají, že pracujete se standardními ukázkovými daty, která jste vybrali v právnické osobě **USMF** a připravili jste vzorové záznamy, které jsou popsány dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-297">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="5f20e-298">Tento scénář také slouží jako příklad, který ukazuje, jak lze funkci použít v produkčním nastavení.</span><span class="sxs-lookup"><span data-stu-id="5f20e-298">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="5f20e-299">Vytvoření nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="5f20e-299">Create a purchase order</span></span>

1. <span data-ttu-id="5f20e-300">Přejděte na **Zásobování a zdroje \> Nákupní objednávky \> Všechny nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-300">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="5f20e-301">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-301">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f20e-302">V dialogovém okně **Vytvoření nákupní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-302">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5f20e-303">**Účet dodavatele:** *104*</span><span class="sxs-lookup"><span data-stu-id="5f20e-303">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="5f20e-304">**Sklad:** *51*</span><span class="sxs-lookup"><span data-stu-id="5f20e-304">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="5f20e-305">Vyberte **OK** - nová prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="5f20e-305">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="5f20e-306">Na pevné záložce **Řádky prodejní objednávky** obsahuje mřížka nový prázdný řádek.</span><span class="sxs-lookup"><span data-stu-id="5f20e-306">On the **Purchase order lines** FastTab, the grid contains a new, blank line.</span></span> <span data-ttu-id="5f20e-307">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="5f20e-307">On this line, set the following values:</span></span>

    - <span data-ttu-id="5f20e-308">**Číslo položky:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="5f20e-308">**Item number:** *M9203*</span></span>
    - <span data-ttu-id="5f20e-309">**Množství:** *3*</span><span class="sxs-lookup"><span data-stu-id="5f20e-309">**Quantity:** *3*</span></span>
    - <span data-ttu-id="5f20e-310">**Jednotka:** *PL*</span><span class="sxs-lookup"><span data-stu-id="5f20e-310">**Unit:** *PL*</span></span>

1. <span data-ttu-id="5f20e-311">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-311">On the Action Pane, select **Save**.</span></span>

### <a name="process-quality-check-receiving"></a><span data-ttu-id="5f20e-312">Zpracování příjmu kontroly kvality</span><span class="sxs-lookup"><span data-stu-id="5f20e-312">Process quality check receiving</span></span>

<span data-ttu-id="5f20e-313">Po vytvoření nákupní objednávky ji můžete obdržet pomocí položky nabídky **Příjem řádku PO** a funkčnosti funkce *Kontrola kvality*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-313">After the purchase order has been created, it can be received by using the **PO line receiving** menu item and the functionality of the *Quality check* feature.</span></span>

#### <a name="receive-pallet-1"></a><span data-ttu-id="5f20e-314">Příjem palety 1</span><span class="sxs-lookup"><span data-stu-id="5f20e-314">Receive pallet 1</span></span>

1. <span data-ttu-id="5f20e-315">Přihlaste se do skladové aplikace jako uživatel skladu *51*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-315">Sign in to the warehouse app as a user for warehouse *51*.</span></span> <span data-ttu-id="5f20e-316">(Zadejte *51* jako ID uživatele a *1* jako heslo.)</span><span class="sxs-lookup"><span data-stu-id="5f20e-316">(Enter *51* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="5f20e-317">Jděte na **Příchozí \> Příjem řádku PO**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-317">Go to **Inbound \> PO line receiving**.</span></span>
1. <span data-ttu-id="5f20e-318">V poli **PONUM** zadejte číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-318">In the **PONUM** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="5f20e-319">Potvrďte znovu číslo nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-319">Confirm the purchase order number.</span></span>
1. <span data-ttu-id="5f20e-320">Do pole **LINENUM** zadejte číslo řádku z nákupní objednávky, kterou přijímáte.</span><span class="sxs-lookup"><span data-stu-id="5f20e-320">In the **LINENUM** field, enter the number of the purchase order line that is being received.</span></span> <span data-ttu-id="5f20e-321">Protože objednávka má v tomto scénáři pouze jeden řádek, zadáte *1* v poli **LINENUM** pro každý krok příjmu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-321">Because the order has only one line in this scenario, you will enter *1* in the **LINENUM** field for each receiving step.</span></span>
1. <span data-ttu-id="5f20e-322">Potvrďte číslo řádku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-322">Confirm the line number.</span></span>
1. <span data-ttu-id="5f20e-323">Do pole **QTY** zadejte množství pro přijetí.</span><span class="sxs-lookup"><span data-stu-id="5f20e-323">In the **QTY** field, enter the quantity to receive.</span></span> <span data-ttu-id="5f20e-324">Protože objednávka platí pro tři palety (*PL*) v tomto scénáři a existují tři kroky příjmu, zadáte hodnotu *1* do pole **QTY** pro každý krok příjmu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-324">Because the purchase order is for three pallets (*PL*) in this scenario, and there are three receiving steps, you will enter *1* in the **QTY** field for each receiving step.</span></span>
1. <span data-ttu-id="5f20e-325">Potvrďte množství.</span><span class="sxs-lookup"><span data-stu-id="5f20e-325">Confirm the quantity.</span></span>

    <span data-ttu-id="5f20e-326">Stránka **Kontrola kvality**, která se objeví, nemá žádná vstupní pole.</span><span class="sxs-lookup"><span data-stu-id="5f20e-326">The **Quality check** page that appears has no entry fields.</span></span> <span data-ttu-id="5f20e-327">Ve spodní části je pouze potvrzovací tlačítko (znak zaškrtnutí) a tlačítko Nabídka (**≡**) nahoře.</span><span class="sxs-lookup"><span data-stu-id="5f20e-327">It has only the confirmation (check mark) button at the bottom and the Menu button (**≡**) at the top.</span></span> <span data-ttu-id="5f20e-328">(Tlačítko Nabídka se někdy označuje jako hamburger nebo hamburgerové tlačítko.) Pro urychlení procesu kontroly kvality, když paleta projde kontrolou kvality, uživatel pouze potvrdí stránku **Kontrola kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-328">(The Menu button is sometimes referred to as the hamburger or the hamburger button.) To expedite the quality check process, when the pallet passes the quality check, the user just confirms the **Quality check** page.</span></span>

    <span data-ttu-id="5f20e-329">![Stránka Kontrola kvality](media/quality-check.png "Stránka Kontrola kvality")</span><span class="sxs-lookup"><span data-stu-id="5f20e-329">![Quality check page](media/quality-check.png "Quality check page")</span></span>

1. <span data-ttu-id="5f20e-330">Vyberte potvrzovací tlačítko a předejte kontrolu kvality palety 1 z řádku 1.</span><span class="sxs-lookup"><span data-stu-id="5f20e-330">Select the confirmation button to pass the quality check for pallet 1 from line 1.</span></span>

    <span data-ttu-id="5f20e-331">Stránka **Objednávky: Vložit**, která se objeví, zobrazuje podrobnosti o práci vložení:</span><span class="sxs-lookup"><span data-stu-id="5f20e-331">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="5f20e-332">**LOC:** Systém určil umístění</span><span class="sxs-lookup"><span data-stu-id="5f20e-332">**LOC:** The system determined location</span></span>

        <span data-ttu-id="5f20e-333">Toto místo je určeným místem výdeje pro příjem nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-333">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="5f20e-334">**LP:** Systémem generované ID poznávací značky</span><span class="sxs-lookup"><span data-stu-id="5f20e-334">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="5f20e-335">**Položka:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="5f20e-335">**Item:** *M9203*</span></span>
    - <span data-ttu-id="5f20e-336">**Množství:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="5f20e-336">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="5f20e-337">Zobrazí se také popis položky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-337">The item description is also shown.</span></span>

1. <span data-ttu-id="5f20e-338">Potvrďte práci zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="5f20e-338">Confirm the putaway work.</span></span>

    <span data-ttu-id="5f20e-339">Na stránce **Úkol** pro přijetí řádku objednávky obdržíte zprávu „Dokončena práce“.</span><span class="sxs-lookup"><span data-stu-id="5f20e-339">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5f20e-340">Pole **LINENUM** je k dispozici, takže můžete začít přijímat další paletu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-340">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

#### <a name="receive-pallet-2"></a><span data-ttu-id="5f20e-341">Příjem palety 2</span><span class="sxs-lookup"><span data-stu-id="5f20e-341">Receive pallet 2</span></span>

<span data-ttu-id="5f20e-342">U tohoto scénáře bude paleta 2 odmítnuta.</span><span class="sxs-lookup"><span data-stu-id="5f20e-342">For this scenario, pallet 2 will be rejected.</span></span>

1. <span data-ttu-id="5f20e-343">V poli **LINENUM** zadejte *1* a potvrďte číslo řádku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-343">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="5f20e-344">Pole **QTY** je nyní k dispozici.</span><span class="sxs-lookup"><span data-stu-id="5f20e-344">The **QTY** field is now available.</span></span> <span data-ttu-id="5f20e-345">Zadejte *1* a potvrďte množství.</span><span class="sxs-lookup"><span data-stu-id="5f20e-345">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="5f20e-346">Zobrazí se stránka **Kontrola kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-346">The **Quality check** page appears.</span></span> <span data-ttu-id="5f20e-347">Pro tento příjem bude paleta odmítnuta z hlediska kvality a bude vložena do umístění kvality *QMS*.</span><span class="sxs-lookup"><span data-stu-id="5f20e-347">For this receipt, the pallet will be rejected for quality, and it will be put into the *QMS* quality location.</span></span>

1. <span data-ttu-id="5f20e-348">Vyberte tlačítko Nabídka (**≡**) v horní části stránky a poté v nabídce vyberte možnost **Odmítnout**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-348">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Reject**.</span></span>
1. <span data-ttu-id="5f20e-349">Na stránce **Úkol**, která se zobrazí, zadejte **QMS** jako místo *vložení* pro odeslání palety k další kontrole.</span><span class="sxs-lookup"><span data-stu-id="5f20e-349">On the **Task** page that appears, enter **QMS** as the *Put* location to send the pallet to for further inspection.</span></span>

    <span data-ttu-id="5f20e-350">Stránka **Kvalita v kontrole kvality: Vložit**, která se objeví, zobrazuje podrobnosti o práci vložení:</span><span class="sxs-lookup"><span data-stu-id="5f20e-350">The **Quality in quality check: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="5f20e-351">**LOC:** *QMS*</span><span class="sxs-lookup"><span data-stu-id="5f20e-351">**LOC:** *QMS*</span></span>

        <span data-ttu-id="5f20e-352">Toto místo je určeným místem výdeje pro příjem odmítnuté kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-352">This location is the designated putaway location for rejected quality receiving.</span></span>

    - <span data-ttu-id="5f20e-353">**LP:** Systémem generované ID poznávací značky</span><span class="sxs-lookup"><span data-stu-id="5f20e-353">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="5f20e-354">**Položka:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="5f20e-354">**Item:** *M9203*</span></span>
    - <span data-ttu-id="5f20e-355">**Množství:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="5f20e-355">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="5f20e-356">Zobrazí se také popis položky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-356">The item description is also shown.</span></span>

1. <span data-ttu-id="5f20e-357">Potvrďte práci zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="5f20e-357">Confirm the putaway work.</span></span>

    <span data-ttu-id="5f20e-358">Na stránce **Úkol** pro přijetí řádku objednávky obdržíte zprávu „Dokončena práce“.</span><span class="sxs-lookup"><span data-stu-id="5f20e-358">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5f20e-359">Pole **LINENUM** je k dispozici, takže můžete začít přijímat další paletu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-359">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

<span data-ttu-id="5f20e-360">Nyní jste dokončili kontrolu kvality a vytvořili jste objednávku kvality pro odmítnutou paletu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-360">You've now completed the quality check and created a quality order for the rejected pallet.</span></span> <span data-ttu-id="5f20e-361">Chcete-li zobrazit vytvořenou objednávku kvality, přejděte na **Řízení zásob \> Periodické úkoly \> Řízení kvality \> Objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-361">To view the order that was created, go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>

<span data-ttu-id="5f20e-362">Testování objednávky kvality je nyní možné zpracovat.</span><span class="sxs-lookup"><span data-stu-id="5f20e-362">Quality order testing can now be processed.</span></span> <span data-ttu-id="5f20e-363">V tomto tématu není zahrnuto testování kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-363">Quality testing isn't covered in this topic.</span></span>

<span data-ttu-id="5f20e-364">Další informace o řízení kvality naleznete v tématu [Přehled řízení kvality](../inventory/enable-quality-management.md).</span><span class="sxs-lookup"><span data-stu-id="5f20e-364">For more information about quality management, see [Quality management overview](../inventory/enable-quality-management.md)</span></span>

#### <a name="receive-pallet-3"></a><span data-ttu-id="5f20e-365">Příjem palety 3</span><span class="sxs-lookup"><span data-stu-id="5f20e-365">Receive pallet 3</span></span>

<span data-ttu-id="5f20e-366">U tohoto scénáře bude paleta 3 přijata.</span><span class="sxs-lookup"><span data-stu-id="5f20e-366">For this scenario, pallet 3 will be accepted.</span></span>

1. <span data-ttu-id="5f20e-367">V poli **LINENUM** zadejte *1* a potvrďte číslo řádku.</span><span class="sxs-lookup"><span data-stu-id="5f20e-367">In the **LINENUM** field, enter *1*, and confirm the line number.</span></span>
1. <span data-ttu-id="5f20e-368">Pole **QTY** je nyní k dispozici.</span><span class="sxs-lookup"><span data-stu-id="5f20e-368">The **QTY** field is now available.</span></span> <span data-ttu-id="5f20e-369">Zadejte *1* a potvrďte množství.</span><span class="sxs-lookup"><span data-stu-id="5f20e-369">Enter *1*, and confirm the quantity.</span></span>

    <span data-ttu-id="5f20e-370">Zobrazí se stránka **Kontrola kvality**.</span><span class="sxs-lookup"><span data-stu-id="5f20e-370">The **Quality check** page appears.</span></span> <span data-ttu-id="5f20e-371">Pro tento příjem bude paleta přijata z hlediska kvality a bude vložena do umístění hromadného výdeje.</span><span class="sxs-lookup"><span data-stu-id="5f20e-371">For this receipt, the pallet will be accepted for quality, and it will be put into a bulk putaway location.</span></span>

1. <span data-ttu-id="5f20e-372">Vyberte potvrzovací tlačítko pro předání kontroly kvality.</span><span class="sxs-lookup"><span data-stu-id="5f20e-372">Select the confirmation button to pass the quality check.</span></span>

    <span data-ttu-id="5f20e-373">Stránka **Objednávky: Vložit**, která se objeví, zobrazuje podrobnosti o práci vložení:</span><span class="sxs-lookup"><span data-stu-id="5f20e-373">The **Purchase orders: Put** page that appears shows details of the put work:</span></span>

    - <span data-ttu-id="5f20e-374">**LOC:** Systém určil umístění</span><span class="sxs-lookup"><span data-stu-id="5f20e-374">**LOC:** The system determined location</span></span>

        <span data-ttu-id="5f20e-375">Toto místo je určeným místem výdeje pro příjem nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-375">This location is the designated putaway location for purchase order receiving.</span></span>

    - <span data-ttu-id="5f20e-376">**LP:** Systémem generované ID poznávací značky</span><span class="sxs-lookup"><span data-stu-id="5f20e-376">**LP:** The system-generated License plate ID</span></span>
    - <span data-ttu-id="5f20e-377">**Položka:** *M9203*</span><span class="sxs-lookup"><span data-stu-id="5f20e-377">**Item:** *M9203*</span></span>
    - <span data-ttu-id="5f20e-378">**Množství:** *1 PL: 100 ea*</span><span class="sxs-lookup"><span data-stu-id="5f20e-378">**Qty:** *1 PL: 100 ea*</span></span>

    <span data-ttu-id="5f20e-379">Zobrazí se také popis položky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-379">The item description is also shown.</span></span>

1. <span data-ttu-id="5f20e-380">Potvrďte práci zaskladnění.</span><span class="sxs-lookup"><span data-stu-id="5f20e-380">Confirm the putaway work.</span></span>

    <span data-ttu-id="5f20e-381">Na stránce **Úkol** pro přijetí řádku objednávky obdržíte zprávu „Dokončena práce“.</span><span class="sxs-lookup"><span data-stu-id="5f20e-381">On the **Task** page for purchase order line receiving, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5f20e-382">Pole **LINENUM** je k dispozici, takže můžete začít přijímat další paletu.</span><span class="sxs-lookup"><span data-stu-id="5f20e-382">The **LINENUM** field is available so that you can start to receive the next pallet.</span></span>

1. <span data-ttu-id="5f20e-383">Vyberte tlačítko Nabídka (**≡**) v horní části stránky a poté v nabídce vyberte možnost **Zrušit** pro návrat do nabídky.</span><span class="sxs-lookup"><span data-stu-id="5f20e-383">Select the Menu button (**≡**) at the top of the page, and then, on the menu, select **Cancel** to return to the menu.</span></span>

<span data-ttu-id="5f20e-384">Nyní můžete mobilní aplikaci zavřít.</span><span class="sxs-lookup"><span data-stu-id="5f20e-384">You can now close the mobile app.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]