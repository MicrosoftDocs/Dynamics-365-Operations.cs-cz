---
title: "Nastavení skladu s použitím šablony konfigurace skladu"
description: "Toto téma vysvětluje nastavení skladu s použitím šablony konfigurace skladu."
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 90a4276f261affd8c90f2deb7cd0b773d43e5485
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="c8d6a-103">Nastavení skladu s použitím šablony konfigurace skladu</span><span class="sxs-lookup"><span data-stu-id="c8d6a-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c8d6a-104">Toto téma vysvětluje nastavení skladu s použitím šablony konfigurace skladu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="c8d6a-105">Existuje několik předdefinovaných šablon konfigurace, které lze použít.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="c8d6a-106">Další informace o použití hodnot těchto šablon naleznete v tématu [Šablony dat konfigurací](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c8d6a-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="c8d6a-107">Scénáře, které mohou být šablony konfigurací užitečné</span><span class="sxs-lookup"><span data-stu-id="c8d6a-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="c8d6a-108">Šablony konfigurací mohou být užitečné v mnoha scénářích.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="c8d6a-109">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="c8d6a-109">Here are some examples:</span></span>

- <span data-ttu-id="c8d6a-110">Dokončili jste a otestovali nastavení konfigurace v testovacím prostředí a nyní chcete kopírovat nastavení do provozního prostředí.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="c8d6a-111">Chcete zavést nastavení skladu pro více právnických osob nebo vytvořit nový sklad ve stejné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="c8d6a-112">Chcete se rychle připravit na ukázku funkcí skladu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="c8d6a-113">Chcete, aby existující položky a sklady používaly funkce v modulu Řízení skladu namísto funkce v modulu Řízení zásob.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="c8d6a-114">Toto téma se zaměřuje na první z těchto scénářů.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="c8d6a-115">Ukazuje použití šablony konfigurace pro zkopírování nastavení konfigurace z testovacího prostředí do provozního prostředí.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="c8d6a-116">Kopírování nastavení konfigurace z testovacího prostředí do provozního prostředí</span><span class="sxs-lookup"><span data-stu-id="c8d6a-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="c8d6a-117">V tomto scénáři již existují v testovacím prostředí nastavení konfigurace pro sklad a některé procesy transakce.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="c8d6a-118">Nyní chcete kopírovat nastavení konfigurace pro sklad z testovacího prostředí do provozního prostředí.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="c8d6a-119">Je důležité, abyste zahrnuli další související data nastavení při kopírování nastavení konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="c8d6a-120">Chcete například nastavit produkty zkopírováním nastavení z testovacího prostředí.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="c8d6a-121">Nelze však nastavit pevně stanovené výdejní skladové místo pro produkt před vytvořením produktu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="c8d6a-122">Ačkoliv jednotlivé šablony konfigurace nepodporují tento typ závislosti, existují výchozí šablony dat, které ho podporují.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="c8d6a-123">Tyto výchozí šablony dat lze snadno zahrnout do procesu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="c8d6a-124">Export výchozí šablony skladu</span><span class="sxs-lookup"><span data-stu-id="c8d6a-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="c8d6a-125">Otevřete pracovní prostor **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8d6a-126">Pokud používáte tento pracovní prostor poprvé, je nutné načíst všechny entity dat předtím, než budete pokračovat.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="c8d6a-127">Vyberte dlaždici **Šablony** a poté vyberte **Načíst výchozí šablony** pro načtení výchozích šablon.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8d6a-128">Možnost **Načíst výchozí šablony** je dostupné pouze v zobrazení **Rozšířené**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="c8d6a-129">Vyberte **Parametry architektury**a poté v poli **Zobrazit výchozí** vyberte **Rozšířené zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="c8d6a-130">Poté, co jsou načteny výchozí šablony, je lze změnit tak, aby splňovaly vaše obchodní požadavky.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8d6a-131">Abyste mohli načíst výchozí šablony a importovat je, musíte mít přístup správce systému.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="c8d6a-132">Tento požadavek pomáhá zaručit, že se všechny šablony načtou do šablony správně.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="c8d6a-133">Ujistěte se, že se nacházíte v právnické osobě, ze které chcete exportovat data specifická pro společnost.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="c8d6a-134">V pracovním prostoru vyberte **Exportovat**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="c8d6a-135">Vytvořte nový projekt exportu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-135">Create a new export project.</span></span>
7. <span data-ttu-id="c8d6a-136">Vyberte **+ Přidat šablonu**a vyhledejte výchozí šablonu skladu **400 - WMS**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="c8d6a-137">Tato šablona přidá entity dat pro konfiguraci skladu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8d6a-138">Je-li nutné filtrovat exportovaná data (například chcete exportovat pouze data, která souvisí s určitým skladem), je nutné vyhodnotit každou datovou entitu a přidat filtrování pomocí dotazu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="c8d6a-139">Případně můžete exportovat všechna data a potom odstranit záznamy, které nejsou vyžadovány v cílových souborech.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="c8d6a-140">Vyberte **Export**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-140">Select **Export**.</span></span> <span data-ttu-id="c8d6a-141">Jsou exportována data, která se vztahují ke všem datovým entitám v projektu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="c8d6a-142">U datového balíčku můžete stáhnout soubor ZIP.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="c8d6a-143">Tento soubor obsahuje všechna data ve vybraném formátu (například formát aplikace Excel).</span><span class="sxs-lookup"><span data-stu-id="c8d6a-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="c8d6a-144">Jak bylo zmíněno, některé záznamy v souborech datových balíčků může být zapotřebí aktualizovat před jejich importem do provozního prostředí.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="c8d6a-145">Při aktualizaci záznamu se ujistěte se, že nezměníte název souboru.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="c8d6a-146">Import nastavení konfigurace skladu</span><span class="sxs-lookup"><span data-stu-id="c8d6a-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="c8d6a-147">V cílovém prostředí se ujistěte, že se nacházíte ve společnosti, do které chcete importovat data skladu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c8d6a-148">Před provedením importu je nutné určit závislosti dat.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="c8d6a-149">Například šablona **Řízení skladu** obsahuje datovou entitu s názvem **Dispoziční kódy skladu**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="c8d6a-150">Tato entita obsahuje data, která souvisí s nastavením stránky **Dispoziční kódy** (**Řízení skladu** > **Nastavení** > **Mobilní zařízení** > **Dispoziční kódy**).</span><span class="sxs-lookup"><span data-stu-id="c8d6a-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="c8d6a-151">Pokud již existující nastavení zpracovává proces vrácení prodejních objednávek , pole **Vrátit dispoziční kód** obsahuje hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="c8d6a-152">Dispoziční kód v tomto poli se vztahuje k datové entitě **Dispoziční kód**, která je součástí šablony **Prodeje a marketing**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="c8d6a-153">Pokud data z datové entity **Dispoziční kód** nejsou importována dříve než data z pole **Dispoziční kódy skladu**, import se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="c8d6a-154">V pracovním prostoru **Správa dat** vyberte **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="c8d6a-155">Vytvořte nový projekt importu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-155">Create a new import project.</span></span>
4. <span data-ttu-id="c8d6a-156">Vyberte **+ Přidat soubor**a odešlete soubor ZIP pro datový balíček.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="c8d6a-157">Vyberte **Import**.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-157">Select **Import**.</span></span> <span data-ttu-id="c8d6a-158">V zobrazení **Rozšířené** můžete použít možnost **Filtr**, abyste rychle získali přehled o problémech, které mohou nastat během importu.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="c8d6a-159">Možnost **Zobrazit protokol provádění** obsahuje podrobné informace o každé datové entitě, která je importována.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="c8d6a-160">Můžete použít zobrazení dat fázování, abyste se dostali rychle k cílovým datům.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="c8d6a-161">V takovém případě se zobrazí, jak vypadají importovaná data na souvisejících stránkách v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="c8d6a-162">Při použití výchozích datových šablon pracuje pořadí importu pro každou datovou entitu předem definovaným způsobem, aby se zajistilo, že všechna závislá data budou importována nejdříve.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="c8d6a-163">Jsou-li vlastní datové entity součástí projektu, je třeba zkontrolovat, že je definováno správné pořadí.</span><span class="sxs-lookup"><span data-stu-id="c8d6a-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="c8d6a-164">Další informace naleznete v tématu[Šablony dat konfigurací](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="c8d6a-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="related-topic"></a><span data-ttu-id="c8d6a-165">Související téma</span><span class="sxs-lookup"><span data-stu-id="c8d6a-165">Related topic</span></span>

[<span data-ttu-id="c8d6a-166">Šablony dat konfigurací</span><span class="sxs-lookup"><span data-stu-id="c8d6a-166">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)

