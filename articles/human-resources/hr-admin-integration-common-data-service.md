---
title: Konfigurace integrace Common Data Service
description: Integraci mezi Common Data Service a instanci Microsoft Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat entitu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008328"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="6bbf7-104">Konfigurace integrace Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6bbf7-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="6bbf7-105">Integraci mezi Common Data Service a instanci Microsoft Dynamics 365 Human Resources můžete zapnout nebo vypnout.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="6bbf7-106">Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat entitu.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="6bbf7-107">Když vypnete integraci, uživatelé mohou provádět změny v Human Resources nebo Common Data Service, ale tyto změny se mezi oběma prostředími nesynchronizují.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="6bbf7-108">Ve výchozím nastavení je integrace mezi Human Resources a Common Data Service vypnuta nebo zapnuta, v závislosti na přítomnosti ukázkových dat v prostředí:</span><span class="sxs-lookup"><span data-stu-id="6bbf7-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="6bbf7-109">**Vypnuta** pro nová prostředí, která nezahrnují ukázková data</span><span class="sxs-lookup"><span data-stu-id="6bbf7-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="6bbf7-110">**Zapnuta** pro nová prostředí, která zahrnují ukázková data</span><span class="sxs-lookup"><span data-stu-id="6bbf7-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="6bbf7-111">Nová prostředí, která zahrnují ukázková data, začnou synchronizovat data při jejich zřizování.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="6bbf7-112">V těchto situacích je vhodné vypnout integraci:</span><span class="sxs-lookup"><span data-stu-id="6bbf7-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="6bbf7-113">Vyplňujete data prostřednictvím Data Management Framework a je nutné je importovat vícekrát, aby je bylo možné dostat do správného stavu.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="6bbf7-114">Existují problémy s daty v modulu Human Resources nebo Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="6bbf7-115">Pokud vypnete integraci, můžete odstranit záznam v jednom prostředí, aniž byste ho odstranili v jiném.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="6bbf7-116">Pokud opět zapnete integraci, bude záznam v prostředí, kde nebyl odstraněn, synchronizován zpět do prostředí, ve kterém byl odstraněn.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="6bbf7-117">Synchronizace začíná při příštím spuštění dávkové úlohy **Integrace Common Data Service zmeškala synchronizaci požadavku**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="6bbf7-118">Když vypnete integraci dat, ujistěte se, že neupravujete stejný záznam v obou prostředích.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="6bbf7-119">Pokud zapnete integraci znovu, bude naposledy upravený záznam synchronizován.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="6bbf7-120">Pokud tedy neprovedete stejné změny v záznamu v obou prostředích, může dojít ke ztrátě dat.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="6bbf7-121">Přístup na stránku integrace Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6bbf7-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="6bbf7-122">V instanci Human Resources, v níž chcete zobrazit nebo konfigurovat nastavení pro integraci s Common Data Service, vyberte dlaždici **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="6bbf7-123">[![Dlaždice správy systému](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="6bbf7-124">Zvolte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="6bbf7-125">[![Karta Odkazy](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="6bbf7-126">V části **Integrace** vyberte **Konfigurace Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="6bbf7-127">[![Odkaz na konfiguraci Common Data Service](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="6bbf7-128">Zapnutí a vypnutí integrace dat mezi Human Resources a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6bbf7-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="6bbf7-129">Chcete-li zapnout integraci, nastavte možnost **Povolit integraci do Common Data Service** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6bbf7-130">Při zapnutí integrace budou data synchronizována při příštím spuštění dávkové úlohy **Integrace Common Data Service zmeškala synchronizaci požadavku**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="6bbf7-131">Všechna data by měla být k dispozici po dokončení dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="6bbf7-132">Chcete-li vypnout integraci, nastavte možnost na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="6bbf7-133">[![Zapnutí a vypnutí integrace Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="6bbf7-134">Zobrazení podrobností integrace dat</span><span class="sxs-lookup"><span data-stu-id="6bbf7-134">View data integration details</span></span>

<span data-ttu-id="6bbf7-135">Na záložce s náhledem **Správa** na stránce **Integrace Common Data Service** můžete zobrazit, jak budou záznamy vzájemně propojeny mezi Human Resources a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="6bbf7-136">Chcete-li zobrazit záznamy pro entitu, vyberte entitu v poli **Název entity CDS**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="6bbf7-137">V mřížce jsou uvedeny všechny záznamy, které jsou propojeny s vybranou entitou.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="6bbf7-138">[![Zobrazení záznamů entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="6bbf7-139">V tuto chvíli nejsou uvedeny všechny entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="6bbf7-140">V mřížce se zobrazí pouze entity, které podporují použití vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="6bbf7-141">Nové entity jsou k dispozici prostřednictvím kontinuálního vydávání aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="6bbf7-142">Mřížka obsahuje následující pole:</span><span class="sxs-lookup"><span data-stu-id="6bbf7-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="6bbf7-143">**Název entity CDS** - název entity v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="6bbf7-144">**Odkaz entity CDS**- identifikátor používající Common Data Service k identifikaci záznamu.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="6bbf7-145">Tato hodnota je ekvivalentní hodnotě **RecId** Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="6bbf7-146">Identifikátor lze najít při otevření entity Common Data Service v aplikaci Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="6bbf7-147">**Název entity Human Resources** – entita, která naposledy synchronizovala data do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="6bbf7-148">Entita může mít buď předponu Common Data Service, nebo jinou předponu.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="6bbf7-149">**Odkaz na Human Resources** - hodnota **RecId**, která je přidružená k záznamu v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="6bbf7-150">**Byla odstraněna z CDS** – hodnota, která určuje, zda byl záznam odstraněn z Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="6bbf7-151">Odebrání přidružení záznamu v Human Resources z Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6bbf7-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="6bbf7-152">Pokud se setkáte s problémy při synchronizaci dat mezi Human Resources a Common Data Service, můžete je vyřešit vymazáním sledování a opakovanou synchronizací sledovací tabulky.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="6bbf7-153">Pokud přidružení odeberete a poté změníte nebo odstraníte záznam v Common Data Service, nebudou provedené změny synchronizovány do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="6bbf7-154">Pokud provedete změny v Human Resources, bude vytvořen nový záznam sledování a záznam bude aktualizován v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="6bbf7-155">Chcete-li odebrat přidružení záznamu mezi Human Resources. a Common Data Service, vyberte entitu v poli **Název entity CDS** a poté vyberte možnost **Vymazat informace o sledování**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="6bbf7-156">[![Vymazat informace o sledování](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="6bbf7-157">Chcete-li spustit úplnou synchronizaci entity po vymazání sledování, postupujte podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="6bbf7-158">Synchronizace entity mezi Human Resources a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6bbf7-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="6bbf7-159">Tento postup použijte v případě, že změnám z Common Data Service trvá příliš dlouho, než se projeví v Human Resources, nebo pokud je nutné aktualizovat tabulku sledování po vymazání sledování.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="6bbf7-160">Chcete-li spustit úplnou synchronizaci entity mezi Human Resources a Common Data Service, vyberte entitu v poli **Název entity CDS** a pak vyberte **Synchronizovat nyní**.</span><span class="sxs-lookup"><span data-stu-id="6bbf7-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="6bbf7-161">[![Spuštění úplné synchronizace](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="6bbf7-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


