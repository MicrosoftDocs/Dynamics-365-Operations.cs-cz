--- 
title: "Přeřazení dlouhodobého majetku"
description: "Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo."
author: saraschi2
manager: AnnBe
ms.date: 06/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fda4d71b050edde2752536985b18ebcad203d078
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="5763f-103">Přeřazení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="5763f-103">Reclassify fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5763f-104">Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.</span><span class="sxs-lookup"><span data-stu-id="5763f-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="5763f-105">Když je dlouhodobý majetek reklasifikován:</span><span class="sxs-lookup"><span data-stu-id="5763f-105">When a fixed asset is reclassified:</span></span>

<span data-ttu-id="5763f-106">• Pro nový dlouhodobý majetek budou vytvořeny všechny oceňovací modely existujícího dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5763f-106">• All value models for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="5763f-107">Veškeré informace nastavené pro původní dlouhodobý majetek se zkopírují do nového dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5763f-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="5763f-108">Stav oceňovacích modelů původního dlouhodobého majetku je uzavřen.</span><span class="sxs-lookup"><span data-stu-id="5763f-108">The status of the value models for the original fixed asset is Closed.</span></span> 

<span data-ttu-id="5763f-109">• Nové oceňovací modely nového dlouhodobého majetku budou mít v poli Datum pořízení uvedeno datum reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="5763f-109">• The new value models of the new fixed asset contain the date of the reclassification in the Acquisition date field.</span></span> <span data-ttu-id="5763f-110">Datum v poli Datum zahájení odpisu bude zkopírováno z původních údajů o aktivech.</span><span class="sxs-lookup"><span data-stu-id="5763f-110">The date in the Depreciation run date field is copied from the original asset information.</span></span> <span data-ttu-id="5763f-111">Pokud již byl zahájen odpis, zobrazí se v poli Datum zahájení odpisu datum reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="5763f-111">If the depreciation has already started, the Date when depreciation was last run field displays the date of the reclassification.</span></span> 

<span data-ttu-id="5763f-112">• Existující transakce dlouhodobého majetku pro původní dlouhodobý majetek jsou zrušeny a opětovně vytvořeny pro nový dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="5763f-112">• The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

1. <span data-ttu-id="5763f-113">Přejděte na Dlouhodobý majetek > Pravidelné úlohy > Reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="5763f-113">Go to Fixed assets > Periodic tasks > Reclassification.</span></span>
2. <span data-ttu-id="5763f-114">V poli Skupina dlouhodobého majetku zvolte skupinu, která má být reklasifikována.</span><span class="sxs-lookup"><span data-stu-id="5763f-114">In the Fixed asset group field, selet the group to reclassify.</span></span>
3. <span data-ttu-id="5763f-115">V poli Číslo dlouhodobého majetku zvolte dlouhodobý majetek určený k reklasifikaci.</span><span class="sxs-lookup"><span data-stu-id="5763f-115">In the Fixed asset number field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="5763f-116">V poli Nová skupina dlouhodobého majetku vyberte skupinu, do které chcete dlouhodobý majetek převést.</span><span class="sxs-lookup"><span data-stu-id="5763f-116">In the New fixed asset group field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="5763f-117">Jestliže je nová skupina dlouhodobého majetku přiřazena k číselné řadě, pole Nové číslo dlouhodobého majetku se aktualizuje číslem z číselné řady nové skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5763f-117">If the new fixed asset group is attached to a number sequence, the New fixed asset number field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="5763f-118">V opačném případě se pole Nové číslo dlouhodobého majetku aktualizuje číslem z číselné řady, která je nastavena na stránce Parametry dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5763f-118">Otherwise, the New fixed asset number field is updated with the number from the number sequence that is set up in the Fixed asset parameters page.</span></span> <span data-ttu-id="5763f-119">Pokud na stránce Parametry dlouhodobého majetku není nastavena číselná řada, zadejte číslo do pole Nové číslo dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="5763f-119">If a number sequence is not set up in the Fixed asset parameters page, enter a number in the New fixed asset number field.</span></span>  
5. <span data-ttu-id="5763f-120">Do pole Datum reklasifikace zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="5763f-120">In the Reclassification date field, enter a date.</span></span>
6. <span data-ttu-id="5763f-121">V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5763f-121">In the Voucher series field, enter or select a value.</span></span>
7. <span data-ttu-id="5763f-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5763f-122">Click OK.</span></span>


