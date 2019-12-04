---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (5. listopadu 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778375"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="4a685-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (5. listopadu 2019)</span><span class="sxs-lookup"><span data-stu-id="4a685-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4a685-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="4a685-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="4a685-105">Změny v aplikaci Attract</span><span class="sxs-lookup"><span data-stu-id="4a685-105">Changes in Attract</span></span>

<span data-ttu-id="4a685-106">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="4a685-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="4a685-107">Změny v aplikaci Onboard</span><span class="sxs-lookup"><span data-stu-id="4a685-107">Changes in Onboard</span></span>

<span data-ttu-id="4a685-108">Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="4a685-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="4a685-109">Změny v Core HR</span><span class="sxs-lookup"><span data-stu-id="4a685-109">Changes in Core HR</span></span>

<span data-ttu-id="4a685-110">Změny popsané v této části se vztahují na číslo sestavení 8.1.2598.</span><span class="sxs-lookup"><span data-stu-id="4a685-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="4a685-111">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="4a685-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="4a685-112">Kopírování instance Core HR</span><span class="sxs-lookup"><span data-stu-id="4a685-112">Copy a Core HR instance</span></span>

<span data-ttu-id="4a685-113">V této týdenní verzi můžete pomocí služby Microsoft Dynamics Lifecycle Services (LCS) kopírovat databázi Microsoft Dynamics 365 Talent: Core HR do prostředí izolovaného prostoru (sandbox).</span><span class="sxs-lookup"><span data-stu-id="4a685-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="4a685-114">Máte-li jiné prostředí izolovaného prostoru (sandbox), můžete také zkopírovat databázi z prostředí do cíleného prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="4a685-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="4a685-115">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="4a685-115">For more information, see:</span></span>

- <span data-ttu-id="4a685-116">[Rozsáhlejší správa prostředí](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management)v plánu 2 vlny vydání Dynamics 365: 2019</span><span class="sxs-lookup"><span data-stu-id="4a685-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="4a685-117">[Zkopírování instance Core HR](hr-copy-instance.md) do dokumentace aplikace Talent</span><span class="sxs-lookup"><span data-stu-id="4a685-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="4a685-118">Dávkové úlohy integrace Common Data Service se nevytvoří, když je povolena integrace Common Data Service (388030)</span><span class="sxs-lookup"><span data-stu-id="4a685-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="4a685-119">Tato změna vytvoří dávkové úlohy pro integraci Common Data Service, když je povolena.</span><span class="sxs-lookup"><span data-stu-id="4a685-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="4a685-120">HcmPersonImageEntity nemění velikost obrázku osoby při odeslání (369469)</span><span class="sxs-lookup"><span data-stu-id="4a685-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="4a685-121">Verze z tohoto týdne při importu pomocí správy dat změní způsob změny velikosti obrázků pro lepší výkon.</span><span class="sxs-lookup"><span data-stu-id="4a685-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="4a685-122">Pozice, která je k dispozici pro datum přiřazení, může předcházet datu aktivace (340103).</span><span class="sxs-lookup"><span data-stu-id="4a685-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="4a685-123">Při této změně se zobrazí varování v případě, že vyberete **Dostupné pro datum přiřazení**, které předchází **Datum aktivace pozice**.</span><span class="sxs-lookup"><span data-stu-id="4a685-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="4a685-124">Nelze vytvořit požadavek na změnu kompenzace v samoobslužných plánech zaměstnanců pro plány založené na kroku (376872).</span><span class="sxs-lookup"><span data-stu-id="4a685-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="4a685-125">Tato verze opravuje problém při požadavku na změny kompenzace prostřednictvím samoobslužných stránek zaměstnanců pro plány založené na jednotlivých krocích.</span><span class="sxs-lookup"><span data-stu-id="4a685-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="4a685-126">Kód důvodu není synchronizován s Common Data Service, pokud je popis delší než 30 znaků. Core HR umožňuje 60 (352682)</span><span class="sxs-lookup"><span data-stu-id="4a685-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="4a685-127">S touto změnou budou v aplikaci Common Data Service aktualizovány kódy důvodů s více než 30 znaky.</span><span class="sxs-lookup"><span data-stu-id="4a685-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="4a685-128">Změny provedené v Common Data Service se také odrazí v aplikaci Talent.</span><span class="sxs-lookup"><span data-stu-id="4a685-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="4a685-129">Řešení integrace z aplikace Talent do Finance and Operations (351961)</span><span class="sxs-lookup"><span data-stu-id="4a685-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="4a685-130">Tato verze opravuje problém, kdy adresy aktualizované v aplikaci Talent nebyly aktualizovány v modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4a685-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="4a685-131">Změny v blocích adresy budou nyní aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="4a685-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="4a685-132">Již brzy</span><span class="sxs-lookup"><span data-stu-id="4a685-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="4a685-133">Tisk kontrol výkonnosti</span><span class="sxs-lookup"><span data-stu-id="4a685-133">Print performance reviews</span></span>

<span data-ttu-id="4a685-134">Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.</span><span class="sxs-lookup"><span data-stu-id="4a685-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="4a685-135">Pracovní prostor Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="4a685-135">Feature management workspace</span></span>

<span data-ttu-id="4a685-136">Funkce se přidávají a aktualizují v každém vydání.</span><span class="sxs-lookup"><span data-stu-id="4a685-136">Features are added and updated in every release.</span></span> <span data-ttu-id="4a685-137">Funkce Správa funkcí poskytuje pracovní prostor, ve kterém si můžete prohlédnout seznam funkcí, které byly dodány v jednotlivých vydáních.</span><span class="sxs-lookup"><span data-stu-id="4a685-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="4a685-138">Ve výchozím nastavení jsou nové funkce vypnuté.</span><span class="sxs-lookup"><span data-stu-id="4a685-138">By default, new features are turned off.</span></span> <span data-ttu-id="4a685-139">Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace.</span><span class="sxs-lookup"><span data-stu-id="4a685-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="4a685-140">Další informace o změnách přicházejících ve správě funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="4a685-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
