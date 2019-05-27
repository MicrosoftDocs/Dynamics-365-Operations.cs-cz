---
title: Vytvoření šablony záznamu pro usnadnění zadávání dat
description: Tento postup ukazuje, jak vytvořit šablonu záznamu tak, že hodnoty pole, které jsou často používány, nemusí být zadány explicitně pro každý nový záznam.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544245"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="96ab0-103">Vytvoření šablony záznamu pro usnadnění zadávání dat</span><span class="sxs-lookup"><span data-stu-id="96ab0-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96ab0-104">Tento postup ukazuje, jak vytvořit šablonu záznamu tak, že hodnoty pole, které jsou často používány, nemusí být zadány explicitně pro každý nový záznam.</span><span class="sxs-lookup"><span data-stu-id="96ab0-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="96ab0-105">V tomto postupu vytvoříte nový záznam pro nové laptopy, které mají být přidány do dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="96ab0-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="96ab0-106">Tento postup používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="96ab0-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="96ab0-107">Přejděte do části Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="96ab0-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="96ab0-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96ab0-108">Click New.</span></span>
3. <span data-ttu-id="96ab0-109">Zadejte nebo vyberte hodnotu v poli Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="96ab0-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="96ab0-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="96ab0-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="96ab0-111">Zadejte například 'laptop potenciálního zákazníka společnosti'.</span><span class="sxs-lookup"><span data-stu-id="96ab0-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="96ab0-112">Do pole Vyhledávání jména zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="96ab0-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="96ab0-113">Například zadejte 'laptop.'</span><span class="sxs-lookup"><span data-stu-id="96ab0-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="96ab0-114">Rozbalte oddíl Technické informace.</span><span class="sxs-lookup"><span data-stu-id="96ab0-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="96ab0-115">Zadejte hodnotu do pole Značka.</span><span class="sxs-lookup"><span data-stu-id="96ab0-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="96ab0-116">Zadejte hodnotu do pole Model.</span><span class="sxs-lookup"><span data-stu-id="96ab0-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="96ab0-117">Zadejte hodnotu do pole Rok výroby modelu.</span><span class="sxs-lookup"><span data-stu-id="96ab0-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="96ab0-118">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="96ab0-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="96ab0-119">Klikněte na Informace o záznamu</span><span class="sxs-lookup"><span data-stu-id="96ab0-119">Click Record info.</span></span>
12. <span data-ttu-id="96ab0-120">Klikněte na možnost Uživatelská šablona.</span><span class="sxs-lookup"><span data-stu-id="96ab0-120">Click User template.</span></span>
13. <span data-ttu-id="96ab0-121">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="96ab0-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="96ab0-122">Zadejte například 'firemní laptop.'</span><span class="sxs-lookup"><span data-stu-id="96ab0-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="96ab0-123">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="96ab0-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="96ab0-124">Zadejte například 'firemní laptop'.</span><span class="sxs-lookup"><span data-stu-id="96ab0-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="96ab0-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="96ab0-125">Click OK.</span></span>
16. <span data-ttu-id="96ab0-126">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="96ab0-126">Click Close.</span></span>

