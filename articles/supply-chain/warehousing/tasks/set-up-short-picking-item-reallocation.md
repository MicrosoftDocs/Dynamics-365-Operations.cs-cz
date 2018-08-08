--- 
title: "Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění"
description: "Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován."
author: ShylaThompson
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 99a4afb58f0c4beef818fd7c0a6a1837e00638d8
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="74dd7-103">Nastavení opakovaného přidělení zboží při krátkodobém vyskladnění</span><span class="sxs-lookup"><span data-stu-id="74dd7-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74dd7-104">Tato procedura ukazuje, jak umožnit pracovníkům skladu rychle najít alternativní umístění, pokud nejsou k dispozici dostatečné zásoby v umístění, do něhož byl nasměrován.</span><span class="sxs-lookup"><span data-stu-id="74dd7-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="74dd7-105">Je možné použít automatický proces opětovného přidělení, který používá směrnice pro umístění k získání zboží, pokud je k dispozici na jiném místě.</span><span class="sxs-lookup"><span data-stu-id="74dd7-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="74dd7-106">Také při použití ručního opětovné přidělení je seznam umístění s dostupným množstvím zobrazen na mobilním zařízení, což umožňuje pracovníkovi skladu zvolit umístění, ze kterého má použít zásoby.</span><span class="sxs-lookup"><span data-stu-id="74dd7-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="74dd7-107">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="74dd7-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="74dd7-108">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="74dd7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="74dd7-109">Nastavit pracovní výjimky</span><span class="sxs-lookup"><span data-stu-id="74dd7-109">Set up work exceptions</span></span>
1. <span data-ttu-id="74dd7-110">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Výjimky práce.</span><span class="sxs-lookup"><span data-stu-id="74dd7-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="74dd7-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="74dd7-111">Click New.</span></span>
    * <span data-ttu-id="74dd7-112">Je možné definovat několik pracovních výjimek práce s jinými zásadami opakovaného přidělení zboží umožňujícími zaměstnanci skladu výběr na základě potřeb dodávky, kterou zpracovávají.</span><span class="sxs-lookup"><span data-stu-id="74dd7-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="74dd7-113">Zadejte hodnotu do pole Kód výjimky práce.</span><span class="sxs-lookup"><span data-stu-id="74dd7-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="74dd7-114">Pracovní výjimku pojmenujte tak, aby indikovala, k čemu se používá.</span><span class="sxs-lookup"><span data-stu-id="74dd7-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="74dd7-115">Například Návod ke krátkodobému vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="74dd7-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="74dd7-116">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="74dd7-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="74dd7-117">Na V poli Typ výjimky vyberte Krátkodobě vyskladnit.</span><span class="sxs-lookup"><span data-stu-id="74dd7-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="74dd7-118">Zaškrtněte políčko Upravit zásoby.</span><span class="sxs-lookup"><span data-stu-id="74dd7-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="74dd7-119">Tato možnost znamená, že zásoby budou automaticky upraveny na 0 v místě krátkodobého vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="74dd7-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="74dd7-120">V poli Výchozí kód typu úpravy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74dd7-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="74dd7-121">Například v USMF můžete vybrat "Odebrat Res Adj Out".</span><span class="sxs-lookup"><span data-stu-id="74dd7-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="74dd7-122">V poli Opakované přidělení zboží vyberte Ruční.</span><span class="sxs-lookup"><span data-stu-id="74dd7-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="74dd7-123">Pokud vyberete Ruční nebo Automatické a ruční, pracovník skladu musí mít povoleno použití ručního přerozdělení.</span><span class="sxs-lookup"><span data-stu-id="74dd7-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="74dd7-124">Nastavení pracovníka k použití ručního opakované přidělení zboží</span><span class="sxs-lookup"><span data-stu-id="74dd7-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="74dd7-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74dd7-125">Close the page.</span></span>
2. <span data-ttu-id="74dd7-126">Přejděte do nabídky Řízení skladu > Nastavení > Pracovník.</span><span class="sxs-lookup"><span data-stu-id="74dd7-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="74dd7-127">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="74dd7-127">Click Edit.</span></span>
4. <span data-ttu-id="74dd7-128">Vyberte ze seznamu Pracovník 24.</span><span class="sxs-lookup"><span data-stu-id="74dd7-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="74dd7-129">Rozbalte oddíl Práce.</span><span class="sxs-lookup"><span data-stu-id="74dd7-129">Expand the Work section.</span></span>
6. <span data-ttu-id="74dd7-130">Vyberte možnost Ano v poli Povolit ruční opakované přidělení zboží.</span><span class="sxs-lookup"><span data-stu-id="74dd7-130">Select Yes in the Allow manual item reallocation field.</span></span>


