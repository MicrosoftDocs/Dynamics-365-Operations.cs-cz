--- 
title: "Vytvoření návrhu odpisování"
description: "Tento postup popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku."
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07d8cf2f1c46b99dfcd1d7c3419fe835f37c5a02
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="34fef-103">Vytvoření návrhu odpisování</span><span class="sxs-lookup"><span data-stu-id="34fef-103">Create a depreciation proposal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34fef-104">Tento postup popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="34fef-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="34fef-105">Tato úloha používá ukázkovou společnost USMF a účetní role.</span><span class="sxs-lookup"><span data-stu-id="34fef-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="34fef-106">Vytvořit návrh odpisu</span><span class="sxs-lookup"><span data-stu-id="34fef-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="34fef-107">Přejděte na Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu.</span><span class="sxs-lookup"><span data-stu-id="34fef-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="34fef-108">V poli Název deníku kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="34fef-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="34fef-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="34fef-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="34fef-110">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="34fef-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="34fef-111">Výběrem možnosti Shrnout odpisy shrnete měsíční odpisy do jednoho řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="34fef-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="34fef-112">Například pokud hodnota Do data je 31. března 2015, vygeneruje se následující popis: Odpis od 31. ledna 2015.</span><span class="sxs-lookup"><span data-stu-id="34fef-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="34fef-113">Pole data na navržených řádcích deníku bude potom nastaveno na 31. března 2015.</span><span class="sxs-lookup"><span data-stu-id="34fef-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="34fef-114">Návrhy odpisu mohou být filtrovány podle majetku, skupiny majetku nebo jiných kritérií pomocí možnosti Filtrování.</span><span class="sxs-lookup"><span data-stu-id="34fef-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="34fef-115">Pokud použijete formulář Vytvořit návrhy pořízení nebo spotřeby pro dlouhodobý majetek, můžete navrhnout odpisy v dávkách.</span><span class="sxs-lookup"><span data-stu-id="34fef-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="34fef-116">To je doporučováno pro větší návrhy, které používají více systémových prostředků.</span><span class="sxs-lookup"><span data-stu-id="34fef-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="34fef-117">Pokud vyberete možnost dávky, můžete během této doby stále provádět jiné úlohy.</span><span class="sxs-lookup"><span data-stu-id="34fef-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="34fef-118">Při návrhu odpisu tímto způsobem se počítají odpisy pro oceňovací modely pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="34fef-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="34fef-119">Klikněte na Vytvoří deník.</span><span class="sxs-lookup"><span data-stu-id="34fef-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="34fef-120">Zkontrolování položek odpisů</span><span class="sxs-lookup"><span data-stu-id="34fef-120">Review depreciation entries</span></span>
1. <span data-ttu-id="34fef-121">Přejděte na Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="34fef-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="34fef-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="34fef-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="34fef-123">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="34fef-123">Click Lines.</span></span>
4. <span data-ttu-id="34fef-124">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="34fef-124">Click Post.</span></span>


