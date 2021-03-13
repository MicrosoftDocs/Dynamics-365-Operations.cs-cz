---
title: Schválení dodavatelů pro konkrétní kategorie zásobování
description: V tomto tématu je vysvětleno, jak schválit dodavatele pro určité kategorie zásobování v aplikaci Dynamics 365 Supply Chain Management.
author: RichardLuan
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 159d918a4dd3b6502bc8ab411d0353545eb4fcba
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016342"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a><span data-ttu-id="d0a84-103">Schválení dodavatelů pro konkrétní kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="d0a84-103">Approve vendors for specific procurement categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0a84-104">V tomto tématu je vysvětleno, jak schválit dodavatele pro určité kategorie zásobování v aplikaci Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d0a84-104">This topic explains how to approve vendors for specific procurement categories in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d0a84-105">Při vytvoření nákupního požadavku může být existovat požadavek vybrat schválené nebo upřednostňované dodavatele v závislosti na tom, jak jsou zásady nákupu nastaveny.</span><span class="sxs-lookup"><span data-stu-id="d0a84-105">When a purchase requisition is created, there may be a requirement to select an approved or preferred vendor, depending on how the purchasing policies are set up.</span></span> <span data-ttu-id="d0a84-106">Tento postup popisuje, jak určit, že je dodavatel schválený nebo upřednostňovaný pro specifickou kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="d0a84-106">This procedure shows you how to specify that a vendor is approved or preferred for a specific procurement category.</span></span> <span data-ttu-id="d0a84-107">Tento úkol by obvykle prováděl zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="d0a84-107">This task would usually be carried out by a procurement professional.</span></span> <span data-ttu-id="d0a84-108">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d0a84-108">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="d0a84-109">V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Dodavatelé > Všichni dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-109">In the navigation pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="d0a84-110">Vyberte dodavatele, kterého chcete nastavit jako schváleného nebo upřednostňovaného dodavatele pro kategorii.</span><span class="sxs-lookup"><span data-stu-id="d0a84-110">Select the vendor that you want to set as an approved or preferred vendor for a category.</span></span>
3. <span data-ttu-id="d0a84-111">V podokně akcí klikněte na možnost **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-111">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="d0a84-112">Zvolte **Kategorie**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-112">Select **Categories**.</span></span>
5. <span data-ttu-id="d0a84-113">Zvolte **Přidat kategorii**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-113">Select **Add category**.</span></span>
6. <span data-ttu-id="d0a84-114">V poli **Kategorie** zaškrtněte **KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-114">In the **Category** field, select **OFFICE AND DESK ACCESSORIES (OFFICE AND DESK ACCESSORIES)**.</span></span>
7. <span data-ttu-id="d0a84-115">V poli **Stav kategorie dodavatele** vyberte **Upřednostňované**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-115">In the **Vendor category status** field, select **Preferred**.</span></span> <span data-ttu-id="d0a84-116">Je možné zadat více než jednoho upřednostněného dodavatele pro kategorii.</span><span class="sxs-lookup"><span data-stu-id="d0a84-116">It's possible to specify more than one preferred vendor for a category.</span></span>  
8. <span data-ttu-id="d0a84-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-117">Select **Save**.</span></span>
9. <span data-ttu-id="d0a84-118">V navigačním podokně přejděte na **Moduly > Zásobování a zdroje > Kategorie zásobování**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-118">In the navigation pane, go to **Modules > Procurement and sourcing > Procurement categories**.</span></span>
10. <span data-ttu-id="d0a84-119">Ve stromovém zobrazení vyberte **KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI\KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-119">In the tree, select **CORP PROCUREMENT CATEGORIES\OFFICE AND DESK ACCESSORIES**.</span></span>
11. <span data-ttu-id="d0a84-120">Rozbalte sekci **Dodavatelé**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-120">Expand the **Vendors** section.</span></span> <span data-ttu-id="d0a84-121">Zkontrolujte, zda se vámi vybraný dodavatel zobrazí jako upřednostněný dodavatel pro kategorii Kancelářské a stolní příslušenství.</span><span class="sxs-lookup"><span data-stu-id="d0a84-121">Check if the vendor that you selected appears as a preferred vendor for the Office and desk accessories category.</span></span> <span data-ttu-id="d0a84-122">Pokud tento postup používáte jako průvodce úkolem, může být nutné zvolit **Odemknout** a umožnit procházení seznamem dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="d0a84-122">If you're running this procedure as a task guide, you may have to select the **Unlock** button to be able to scroll down to the list of vendors.</span></span>  <span data-ttu-id="d0a84-123">Také je možné přidat upřednostňované a schválené dodavatele na této stránce.</span><span class="sxs-lookup"><span data-stu-id="d0a84-123">It's also possible to add preferred and approved vendors on this page.</span></span>  
12. <span data-ttu-id="d0a84-124">Ve stromové struktuře rozbalte **KANCELÁŘSKÉ A STOLNÍ PŘÍSLUŠENSTVÍ** a vyberte **Nůžky**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-124">In the tree, expand **OFFICE AND DESK ACCESSORIES** and select **Scissors**.</span></span>
13. <span data-ttu-id="d0a84-125">Vyberte **Ne** v poli **Zdědit dodavatele z nadřazené kategorie:**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-125">Select **No** in the **Inherit vendors from parent category:** field.</span></span>
14. <span data-ttu-id="d0a84-126">Vyberte **Ano** v poli **Zdědit dodavatele z nadřazené kategorie:**.</span><span class="sxs-lookup"><span data-stu-id="d0a84-126">Select **Yes** in the **Inherit vendors from parent category:** field.</span></span>

