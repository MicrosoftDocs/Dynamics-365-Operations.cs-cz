---
title: Přehled integrace s Microsoft Dynamics 365 Field Service
description: Toto téma poskytuje přehled o integraci s Microsoft Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 2a5c3e49f09bf4f1f90449db10d439f563ecc2c0
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249822"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="b960f-103">Přehled integrace s Microsoft Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="b960f-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b960f-104">Supply Chain Management umožňuje synchronizaci obchodních procesů mezi aplikacemi Dynamics 365 Supply Chain Management a Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b960f-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="b960f-105">Scénáře integrace jsou konfigurovány s použitím rozsáhlých šablon integrátoru dat a Common Data Service pro umožnění synchronizace obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="b960f-105">The integration scenarios are configured by using extensible Data integrator templates and Common Data Service to enable the synchronization of business processes.</span></span>
<span data-ttu-id="b960f-106">Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních obchodních potřeb.</span><span class="sxs-lookup"><span data-stu-id="b960f-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="b960f-107">Integrace Field Service staví na současné funkci potenciálního zákazníka k hotovosti.</span><span class="sxs-lookup"><span data-stu-id="b960f-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/field-service-integration.png)

<span data-ttu-id="b960f-109">První fáze integrace mezi Field Service a Supply Chain Management se zaměřuje na povolení pracovních příkazů a smluv ve Field Service pro fakturaci v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b960f-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="b960f-110">Podporovaný tok začíná ve Field Service, kde jsou informace z pracovních příkazů synchronizovány s Supply Chain Management jako prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b960f-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="b960f-111">V Supply Chain Management jsou prodejní objednávky fakturovány za účelem generování fakturačních dokumentů.</span><span class="sxs-lookup"><span data-stu-id="b960f-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="b960f-112">Kromě toho jsou informace z faktur smluv ve službě Field Service synchronizovány do aplikace Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b960f-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="b960f-113">Integrátor dat Microsoft Dynamics 365 synchronizuje data pomocí upravitelné projektů.</span><span class="sxs-lookup"><span data-stu-id="b960f-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="b960f-114">Standardní šablony lze používat k vytváření projektů vlastní integrace, kde další standardní a vlastní pole a také entity, mohou být mapovány pro účely úpravy integrace a plnění konkrétních požadavků.</span><span class="sxs-lookup"><span data-stu-id="b960f-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="b960f-115">První fáze integrace mezi Field Service a Finance and Supply Chain Management umožňuje synchronizaci následujících položek:</span><span class="sxs-lookup"><span data-stu-id="b960f-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="b960f-116">Produkty v modulu Supply Chain Management na produkty v modulu Field Service, které zahrnují informace o typu produktu</span><span class="sxs-lookup"><span data-stu-id="b960f-116">Products in Supply Chain Management to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="b960f-117">Pracovní příkazy ve službě Field Service do prodejních objednávek v aplikaci Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b960f-117">Work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="b960f-118">Faktury v aplikaci Field Service na volné textové faktury v Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b960f-118">Invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="b960f-119">Příklad synchronizace výrobního příkazu mezi Field Service a Supply Chain Management uvádí krátké video na YouTube [Jak synchronizovat výrobní příkaz s integrací Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="b960f-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="b960f-120">Integrace s aplikací Field Service, včetně informací a zásobách a projektu</span><span class="sxs-lookup"><span data-stu-id="b960f-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="b960f-121">Další funkce v této druhé fázi se zaměřovala na to, aby technikům v terénu poskytovala přehled o skladových informacích z modulu Supply Chain Management, a umožnila jim tak aktualizovat úrovně zásob a provádět převod materiálů.</span><span class="sxs-lookup"><span data-stu-id="b960f-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="b960f-122">Kromě toho společnosti zajišťující instalaci nebo servis prodaného zboží budou využívat lepší kontrolu a viditelnost plného prodejního a servisního procesu s integrací z projektů.</span><span class="sxs-lookup"><span data-stu-id="b960f-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="b960f-123">Funkce zahrnuje integraci následujících informací:</span><span class="sxs-lookup"><span data-stu-id="b960f-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="b960f-124">Informace o skladovacím místě</span><span class="sxs-lookup"><span data-stu-id="b960f-124">Warehouse information</span></span>
- <span data-ttu-id="b960f-125">Informace o množství na skladě</span><span class="sxs-lookup"><span data-stu-id="b960f-125">On-hand inventory information</span></span>
- <span data-ttu-id="b960f-126">Převody zásob</span><span class="sxs-lookup"><span data-stu-id="b960f-126">Inventory transfers</span></span>
- <span data-ttu-id="b960f-127">Úpravy zásob</span><span class="sxs-lookup"><span data-stu-id="b960f-127">Inventory adjustments</span></span>
- <span data-ttu-id="b960f-128">Projekty Supply Chain Management spojené s pracovními objednávkami Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="b960f-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="b960f-129">Pracovní příkazy Dynamics 365 Field Service s odkazem na projekty Supply Chain Management, použijte toto číslo projektu na prodejní objednávky, abyste povolili fakturaci z projektu.</span><span class="sxs-lookup"><span data-stu-id="b960f-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Synchronizace obchodních procesů mezi Supply Chain Management a Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="b960f-131">Druhá fáze integrace mezi Field Service a Supply Chain Management umožňuje synchronizaci s následujícími šablonami:</span><span class="sxs-lookup"><span data-stu-id="b960f-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="b960f-132">Sklady (Supply Chain Management do Field Service) - sklady ze Supply Chain Management do Field Service [rozšířený dotaz]</span><span class="sxs-lookup"><span data-stu-id="b960f-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="b960f-133">Zásoby produktu (Supply Chain Management do Field Service) - informace o úrovni zásob ze Supply Chain Management do Field Service [rozšířený dotaz]</span><span class="sxs-lookup"><span data-stu-id="b960f-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="b960f-134">Úprava zásob (Field Service do Supply Chain Management) - Úprava zásob z Field Service do Supply Chain Management [rozšířený dotaz]</span><span class="sxs-lookup"><span data-stu-id="b960f-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="b960f-135">Převody zásob (Field Service do Supply Chain Management) - Převody zásob z Field Service do Supply Chain Management [rozšířený dotaz]</span><span class="sxs-lookup"><span data-stu-id="b960f-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="b960f-136">Projekty (Supply Chain Management do Field Service) - seznam projektů ze Supply Chain Management do Field Service</span><span class="sxs-lookup"><span data-stu-id="b960f-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="b960f-137">pracovní příkazy s projektem (Field Service do Supply Chain Management) - Pracovní příkazy v Field Service do příkazů k prodeji v Supply Chain Management, s podporou projektu [Pokročilý dotaz]</span><span class="sxs-lookup"><span data-stu-id="b960f-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="b960f-138">Produkty Field Service Products se skladovou jednotkou (Supply Chain Management do Sales) - prodejné vydané produkty Supply Chain Management pro Field Service, včetně skladové jednotky</span><span class="sxs-lookup"><span data-stu-id="b960f-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="b960f-139">Systémové požadavky</span><span class="sxs-lookup"><span data-stu-id="b960f-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="b960f-140">Systémové požadavky pro Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b960f-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="b960f-141">Integrace Field Service podporuje následující verze:</span><span class="sxs-lookup"><span data-stu-id="b960f-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="b960f-142">Dynamics 365 for Finance and Operations verze 8.1.2 (Prosinec 2018) byla vydána v 2018 dne a má číslo sestavení aplikace 8.1.195 s aktualizací Platform update 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="b960f-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="b960f-143">Požadavky na systém pro Field Service</span><span class="sxs-lookup"><span data-stu-id="b960f-143">System requirements for Field Service</span></span>
<span data-ttu-id="b960f-144">Chcete-li použít řešení integrace Field Service, je nutné nainstalovat následující komponenty:</span><span class="sxs-lookup"><span data-stu-id="b960f-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="b960f-145">Field Service (verze 8.2.0.286) nebo novější na Dynamics 365 9.1.x - vydána v listopadu 2018</span><span class="sxs-lookup"><span data-stu-id="b960f-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="b960f-146">Řešení Prospect to Cash (P2C) pro Dynamics 365, verze 1.15.0.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="b960f-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="b960f-147">Řešení je k dispozici ke stažení z [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="b960f-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="b960f-148">Řešení 'Field Service Integration, Project and Inventory' pro Dynamics 365, verze 2.0.0.0 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="b960f-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="b960f-149">Řešení je k dispozici ke stažení z [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="b960f-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
