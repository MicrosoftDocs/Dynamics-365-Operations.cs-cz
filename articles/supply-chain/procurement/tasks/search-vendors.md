---
title: Vyhledání dodavatelů
description: Zjistěte, jak vyhledávat dodavatele na základě specifických kritérií.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc28deb979fe8dc4e31befe6d4d5f6f91388f13e
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018045"
---
# <a name="search-for-vendors"></a><span data-ttu-id="71649-103">Vyhledání dodavatelů</span><span class="sxs-lookup"><span data-stu-id="71649-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71649-104">Zjistěte, jak vyhledávat dodavatele na základě specifických kritérií.</span><span class="sxs-lookup"><span data-stu-id="71649-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="71649-105">Tento příklad ukazuje, jak vyhledávat dodavatele, kteří byli schváleni pro určitou kategorii zásobování a mají primární adresu v určité zemi.</span><span class="sxs-lookup"><span data-stu-id="71649-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="71649-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="71649-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="71649-107">Tento úkol by obvykle prováděl zásobovací pracovník.</span><span class="sxs-lookup"><span data-stu-id="71649-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="71649-108">Přejděte do nabídky Zásobování a zdroje > Dodavatelé > Hledání dodavatele.</span><span class="sxs-lookup"><span data-stu-id="71649-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="71649-109">Kliknutím na znaménko Plus otevřete stránku Výběr kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="71649-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="71649-110">Ve stromovém zobrazení vyberte “KATEGORIE ZÁSOBOVÁNÍ SPOLEČNOSTI\KANCELÁŘSKÉ POČÍTAČE“.</span><span class="sxs-lookup"><span data-stu-id="71649-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="71649-111">Pokud tento postup provádíte jako průvodce úkolem, možná bude třeba kliknout na tlačítko Odemknout a až potom vybrat správný uzel.</span><span class="sxs-lookup"><span data-stu-id="71649-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="71649-112">Pokud nepoužíváte data USMF, vyberte jednu z kategorií, kterou máte.</span><span class="sxs-lookup"><span data-stu-id="71649-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="71649-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="71649-113">Click Add.</span></span>
    * <span data-ttu-id="71649-114">Zde lze vybrat více než jednu kategorii.</span><span class="sxs-lookup"><span data-stu-id="71649-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="71649-115">Pokud tak učiníte, hledání vrátí všechny dodavatele, kteří byli schváleni alespoň pro jednu z kategorií.</span><span class="sxs-lookup"><span data-stu-id="71649-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="71649-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="71649-116">Click OK.</span></span>
6. <span data-ttu-id="71649-117">V poli Země/oblast zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="71649-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="71649-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="71649-118">Click OK.</span></span>

