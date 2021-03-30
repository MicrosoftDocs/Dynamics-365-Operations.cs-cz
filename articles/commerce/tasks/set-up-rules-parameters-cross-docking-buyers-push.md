---
title: " Nastavení pravidel a parametrů pro cross docking a metodu buyer's push"
description: Tato procedura ukazuje postup vytváření pravidel doplnění.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d4cd276283483340f1dc0bc995cc9073a8aa9c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232682"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="c9324-103"> Nastavení pravidel a parametrů pro cross docking a metodu buyer's push</span><span class="sxs-lookup"><span data-stu-id="c9324-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9324-104">Tato procedura ukazuje postup vytváření pravidel doplnění.</span><span class="sxs-lookup"><span data-stu-id="c9324-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="c9324-105">Pravidla doplnění lze použít k řízení distribuce produktů do obchodů při použití metod cross docking a buyer´s push.</span><span class="sxs-lookup"><span data-stu-id="c9324-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="c9324-106">Pravidla doplnění lze nastavit pro obchody a skupiny obchodů.</span><span class="sxs-lookup"><span data-stu-id="c9324-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="c9324-107">Hmotnost definovaná pro jednotlivé řádky v pravidle bude určovat, jak bude množství produktů distribuováno mezi obchody při použití pravidel doplnění jako distribuční metody pro metodu cross docking a buyer´s push.</span><span class="sxs-lookup"><span data-stu-id="c9324-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="c9324-108">Tato procedura používá ukázkovou společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="c9324-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="c9324-109">Přejděte na Pravidla doplnění.</span><span class="sxs-lookup"><span data-stu-id="c9324-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="c9324-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="c9324-110">Click New.</span></span>
3. <span data-ttu-id="c9324-111">Zadejte hodnotu do pole Pravidlo doplnění.</span><span class="sxs-lookup"><span data-stu-id="c9324-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="c9324-112">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="c9324-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c9324-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c9324-113">Click Save.</span></span>
6. <span data-ttu-id="c9324-114">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c9324-114">Click Add.</span></span>
7. <span data-ttu-id="c9324-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c9324-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c9324-116">Můžete vybrat Hierarchie doplnění nebo Kanál pro typ.</span><span class="sxs-lookup"><span data-stu-id="c9324-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="c9324-117">Hodnota určuje, zda výběr v položce Název bude hierarchie kanálů nebo konkrétní kanál.</span><span class="sxs-lookup"><span data-stu-id="c9324-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="c9324-118">V tomto příkladu ponechejte nastavení Hierarchie doplnění.</span><span class="sxs-lookup"><span data-stu-id="c9324-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="c9324-119">Vyberte hodnotu v poli Název.</span><span class="sxs-lookup"><span data-stu-id="c9324-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="c9324-120">Výchozí hodnota hmotnosti se převezme od hmotnosti definované ve skladu.</span><span class="sxs-lookup"><span data-stu-id="c9324-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="c9324-121">Tuto hmotnost lze použít pro Pravidlo doplnění nebo můžete zadat novou hmotnost do pole Hmotnost.</span><span class="sxs-lookup"><span data-stu-id="c9324-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="c9324-122">Zadejte číslo do pole Hmotnost.</span><span class="sxs-lookup"><span data-stu-id="c9324-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="c9324-123">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c9324-123">Click Add.</span></span>
11. <span data-ttu-id="c9324-124">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c9324-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="c9324-125">V poli Typ vyberte možnost „Kanál“.</span><span class="sxs-lookup"><span data-stu-id="c9324-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="c9324-126">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c9324-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="c9324-127">Zadejte číslo do pole Hmotnost.</span><span class="sxs-lookup"><span data-stu-id="c9324-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="c9324-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c9324-128">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]