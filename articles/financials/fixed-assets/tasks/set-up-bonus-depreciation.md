---
title: Nastavení počátečního mimořádného odpisu
description: Tento postup popisuje vytvoření nové náhrady za zvláštní odpisy a její přiřazení ke knize dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839874"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="758b0-103">Nastavení počátečního mimořádného odpisu</span><span class="sxs-lookup"><span data-stu-id="758b0-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="758b0-104">Tento postup popisuje vytvoření nové náhrady za zvláštní odpisy a její přiřazení ke knize dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="758b0-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="758b0-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="758b0-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="758b0-106">Vytvoření náhrady za zvláštní odpisy</span><span class="sxs-lookup"><span data-stu-id="758b0-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="758b0-107">Přejděte do části Dlouhodobý majetek > Nastavení > Náhrada za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="758b0-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="758b0-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="758b0-108">Click New.</span></span>
3. <span data-ttu-id="758b0-109">Zadejte hodnotu do pole Náhrada za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="758b0-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="758b0-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="758b0-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="758b0-111">V poli Procento zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="758b0-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="758b0-112">Pokud nebylo určeno procento, nastavte částku.</span><span class="sxs-lookup"><span data-stu-id="758b0-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="758b0-113">Přiřazení náhrady za zvláštní odpisy ke knize pro skupinu dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="758b0-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="758b0-114">Přejděte do části Dlouhodobý majetek > Nastavení > Skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="758b0-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="758b0-115">V seznamu vyberte skupinu dlouhodobého majetku, která je přiřazena k náhradě za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="758b0-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="758b0-116">Klepněte na Knihy.</span><span class="sxs-lookup"><span data-stu-id="758b0-116">Click Books.</span></span>
4. <span data-ttu-id="758b0-117">V seznamu vyberte knihu, která je přiřazena k náhradě za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="758b0-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="758b0-118">Klikněte na Náhrada za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="758b0-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="758b0-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="758b0-119">Click New.</span></span>
7. <span data-ttu-id="758b0-120">V poli Náhrada za zvláštní odpisy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="758b0-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="758b0-121">Výchozí hodnota pro procento nebo částku je převzatá z nastavení náhrady za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="758b0-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="758b0-122">V poli Priorita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="758b0-122">In the Priority field, enter a number.</span></span>

