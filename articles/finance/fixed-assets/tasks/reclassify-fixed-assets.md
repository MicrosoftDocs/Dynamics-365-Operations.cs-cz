---
title: Přeřazení dlouhodobého majetku
description: Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd108f2e778b31749c66b2787d9f59467cae97dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441089"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="f5d7b-103">Přeřazení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="f5d7b-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5d7b-104">Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="f5d7b-105">Když je dlouhodobý majetek reklasifikován:</span><span class="sxs-lookup"><span data-stu-id="f5d7b-105">When a fixed asset is reclassified:</span></span>

* <span data-ttu-id="f5d7b-106">Pro nový dlouhodobý majetek budou vytvořeny všechny knihy pro existující dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="f5d7b-107">Veškeré informace nastavené pro původní dlouhodobý majetek se zkopírují do nového dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="f5d7b-108">Stav knih původního dlouhodobého majetku je Zavřeno.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-108">The status of the books for the original fixed asset is Closed.</span></span> 

* <span data-ttu-id="f5d7b-109">Nové knihy nového dlouhodobého majetku budou mít v poli **Datum pořízení** uvedeno datum reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-109">The new books of the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="f5d7b-110">Datum v poli **Datum zahájení odpisu** bude zkopírováno z původních informací o majetku.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="f5d7b-111">Pokud již byl zahájen odpis, zobrazí se v poli **Datum posledního odpisu** datum reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

* <span data-ttu-id="f5d7b-112">Existující transakce dlouhodobého majetku pro původní dlouhodobý majetek jsou zrušeny a opětovně vytvořeny pro nový dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

<span data-ttu-id="f5d7b-113">Chcete-li reklasifikovat dlouhodobý majetek, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f5d7b-113">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="f5d7b-114">Přejděte na **Dlouhodobý majetek > Pravidelné úlohy > Reklasifikace.**</span><span class="sxs-lookup"><span data-stu-id="f5d7b-114">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="f5d7b-115">V poli **Skupina dlouhodobého majetku** zvolte skupinu, která má být reklasifikována.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-115">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="f5d7b-116">V poli **Číslo dlouhodobého majetku** zvolte dlouhodobý majetek určený k reklasifikaci.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-116">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="f5d7b-117">V poli **Nová skupina dlouhodobého majetku** vyberte skupinu, do které chcete dlouhodobý majetek převést.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-117">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="f5d7b-118">Jestliže je nová skupina dlouhodobého majetku přiřazena k číselné řadě, pole **Nové číslo dlouhodobého majetku** se aktualizuje číslem z číselné řady nové skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-118">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="f5d7b-119">V opačném případě se pole **Nové číslo dlouhodobého majetku** aktualizuje číslem z číselné řady, která je nastavena na stránce **Parametry dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-119">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="f5d7b-120">Pokud na stránce **Parametry dlouhodobého majetku** není nastavena číselná řada, zadejte číslo do pole **Nové číslo dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-120">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="f5d7b-121">Do pole **Datum reklasifikace** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-121">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="f5d7b-122">V poli **Číselná řada dokladů** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-122">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="f5d7b-123">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5d7b-123">Click **OK**.</span></span>
