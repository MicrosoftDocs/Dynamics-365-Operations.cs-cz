---
title: Konfigurovat integraci se službou Common Data Service
description: Integraci mezi Common Data Service a Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat entitu.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8cbead2961c4576a5394080aae2fec109bce3f10
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621297"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="cdb81-104">Konfigurovat integraci se službou Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cdb81-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="cdb81-105">Integraci mezi Common Data Service a Dynamics 365 Human Resources můžete zapnout nebo vypnout.</span><span class="sxs-lookup"><span data-stu-id="cdb81-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="cdb81-106">Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat entitu.</span><span class="sxs-lookup"><span data-stu-id="cdb81-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="cdb81-107">Když vypnete integraci, uživatelé mohou provádět změny v Human Resources nebo Common Data Service, ale tyto změny se mezi oběma prostředími nesynchronizují.</span><span class="sxs-lookup"><span data-stu-id="cdb81-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="cdb81-108">Ve výchozím nastavení je integrace dat mezi Human Resources a Common Data Service vypnuta.</span><span class="sxs-lookup"><span data-stu-id="cdb81-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="cdb81-109">V těchto situacích je vhodné vypnout integraci:</span><span class="sxs-lookup"><span data-stu-id="cdb81-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="cdb81-110">Vyplňujete data prostřednictvím Data Management Framework a je nutné je importovat vícekrát, aby je bylo možné dostat do správného stavu.</span><span class="sxs-lookup"><span data-stu-id="cdb81-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="cdb81-111">Existují problémy s daty v modulu Human Resources nebo Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="cdb81-112">Pokud vypnete integraci, můžete odstranit záznam v jednom prostředí, aniž byste ho odstranili v jiném.</span><span class="sxs-lookup"><span data-stu-id="cdb81-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="cdb81-113">Pokud opět zapnete integraci, bude záznam v prostředí, kde nebyl odstraněn, synchronizován zpět do prostředí, ve kterém byl odstraněn.</span><span class="sxs-lookup"><span data-stu-id="cdb81-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="cdb81-114">Synchronizace začíná při příštím spuštění dávkové úlohy **Integrace Common Data Service zmeškala synchronizaci požadavku**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="cdb81-115">Když vypnete integraci dat, ujistěte se, že neupravujete stejný záznam v obou prostředích.</span><span class="sxs-lookup"><span data-stu-id="cdb81-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="cdb81-116">Pokud zapnete integraci znovu, bude naposledy upravený záznam synchronizován.</span><span class="sxs-lookup"><span data-stu-id="cdb81-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="cdb81-117">Pokud tedy neprovedete stejné změny v záznamu v obou prostředích, může dojít ke ztrátě dat.</span><span class="sxs-lookup"><span data-stu-id="cdb81-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="cdb81-118">Přístup na stránku integrace Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cdb81-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="cdb81-119">V instanci Human Resources, v níž chcete zobrazit nebo konfigurovat nastavení pro integraci s Common Data Service, vyberte dlaždici **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="cdb81-120">[![Dlaždice správy systému](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="cdb81-121">Zvolte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="cdb81-122">[![Karta Odkazy](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="cdb81-123">V části **Integrace** vyberte **Konfigurace Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="cdb81-124">[![Odkaz na konfiguraci Common Data Service](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="cdb81-125">Zapnutí a vypnutí integrace dat mezi Human Resources a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cdb81-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="cdb81-126">Chcete-li zapnout integraci, nastavte možnost **Povolit integraci do Common Data Service** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cdb81-127">Při zapnutí integrace budou data synchronizována při příštím spuštění dávkové úlohy **Integrace Common Data Service zmeškala synchronizaci požadavku**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="cdb81-128">Všechna data by měla být k dispozici po dokončení dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="cdb81-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="cdb81-129">Chcete-li vypnout integraci, nastavte možnost na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="cdb81-130">[![Zapnutí a vypnutí integrace Common Data Service](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="cdb81-131">Důrazně doporučujeme vypnout integraci Common Data Service při provádění úkolů migrace dat.</span><span class="sxs-lookup"><span data-stu-id="cdb81-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="cdb81-132">Odesílání velkého objemu dat může výrazně ovlivnit výkon.</span><span class="sxs-lookup"><span data-stu-id="cdb81-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="cdb81-133">Například nahrávání 2000 pracovníků může trvat několik hodin, když je integrace povolena, a méně než jednu hodinu, pokud je zakázána.</span><span class="sxs-lookup"><span data-stu-id="cdb81-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="cdb81-134">Čísla uvedená v tomto příkladu slouží pouze k demonstračním účelům.</span><span class="sxs-lookup"><span data-stu-id="cdb81-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="cdb81-135">Přesné množství času potřebného k importu záznamů se může značně lišit v závislosti na mnoha faktorech.</span><span class="sxs-lookup"><span data-stu-id="cdb81-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="cdb81-136">Zobrazení podrobností integrace dat</span><span class="sxs-lookup"><span data-stu-id="cdb81-136">View data integration details</span></span>

<span data-ttu-id="cdb81-137">Na záložce s náhledem **Správa** na stránce **Integrace Common Data Service** můžete zobrazit, jak budou záznamy vzájemně propojeny mezi Human Resources a Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="cdb81-138">Chcete-li zobrazit záznamy pro entitu, vyberte entitu v poli **Název entity CDS**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="cdb81-139">V mřížce jsou uvedeny všechny záznamy, které jsou propojeny s vybranou entitou.</span><span class="sxs-lookup"><span data-stu-id="cdb81-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="cdb81-140">[![Zobrazení záznamů entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="cdb81-141">V tuto chvíli nejsou uvedeny všechny entity Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="cdb81-142">V mřížce se zobrazí pouze entity, které podporují použití vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="cdb81-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="cdb81-143">Nové entity jsou k dispozici prostřednictvím kontinuálního vydávání aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cdb81-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="cdb81-144">Mřížka obsahuje následující pole:</span><span class="sxs-lookup"><span data-stu-id="cdb81-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="cdb81-145">**Název entity CDS** - název entity v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="cdb81-146">**Odkaz entity CDS**- identifikátor používající Common Data Service k identifikaci záznamu.</span><span class="sxs-lookup"><span data-stu-id="cdb81-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="cdb81-147">Tato hodnota je ekvivalentní hodnotě **RecId** Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cdb81-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="cdb81-148">Identifikátor lze najít při otevření entity Common Data Service v aplikaci Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cdb81-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="cdb81-149">**Název entity Human Resources** – entita, která naposledy synchronizovala data do Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="cdb81-150">Entita může mít buď předponu Common Data Service, nebo jinou předponu.</span><span class="sxs-lookup"><span data-stu-id="cdb81-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="cdb81-151">**Odkaz na Human Resources** - hodnota **RecId**, která je přidružená k záznamu v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cdb81-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="cdb81-152">**Byla odstraněna z CDS** – hodnota, která určuje, zda byl záznam odstraněn z Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="cdb81-153">Odebrání přidružení záznamu v Human Resources z Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cdb81-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="cdb81-154">Pokud se setkáte s problémy při synchronizaci dat mezi Human Resources a Common Data Service, můžete je vyřešit vymazáním sledování a opakovanou synchronizací sledovací tabulky.</span><span class="sxs-lookup"><span data-stu-id="cdb81-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="cdb81-155">Pokud přidružení odeberete a poté změníte nebo odstraníte záznam v Common Data Service, nebudou provedené změny synchronizovány do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cdb81-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="cdb81-156">Pokud provedete změny v Human Resources, bude vytvořen nový záznam sledování a záznam bude aktualizován v Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cdb81-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="cdb81-157">Chcete-li odebrat přidružení záznamu mezi Human Resources. a Common Data Service, vyberte entitu v poli **Název entity CDS** a poté vyberte možnost **Vymazat informace o sledování**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="cdb81-158">[![Vymazat informace o sledování](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="cdb81-159">Chcete-li spustit úplnou synchronizaci entity po vymazání sledování, postupujte podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="cdb81-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="cdb81-160">Synchronizace entity mezi Human Resources a Common Data Service</span><span class="sxs-lookup"><span data-stu-id="cdb81-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="cdb81-161">Tento postup použijte v následujících případech:</span><span class="sxs-lookup"><span data-stu-id="cdb81-161">Use this procedure when:</span></span>

- <span data-ttu-id="cdb81-162">Zobrazení změn Common Data Service v Human Resources trvá příliš dlouho.</span><span class="sxs-lookup"><span data-stu-id="cdb81-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="cdb81-163">Chcete-li sledování vymazat, je nutné aktualizovat sledovací tabulku.</span><span class="sxs-lookup"><span data-stu-id="cdb81-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="cdb81-164">Chcete-li spustit úplnou synchronizaci entity mezi Human Resources a Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="cdb81-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="cdb81-165">V poli **Název entity CDS** vyberte entitu.</span><span class="sxs-lookup"><span data-stu-id="cdb81-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="cdb81-166">Vyberte **Synchronizovat nyní**.</span><span class="sxs-lookup"><span data-stu-id="cdb81-166">Select **Sync now**.</span></span>

<span data-ttu-id="cdb81-167">[![Spuštění úplné synchronizace](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="cdb81-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


