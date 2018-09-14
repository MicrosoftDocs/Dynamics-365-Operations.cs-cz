--- 
title: "Definování skupin prostředků diskrétní výroby"
description: "Skupina prostředků je sada provozních prostředků, které obvykle odpovídají fyzické organizaci pracovních buněk, definovaných žlutými pruhy ve výrobní dílně."
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="fa237-103">Definování skupin prostředků diskrétní výroby</span><span class="sxs-lookup"><span data-stu-id="fa237-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa237-104">Skupina prostředků je sada provozních prostředků, které obvykle odpovídají fyzické organizaci pracovních buněk, definovaných žlutými pruhy ve výrobní dílně.</span><span class="sxs-lookup"><span data-stu-id="fa237-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="fa237-105">Tento postup popisuje, jak definovat skupinu prostředků pro použití v samostatné výrobě.</span><span class="sxs-lookup"><span data-stu-id="fa237-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="fa237-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="fa237-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="fa237-107">Přejděte do Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="fa237-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="fa237-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fa237-108">Click New.</span></span>
3. <span data-ttu-id="fa237-109">Zadejte hodnotu do pole Skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="fa237-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="fa237-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="fa237-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fa237-111">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="fa237-112">V poli Produkční jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="fa237-113">Definování výchozích operačních parametrů</span><span class="sxs-lookup"><span data-stu-id="fa237-113">Define default operational parameters</span></span>
1. <span data-ttu-id="fa237-114">Rozbalte sekci Operace.</span><span class="sxs-lookup"><span data-stu-id="fa237-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="fa237-115">V poli Podíl odpadu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fa237-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="fa237-116">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="fa237-117">V Kategorie operačního času zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="fa237-118">V poli Procento plánování operací zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fa237-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="fa237-119">Definujte provozní hodiny</span><span class="sxs-lookup"><span data-stu-id="fa237-119">Define operating hours</span></span>
1. <span data-ttu-id="fa237-120">Rozbalte sekci Kalendáře.</span><span class="sxs-lookup"><span data-stu-id="fa237-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="fa237-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fa237-121">Click Add.</span></span>
3. <span data-ttu-id="fa237-122">V poli Kalendář zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="fa237-123">Přidejte provozní prostředky</span><span class="sxs-lookup"><span data-stu-id="fa237-123">Add operations resources</span></span>
1. <span data-ttu-id="fa237-124">Rozbalte sekci Prostředky.</span><span class="sxs-lookup"><span data-stu-id="fa237-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="fa237-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fa237-125">Click Add.</span></span>
3. <span data-ttu-id="fa237-126">V poli Prostředky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="fa237-127">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fa237-127">Click Add.</span></span>
5. <span data-ttu-id="fa237-128">V poli Prostředky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fa237-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="fa237-129">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fa237-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fa237-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fa237-130">In the list, click the link in the selected row.</span></span>


