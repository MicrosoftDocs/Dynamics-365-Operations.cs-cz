--- 
title: "Vytvoření typů oslovení a kritérií hodnocení pro požadavky na nabídku"
description: "Tato příručka popisuje způsob vytvoření typu oslovení a jeho přiřazení k metodě hodnocení."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 095855d552d228375635bdbaa9fca37c47a3b952
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="7a0c8-103">Vytvoření typů oslovení a kritérií hodnocení pro požadavky na nabídku</span><span class="sxs-lookup"><span data-stu-id="7a0c8-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a0c8-104">Tato příručka popisuje způsob vytvoření typu oslovení a jeho přiřazení k metodě hodnocení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="7a0c8-105">Rovněž zobrazuje způsob použití typu oslovení pro požadavek na nabídku, který stanoví výchozí metodu hodnocení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="7a0c8-106">Tyto úkoly obvykle provádějí vedoucí nákupu.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="7a0c8-107">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7a0c8-108">Před zahájením je nutné mít k dispozici metodu hodnocení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="7a0c8-109">Vytvořit nový typ oslovení</span><span class="sxs-lookup"><span data-stu-id="7a0c8-109">Create a solicitation type</span></span>
1. <span data-ttu-id="7a0c8-110">Přejděte na Zásobování a zdroje > Nastavení > Požadavek na nabídku > Typ oslovení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="7a0c8-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-111">Click New.</span></span>
3. <span data-ttu-id="7a0c8-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="7a0c8-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7a0c8-114">V poli Metoda hodnocení vyberte metodu hodnocení, kterou chcete pro tento typ oslovení použít.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="7a0c8-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-115">Click Save.</span></span>
7. <span data-ttu-id="7a0c8-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="7a0c8-117">Použití typu oslovení</span><span class="sxs-lookup"><span data-stu-id="7a0c8-117">Use the solicitation type</span></span>
1. <span data-ttu-id="7a0c8-118">Přejděte na Zásobování a zdroje > Požadavky na nabídky > Všechny požadavky na nabídky.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="7a0c8-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-119">Click New.</span></span>
3. <span data-ttu-id="7a0c8-120">V poli Typ oslovení vyberte typ oslovení, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
4. <span data-ttu-id="7a0c8-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-121">Click OK.</span></span>
5. <span data-ttu-id="7a0c8-122">Klikněte na Kritéria hodnocení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="7a0c8-123">Zobrazená kritéria hodnocení jsou ta z metody hodnocení, která je přidružena k typu oslovení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="7a0c8-124">Na této stránce je možné přidat nebo odstranit kritérií.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="7a0c8-125">Dále je možné přidat nová kritéria kopírováním z jiné metody hodnocení.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="7a0c8-126">Klikněte na Kopírovat kritéria.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="7a0c8-127">V poli Metoda hodnocení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="7a0c8-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-128">Click OK.</span></span>
9. <span data-ttu-id="7a0c8-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7a0c8-129">Close the page.</span></span>


