---
title: Povolit správu kvality a neshod
description: Toto téma poskytuje přehled procesu pro nastavení a konfiguraci funkcí správy kvality a neshod v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956247"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="a0527-103">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="a0527-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0527-104">Toto téma poskytuje přehled procesu pro nastavení a konfiguraci funkcí správy kvality a neshod v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a0527-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="a0527-105">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="a0527-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="a0527-106">Chcete-li ve svém systému povolit správu kvality, postupujte podle těchto pokynů.</span><span class="sxs-lookup"><span data-stu-id="a0527-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="a0527-107">Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry řízení zásob a skladu**.</span><span class="sxs-lookup"><span data-stu-id="a0527-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="a0527-108">Na kartě **Správa kvality** nastavte možnost **Použít správu kvality** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="a0527-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="a0527-109">Do pole **Hodinová sazba** zadejte hodinovou pracovní sazbu v místní měně.</span><span class="sxs-lookup"><span data-stu-id="a0527-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="a0527-110">Hodinová sazba se používá pro výpočet nákladů na operace, které souvisejí s neshodou.</span><span class="sxs-lookup"><span data-stu-id="a0527-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="a0527-111">Hodinová sazba a vypočtené náklady poskytují referenční informace o neshodách.</span><span class="sxs-lookup"><span data-stu-id="a0527-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="a0527-112">S ostatními funkcemi nespolupracují.</span><span class="sxs-lookup"><span data-stu-id="a0527-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="a0527-113">Vyberte **Nastavení sestavy**.</span><span class="sxs-lookup"><span data-stu-id="a0527-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="a0527-114">Přidejte nové řádky pro různé typy zpráv a vyberte typ dokumentu, který se má použít pro každou zprávu.</span><span class="sxs-lookup"><span data-stu-id="a0527-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="a0527-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a0527-115">Close the page.</span></span>
1. <span data-ttu-id="a0527-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a0527-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="a0527-117">Proces konfigurace správy kvality</span><span class="sxs-lookup"><span data-stu-id="a0527-117">Quality management configuration process</span></span>

<span data-ttu-id="a0527-118">Než začnete používat funkce správy kvality a generovat objednávky kvality, musíte nakonfigurovat systém a předpoklady.</span><span class="sxs-lookup"><span data-stu-id="a0527-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="a0527-119">Zde je seznam kroků, které jsou nutné ke konfiguraci správy kvality.</span><span class="sxs-lookup"><span data-stu-id="a0527-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="a0527-120">[Povolit správu kvality a neshod](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="a0527-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="a0527-121">Volitelně: [Nakonfigurovat zkušební nástroje](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="a0527-122">[Nakonfigurovat testy](quality-tests.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="a0527-123">[Nakonfigurujte testovací proměnné a výsledky](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="a0527-124">[Konfigurujte testovací skupiny](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="a0527-125">Volitelné: [Nakonfigurujte skupiny kvality a odkazy na produkty](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="a0527-126">Volitelně: [Nakonfigurujte přidružení kvality](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="a0527-127">Po dokončení konfigurace můžete začít vytvářet a zpracovávat objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="a0527-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="a0527-128">Další informace o vytváření a objednávek kvality a práci s nimi naleznete v tématu [Objednávky kvality](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="a0527-129">Proces konfigurace správy neshod</span><span class="sxs-lookup"><span data-stu-id="a0527-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="a0527-130">Než začnete používat funkce správy neshod a generovat neshody, musíte nakonfigurovat systém a předpoklady.</span><span class="sxs-lookup"><span data-stu-id="a0527-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="a0527-131">Zde je seznam kroků, které jsou nutné ke konfiguraci správy neshod.</span><span class="sxs-lookup"><span data-stu-id="a0527-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="a0527-132">[Povolit správu kvality a neshod](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="a0527-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="a0527-133">[Konfigurujte pracovníky, kteří jsou odpovědní za schvalování neshod](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="a0527-134">[Nakonfigurujte typy problémů](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="a0527-135">[Nakonfigurujte karanténní zóny](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="a0527-136">[Nakonfigurujte typy diagnostiky](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="a0527-137">[Nakonfigurujte operace](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="a0527-138">Volitelně: [Nakonfigurujte poplatky za kvalitu](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="a0527-139">Po dokončení konfigurace můžete začít vytvářet a zpracovávat neshody.</span><span class="sxs-lookup"><span data-stu-id="a0527-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="a0527-140">Další informace o vytvoření neshod a práci s nimi naleznete v tématu [Vytvoření a zpracování neshod](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="a0527-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0527-141">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a0527-141">Additional resources</span></span>

- [<span data-ttu-id="a0527-142">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="a0527-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="a0527-143">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="a0527-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="a0527-144">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="a0527-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
