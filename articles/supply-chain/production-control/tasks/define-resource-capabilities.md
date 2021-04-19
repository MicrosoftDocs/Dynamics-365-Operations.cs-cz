---
title: Definování schopností prostředku
description: Schopnosti prostředku popisují, jaké mají provozní prostředky možnosti.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 072991e7b3844ad3583b7d0c575d426299f74e9f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828699"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="9c0b5-103">Definování schopností prostředku</span><span class="sxs-lookup"><span data-stu-id="9c0b5-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c0b5-104">Schopnosti prostředku popisují, jaké mají provozní prostředky možnosti.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="9c0b5-105">Při plánování jsou požadavky jednotlivých úloh a operací porovnávány s možnostmi dostupných prostředků.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="9c0b5-106">Tento Průvodce úkolem vám pomůže vytvořit schopnosti prostředku a přiřadit je k prostředku.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="9c0b5-107">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="9c0b5-108">Vytvořit schopnosti prostředku</span><span class="sxs-lookup"><span data-stu-id="9c0b5-108">Create a resource capability</span></span>
1. <span data-ttu-id="9c0b5-109">Přejděte na Schopnosti prostředku.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="9c0b5-110">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-110">Click New.</span></span>
3. <span data-ttu-id="9c0b5-111">V poli Schopnost zadejte ID schopnosti prostředku.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="9c0b5-112">Pro danou operaci použijte ID možnosti a určete tak, že zdroje musí mít tyto možnosti pro provedení operace.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="9c0b5-113">Do pole Popis zadejte popis schopností.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="9c0b5-114">Přiřadit schopnost k prostředku</span><span class="sxs-lookup"><span data-stu-id="9c0b5-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="9c0b5-115">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-115">Click Add.</span></span>
2. <span data-ttu-id="9c0b5-116">V poli Prostředek zadejte ID prostředku.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="9c0b5-117">Schopnost zdrojů může být přiřazena k jednomu nebo více zdrojům.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="9c0b5-118">Do pole Vypršení platnosti zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="9c0b5-119">Toto pole lze použít k určení toho, že zdroj má možnosti jen po omezenou dobu.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="9c0b5-120">V poli Priorita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="9c0b5-121">Při plánování prací a operací můžete určit, zda chcete vybrat zdroje podle priority.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="9c0b5-122">Pokud tuto možnost vyberte, a více než jeden zdroj může provádět úlohy nebo operace do požadovaného data, zdroj, který má prioritu nejnižší s ohledem na požadovanou funkci, bude vybrán.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="9c0b5-123">Do pole Úroveň zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="9c0b5-124">Pokud zadáte, že úloha nebo operace vyžaduje určitou možnost, můžete také určit minimální potřebné úrovně.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="9c0b5-125">použijte úroveň schopností k odlišení zdrojů, které lze použít ve stejné úloze, ale s různou rychlostí, silnými stránkami, velikostmi a tak dále.</span><span class="sxs-lookup"><span data-stu-id="9c0b5-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]