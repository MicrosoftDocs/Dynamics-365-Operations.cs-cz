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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fed9f09b4e37da00a5d78fa088e8814db48456b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968922"
---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="bb341-103">Nastavení počátečního mimořádného odpisu</span><span class="sxs-lookup"><span data-stu-id="bb341-103">Set up bonus depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb341-104">Tento postup popisuje vytvoření nové náhrady za zvláštní odpisy a její přiřazení ke knize dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="bb341-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="bb341-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="bb341-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="bb341-106">Vytvoření náhrady za zvláštní odpisy</span><span class="sxs-lookup"><span data-stu-id="bb341-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="bb341-107">Přejděte do části Dlouhodobý majetek > Nastavení > Náhrada za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="bb341-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="bb341-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bb341-108">Click New.</span></span>
3. <span data-ttu-id="bb341-109">Zadejte hodnotu do pole Náhrada za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="bb341-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="bb341-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="bb341-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bb341-111">V poli Procento zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="bb341-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="bb341-112">Pokud nebylo určeno procento, nastavte částku.</span><span class="sxs-lookup"><span data-stu-id="bb341-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="bb341-113">Přiřazení náhrady za zvláštní odpisy ke knize pro skupinu dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="bb341-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="bb341-114">Přejděte do části Dlouhodobý majetek > Nastavení > Skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="bb341-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="bb341-115">V seznamu vyberte skupinu dlouhodobého majetku, která je přiřazena k náhradě za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="bb341-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="bb341-116">Klepněte na Knihy.</span><span class="sxs-lookup"><span data-stu-id="bb341-116">Click Books.</span></span>
4. <span data-ttu-id="bb341-117">V seznamu vyberte knihu, která je přiřazena k náhradě za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="bb341-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="bb341-118">Klikněte na Náhrada za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="bb341-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="bb341-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bb341-119">Click New.</span></span>
7. <span data-ttu-id="bb341-120">V poli Náhrada za zvláštní odpisy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bb341-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="bb341-121">Výchozí hodnota pro procento nebo částku je převzatá z nastavení náhrady za zvláštní odpisy.</span><span class="sxs-lookup"><span data-stu-id="bb341-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="bb341-122">V poli Priorita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bb341-122">In the Priority field, enter a number.</span></span>

