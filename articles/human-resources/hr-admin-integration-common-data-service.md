---
title: Konfigurovat integraci se službou Dataverse
description: Integraci mezi Microsoft Dataverse a Dynamics 365 Human Resources můžete zapnout nebo vypnout. Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat tabulku.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: bf406a954f5bb8b49627b58a901d0721cdad407b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890021"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="91f2f-104">Konfigurovat integraci se službou Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="91f2f-105">Integraci mezi Microsoft Dataverse a Dynamics 365 Human Resources můžete zapnout nebo vypnout.</span><span class="sxs-lookup"><span data-stu-id="91f2f-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="91f2f-106">Chcete-li pomoci při řešení problémů s daty mezi oběma prostředími, můžete také zobrazit podrobnosti o synchronizaci, vymazat data sledování a znovu synchronizovat tabulku.</span><span class="sxs-lookup"><span data-stu-id="91f2f-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="91f2f-107">Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="91f2f-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="91f2f-108">Když vypnete integraci, uživatelé mohou provádět změny v Human Resources nebo Dataverse, ale tyto změny se mezi oběma prostředími nesynchronizují.</span><span class="sxs-lookup"><span data-stu-id="91f2f-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="91f2f-109">Ve výchozím nastavení je integrace dat mezi Human Resources a Dataverse vypnuta.</span><span class="sxs-lookup"><span data-stu-id="91f2f-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="91f2f-110">V těchto situacích je vhodné vypnout integraci:</span><span class="sxs-lookup"><span data-stu-id="91f2f-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="91f2f-111">Vyplňujete data prostřednictvím Data Management Framework a je nutné je importovat vícekrát, aby je bylo možné dostat do správného stavu.</span><span class="sxs-lookup"><span data-stu-id="91f2f-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="91f2f-112">Existují problémy s daty v modulu Human Resources nebo Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="91f2f-113">Pokud vypnete integraci, můžete odstranit záznam v jednom prostředí, aniž byste ho odstranili v jiném.</span><span class="sxs-lookup"><span data-stu-id="91f2f-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="91f2f-114">Pokud opět zapnete integraci, bude záznam v prostředí, kde nebyl odstraněn, synchronizován zpět do prostředí, ve kterém byl odstraněn.</span><span class="sxs-lookup"><span data-stu-id="91f2f-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="91f2f-115">Synchronizace začíná při příštím spuštění dávkové úlohy **Integrace Dataverse zmeškala synchronizaci požadavku**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="91f2f-116">Když vypnete integraci dat, ujistěte se, že neupravujete stejný záznam v obou prostředích.</span><span class="sxs-lookup"><span data-stu-id="91f2f-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="91f2f-117">Pokud zapnete integraci znovu, bude naposledy upravený záznam synchronizován.</span><span class="sxs-lookup"><span data-stu-id="91f2f-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="91f2f-118">Pokud tedy neprovedete stejné změny v záznamu v obou prostředích, může dojít ke ztrátě dat.</span><span class="sxs-lookup"><span data-stu-id="91f2f-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="91f2f-119">Přístup na stránku integrace Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="91f2f-120">V instanci Human Resources, v níž chcete zobrazit nebo konfigurovat nastavení pro integraci s Dataverse, vyberte dlaždici **Správa systému**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="91f2f-121">[![Dlaždice správy systému](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="91f2f-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="91f2f-122">Zvolte kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="91f2f-123">[![Karta Odkazy](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="91f2f-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="91f2f-124">V části **Integrace** vyberte **Konfigurace Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="91f2f-125">[![Odkaz na konfiguraci Dataverse](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="91f2f-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="91f2f-126">Zapnutí a vypnutí integrace dat mezi Human Resources a Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="91f2f-127">Chcete-li zapnout integraci, nastavte možnost **Povolit integraci Dataverse** na stránce **Integrace doMicrosoft Dataverse** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="91f2f-128">Při zapnutí integrace budou data synchronizována při příštím spuštění dávkové úlohy **Integrace Dataverse zmeškala synchronizaci požadavku**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="91f2f-129">Všechna data by měla být k dispozici po dokončení dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="91f2f-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="91f2f-130">Chcete-li vypnout integraci, nastavte možnost na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="91f2f-131">[![Zapnutí a vypnutí integrace Dataverse](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="91f2f-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="91f2f-132">Důrazně doporučujeme vypnout integraci Dataverse při provádění úkolů migrace dat.</span><span class="sxs-lookup"><span data-stu-id="91f2f-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="91f2f-133">Odesílání velkého objemu dat může výrazně ovlivnit výkon.</span><span class="sxs-lookup"><span data-stu-id="91f2f-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="91f2f-134">Například nahrávání 2000 pracovníků může trvat několik hodin, když je integrace povolena, a méně než jednu hodinu, pokud je zakázána.</span><span class="sxs-lookup"><span data-stu-id="91f2f-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="91f2f-135">Čísla uvedená v tomto příkladu slouží pouze k demonstračním účelům.</span><span class="sxs-lookup"><span data-stu-id="91f2f-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="91f2f-136">Přesné množství času potřebného k importu záznamů se může značně lišit v závislosti na mnoha faktorech.</span><span class="sxs-lookup"><span data-stu-id="91f2f-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="91f2f-137">Zobrazení podrobností integrace dat</span><span class="sxs-lookup"><span data-stu-id="91f2f-137">View data integration details</span></span>

<span data-ttu-id="91f2f-138">Na záložce s náhledem **Správa** na stránce **Integrace Microsoft Dataverse** můžete zobrazit, jak budou řádky vzájemně propojeny mezi Human Resources a Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="91f2f-139">Chcete-li zobrazit řádky tabulky, vyberte tabulku v poli **Tabulky Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="91f2f-140">V mřížce jsou uvedeny všechny řádky, které jsou propojeny s vybranou tabulkou.</span><span class="sxs-lookup"><span data-stu-id="91f2f-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="91f2f-141">V tuto chvíli nejsou uvedeny všechny tabulky Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="91f2f-142">V mřížce se zobrazí pouze tabulky, které podporují použití vlastních polí.</span><span class="sxs-lookup"><span data-stu-id="91f2f-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="91f2f-143">Nové tabulky jsou k dispozici prostřednictvím kontinuálního vydávání aplikace Human Resources.</span><span class="sxs-lookup"><span data-stu-id="91f2f-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="91f2f-144">Mřížka obsahuje následující pole:</span><span class="sxs-lookup"><span data-stu-id="91f2f-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="91f2f-145">**Tabulka Dataverse** - Název tabulky v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="91f2f-146">**Odkaz na Dataverse tabulku**- identifikátor používající Dataverse k identifikaci záznamu.</span><span class="sxs-lookup"><span data-stu-id="91f2f-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="91f2f-147">Tato hodnota je ekvivalentní hodnotě **RecId** Human Resources.</span><span class="sxs-lookup"><span data-stu-id="91f2f-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="91f2f-148">Identifikátor lze najít při otevření tabulky Dataverse v aplikaci Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="91f2f-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="91f2f-149">**Název entity Human Resources** – entita Human Resources, která naposledy synchronizovala data do Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="91f2f-150">Entita může mít buď předponu Dataverse, nebo jinou předponu.</span><span class="sxs-lookup"><span data-stu-id="91f2f-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="91f2f-151">**Odkaz na Human Resources** - hodnota **RecId**, která je přidružená k záznamu v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="91f2f-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="91f2f-152">**Odstraněna z Dataverse** - hodnota, která určuje, zda byl řádek odstraněn z Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="91f2f-153">Záznamy v Human Resources odpovídají řádkům v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="91f2f-154">Odebrání přidružení záznamu v Human Resources z řádku Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="91f2f-155">Pokud se setkáte s problémy při synchronizaci dat mezi Human Resources a Dataverse, můžete je vyřešit vymazáním sledování a opakovanou synchronizací sledovací tabulky.</span><span class="sxs-lookup"><span data-stu-id="91f2f-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="91f2f-156">Pokud přidružení odeberete a poté změníte nebo odstraníte řádek v Dataverse, nebudou provedené změny synchronizovány do Human Resources.</span><span class="sxs-lookup"><span data-stu-id="91f2f-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="91f2f-157">Pokud provedete změny v Human Resources, bude vytvořen nový záznam sledování a řádek bude aktualizován v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="91f2f-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="91f2f-158">Chcete-li odebrat přidružení záznamu mezi záznamem a řádkem Dataverse v Human Resources, vyberte **Tabulka Dataverse** a poté vyberte možnost **Vymazat informace o sledování**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="91f2f-159">[![Vymazat informace o sledování](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="91f2f-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="91f2f-160">Chcete-li spustit úplnou synchronizaci tabulky po vymazání sledování, postupujte podle následujícího postupu.</span><span class="sxs-lookup"><span data-stu-id="91f2f-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="91f2f-161">Synchronizace tabulky mezi Human Resources a Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="91f2f-162">Tento postup použijte v následujících případech:</span><span class="sxs-lookup"><span data-stu-id="91f2f-162">Use this procedure when:</span></span>

- <span data-ttu-id="91f2f-163">Zobrazení změn Dataverse v Human Resources trvá příliš dlouho.</span><span class="sxs-lookup"><span data-stu-id="91f2f-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="91f2f-164">Chcete-li sledování vymazat, je nutné aktualizovat sledovací tabulku.</span><span class="sxs-lookup"><span data-stu-id="91f2f-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="91f2f-165">Chcete-li spustit úplnou synchronizaci tabulky mezi Human Resources a Dataverse:</span><span class="sxs-lookup"><span data-stu-id="91f2f-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="91f2f-166">Vyberte tabulku v poli **Tabulka Dataverse**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="91f2f-167">Vyberte **Synchronizovat nyní**.</span><span class="sxs-lookup"><span data-stu-id="91f2f-167">Select **Sync now**.</span></span>

<span data-ttu-id="91f2f-168">[![Spuštění úplné synchronizace](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="91f2f-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="91f2f-169">Viz také</span><span class="sxs-lookup"><span data-stu-id="91f2f-169">See also</span></span>

[<span data-ttu-id="91f2f-170">Tabulky Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="91f2f-171">Konfigurace virtuálních tabulek Dataverse</span><span class="sxs-lookup"><span data-stu-id="91f2f-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="91f2f-172">Virtuální tabulky lidských zdrojů - časté dotazy</span><span class="sxs-lookup"><span data-stu-id="91f2f-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="91f2f-173">Co je Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="91f2f-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="91f2f-174">Aktualizace terminologie</span><span class="sxs-lookup"><span data-stu-id="91f2f-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]