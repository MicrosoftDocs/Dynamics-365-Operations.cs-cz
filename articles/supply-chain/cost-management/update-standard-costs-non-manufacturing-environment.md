---
title: "Aktualizace standardních nákladů v nevýrobním prostředí"
description: "V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady v nevýrobním prostředí."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 432cdc516c74c4fff570366d0eab77323d3159bf
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="e9321-103">Aktualizace standardních nákladů v nevýrobním prostředí</span><span class="sxs-lookup"><span data-stu-id="e9321-103">Update standard costs in a non-manufacturing environment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e9321-104">V tomto článku jsou pokyny k tomu, jak aktualizovat standardní náklady v nevýrobním prostředí.</span><span class="sxs-lookup"><span data-stu-id="e9321-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="e9321-105">Tyto pokyny předpokládají, že používáte pro aktualizaci standardních nákladů metodou s použitím dvou verzí.</span><span class="sxs-lookup"><span data-stu-id="e9321-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="e9321-106">V tomto přístupu jedna nákladová verze obsahuje původně definované standardní náklady pro nastavené období a druhá nákladová verze obsahuje vzestupné aktualizace.</span><span class="sxs-lookup"><span data-stu-id="e9321-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="e9321-107">Každá aktualizace je zadána jako záznam o nákladech do druhé nákladové verze a nakonec bude aktivována.</span><span class="sxs-lookup"><span data-stu-id="e9321-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="e9321-108">Alternativní řešení používá přístup s použitím jedné verze pomocí původně definované sady standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="e9321-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="e9321-109">Metoda s použitím dvou verzí vyžaduje určení druhé nákladové verze.</span><span class="sxs-lookup"><span data-stu-id="e9321-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="e9321-110">Uvádíme pokyny k definování této nákladové verze:</span><span class="sxs-lookup"><span data-stu-id="e9321-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="e9321-111">Přiřaďte nákladový typ **Standardní náklady**.</span><span class="sxs-lookup"><span data-stu-id="e9321-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="e9321-112">Přiřazení platného popisného identifikátoru značícího obsah nákladové verze, jako je například **2016-AKTUALIZACE**.</span><span class="sxs-lookup"><span data-stu-id="e9321-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="e9321-113">Ověřte, že obsah zahrnuje záznamy o nákladech.</span><span class="sxs-lookup"><span data-stu-id="e9321-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="e9321-114">Povolte zadávání záznamů nákladů pro všechna pracoviště.</span><span class="sxs-lookup"><span data-stu-id="e9321-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="e9321-115">Pokud určíte pracoviště, záznamy nákladů lze zadat pouze pro dané pracoviště.</span><span class="sxs-lookup"><span data-stu-id="e9321-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="e9321-116">Určete pro princip zálohy hodnotu **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="e9321-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="e9321-117">Princip zálohy se vztahuje pouze na výpočty nákladů vyráběných položek.</span><span class="sxs-lookup"><span data-stu-id="e9321-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="e9321-118">Chcete-li opravit, upravit nebo aktualizovat standardní náklady nových položek, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="e9321-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="e9321-119">Pomocí stránky **Nastavení** **nákladové verze** povolte zadání záznamy nákladů do druhé nákladové verze.</span><span class="sxs-lookup"><span data-stu-id="e9321-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="e9321-120">Případně zabraňte aktivaci čekajících nákladů, protože tato aktivace bude povolena po úplném a přesném definování těchto nákladů.</span><span class="sxs-lookup"><span data-stu-id="e9321-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="e9321-121">Můžete také volitelně zadat datum do pole **Od data**.</span><span class="sxs-lookup"><span data-stu-id="e9321-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="e9321-122">Obecné platí, že používejte data, pokud chcete aktivovat přírůstkové aktualizace.</span><span class="sxs-lookup"><span data-stu-id="e9321-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="e9321-123">Případně ponechte pole **Od data** prázdné pro nákladovou verzi, a pak zadejte datum v poli **Od data** pro každý záznam o nákladech.</span><span class="sxs-lookup"><span data-stu-id="e9321-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="e9321-124">Pomocí stránky **Cena položky** zadejte aktualizuje jako záznamy nákladů na položky, které se nacházejí v druhé nákladové verzi.</span><span class="sxs-lookup"><span data-stu-id="e9321-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="e9321-125">Pomocí sestavy **Ceny položek** ověřte úplnost a přesnost záznamů nákladů položek v druhé nákladové verzi.</span><span class="sxs-lookup"><span data-stu-id="e9321-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="e9321-126">Pomocí stránky **Údržba nákladové verze** upravte příznak blokování a umožnit tak aktivaci záznamů čekajících nákladů ve druhé nákladové verzi.</span><span class="sxs-lookup"><span data-stu-id="e9321-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="e9321-127">Pomocí stránky **Aktivovat ceny** (kterou otevřete ze stránky **Údržba nákladové verze**) povolte všechny čekající záznamy nákladů položek ve druhé nákladové verzi.</span><span class="sxs-lookup"><span data-stu-id="e9321-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="e9321-128">Čekající záznamy nákladů pro jednotlivé položky lze také povolit klepnutím na tlačítko **Aktivovat nezpracované ceny** na stránce **Cena položky**.</span><span class="sxs-lookup"><span data-stu-id="e9321-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="e9321-129">Pomocí stránky **Nastavení nákladové verze** upravte příznaky blokování ve druhé nákladové verzi pro zabránění další údržby dat.</span><span class="sxs-lookup"><span data-stu-id="e9321-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="e9321-130">Zásady blokování zabraňují zadávání nových čekajících nákladů a aktivaci čekajících nákladů.</span><span class="sxs-lookup"><span data-stu-id="e9321-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





