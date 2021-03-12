---
title: Vytvoření návrhu odpisování
description: Toto téma popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3d62e982d26afbec7ac04dd80592a73f4a3286f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968896"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="f8c8b-103">Vytvoření návrhu odpisování</span><span class="sxs-lookup"><span data-stu-id="f8c8b-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8c8b-104">Toto téma popisuje způsob dávkové nabídky práce odpisů a vysvětluje postup při návrhu odpisu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="f8c8b-105">Tato úloha používá ukázkovou společnost USMF a účetní role.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="f8c8b-106">Vytvoření návrhu odpisování</span><span class="sxs-lookup"><span data-stu-id="f8c8b-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="f8c8b-107">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Vytvořit návrh odpisu**.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="f8c8b-108">V poli **Název deníku** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="f8c8b-109">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="f8c8b-110">Výběrem možnosti **Shrnout odpisy** shrnete měsíční odpisy do jednoho řádku deníku.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="f8c8b-111">Například pokud hodnota Do data je 31. března 2015, vygeneruje se následující popis: "Odpis od 31. ledna 2015."</span><span class="sxs-lookup"><span data-stu-id="f8c8b-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="f8c8b-112">Pole **Datum** na navržených řádcích deníku bude potom nastaveno na 31. března 2015.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="f8c8b-113">Návrhy odpisu mohou být filtrovány podle majetku, skupiny majetku nebo jiných kritérií pomocí možnosti **Filtrování**.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="f8c8b-114">Pokud použijete formulář **Vytvořit návrhy pořízení nebo spotřeby pro dlouhodobý majetek**, můžete navrhnout odpisy v dávkách.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="f8c8b-115">To je doporučováno pro větší návrhy, které používají více systémových prostředků.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="f8c8b-116">Pokud vyberete možnost dávky, můžete během této doby stále provádět jiné úlohy.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="f8c8b-117">Při návrhu odpisu tímto způsobem se počítají odpisy pro oceňovací modely pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="f8c8b-118">Vyberte **Vytvořit deník**.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="f8c8b-119">Zkontrolování položek odpisů</span><span class="sxs-lookup"><span data-stu-id="f8c8b-119">Review depreciation entries</span></span>
1. <span data-ttu-id="f8c8b-120">V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Položky deníku > Deník dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="f8c8b-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f8c8b-122">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-122">Select **Lines**.</span></span>
4. <span data-ttu-id="f8c8b-123">Zvolte **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="f8c8b-123">Select **Post**.</span></span>

