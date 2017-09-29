--- 
title: "Definování skupin prostředků diskrétní výroby"
description: "Skupina prostředků je sada provozních prostředků, které obvykle odpovídají fyzické organizaci pracovních buněk, definovaných žlutými pruhy ve výrobní dílně."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2423fe91d1531a326080e3a584195ea864f2e3e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="4d799-103">Definování skupin prostředků diskrétní výroby</span><span class="sxs-lookup"><span data-stu-id="4d799-103">Define discrete manufacturing resource group</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d799-104">Skupina prostředků je sada provozních prostředků, které obvykle odpovídají fyzické organizaci pracovních buněk, definovaných žlutými pruhy ve výrobní dílně.</span><span class="sxs-lookup"><span data-stu-id="4d799-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="4d799-105">Tento postup popisuje, jak definovat skupinu prostředků pro použití v samostatné výrobě.</span><span class="sxs-lookup"><span data-stu-id="4d799-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="4d799-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="4d799-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="4d799-107">Přejděte do Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="4d799-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="4d799-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4d799-108">Click New.</span></span>
3. <span data-ttu-id="4d799-109">Zadejte hodnotu do pole Skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="4d799-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="4d799-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="4d799-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4d799-111">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="4d799-112">V poli Produkční jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="4d799-113">Definování výchozích operačních parametrů</span><span class="sxs-lookup"><span data-stu-id="4d799-113">Define default operational parameters</span></span>
1. <span data-ttu-id="4d799-114">Rozbalte sekci Operace.</span><span class="sxs-lookup"><span data-stu-id="4d799-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="4d799-115">V poli Podíl odpadu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4d799-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="4d799-116">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="4d799-117">V Kategorie operačního času zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="4d799-118">V poli Procento plánování operací zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4d799-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="4d799-119">Definujte provozní hodiny</span><span class="sxs-lookup"><span data-stu-id="4d799-119">Define operating hours</span></span>
1. <span data-ttu-id="4d799-120">Rozbalte sekci Kalendáře.</span><span class="sxs-lookup"><span data-stu-id="4d799-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="4d799-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4d799-121">Click Add.</span></span>
3. <span data-ttu-id="4d799-122">V poli Kalendář zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="4d799-123">Přidejte provozní prostředky</span><span class="sxs-lookup"><span data-stu-id="4d799-123">Add operations resources</span></span>
1. <span data-ttu-id="4d799-124">Rozbalte sekci Prostředky.</span><span class="sxs-lookup"><span data-stu-id="4d799-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="4d799-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4d799-125">Click Add.</span></span>
3. <span data-ttu-id="4d799-126">V poli Prostředky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="4d799-127">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4d799-127">Click Add.</span></span>
5. <span data-ttu-id="4d799-128">V poli Prostředky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d799-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="4d799-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4d799-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4d799-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="4d799-130">In the list, click the link in the selected row.</span></span>


