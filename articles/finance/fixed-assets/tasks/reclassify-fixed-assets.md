---
title: Přeřazení dlouhodobého majetku
description: Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944704"
---
# <a name="reclassify-fixed-assets"></a><span data-ttu-id="3c41e-103">Přeřazení dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="3c41e-103">Reclassify fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3c41e-104">Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.</span><span class="sxs-lookup"><span data-stu-id="3c41e-104">To reclassify a fixed asset, you must transfer it to a new fixed asset group or assign a new fixed asset number to it in the same group.</span></span> 

<span data-ttu-id="3c41e-105">Když je dlouhodobý majetek reklasifikován:</span><span class="sxs-lookup"><span data-stu-id="3c41e-105">When a fixed asset is reclassified:</span></span>

- <span data-ttu-id="3c41e-106">Pro nový dlouhodobý majetek budou vytvořeny všechny knihy pro existující dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="3c41e-106">All books for the existing fixed asset are created for the new fixed asset.</span></span> <span data-ttu-id="3c41e-107">Veškeré informace nastavené pro původní dlouhodobý majetek se zkopírují do nového dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3c41e-107">Any information that was set up for the original fixed asset is copied to the new fixed asset.</span></span> <span data-ttu-id="3c41e-108">Stav knih původního dlouhodobého majetku je Zavřeno.</span><span class="sxs-lookup"><span data-stu-id="3c41e-108">The status of the books for the original fixed asset is Closed.</span></span> 

- <span data-ttu-id="3c41e-109">Nové knihy nového dlouhodobého majetku budou mít v poli **Datum pořízení** uvedeno datum reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="3c41e-109">The new books for the new fixed asset contain the date of the reclassification in the **Acquisition date** field.</span></span> <span data-ttu-id="3c41e-110">Datum v poli **Datum zahájení odpisu** bude zkopírováno z původních informací o majetku.</span><span class="sxs-lookup"><span data-stu-id="3c41e-110">The date in the **Depreciation run date** field is copied from the original asset information.</span></span> <span data-ttu-id="3c41e-111">Pokud již byl zahájen odpis, zobrazí se v poli **Datum posledního odpisu** datum reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="3c41e-111">If the depreciation has already started, the **Date when depreciation was last run** field displays the date of the reclassification.</span></span> 

- <span data-ttu-id="3c41e-112">Existující transakce dlouhodobého majetku pro původní dlouhodobý majetek jsou zrušeny a opětovně vytvořeny pro nový dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="3c41e-112">The existing fixed asset transactions for the original fixed asset are canceled and regenerated for the new fixed asset.</span></span>

- <span data-ttu-id="3c41e-113">Když je majetek, který má transakci převodu, překlasifikován, systém zobrazí zprávu v možnosti **Centrum akcí** k označení, že transakce převodu nebyla dokončena během procesu reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="3c41e-113">When an asset that has a transfer transaction has been reclassified, the system will display a message in the **Action center** to indicate that a transfer transaction wasn't completed during the reclassification process.</span></span> <span data-ttu-id="3c41e-114">Je nutné dokončit transakci převodu, abyste přesunuli existující transakce reklasifikace do příslušných finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="3c41e-114">It's necessary to complete a transfer transaction to move the existing reclassification transactions to the appropriate financial dimensions.</span></span> 

   <span data-ttu-id="3c41e-115">Během procesu reklasifikace provede systém následující akce, které reklasifikují zůstatek majetku z původního na nový.</span><span class="sxs-lookup"><span data-stu-id="3c41e-115">During the reclassification process, the system runs the following actions to reclassify the asset balance from the original asset to the new asset.</span></span> 
   
   - <span data-ttu-id="3c41e-116">Proces reklasifikace zkopíruje data z původní knihy dlouhodobého majetku do nové knihy dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3c41e-116">The reclassification process copies the data from the original fixed asset book to the new fixed asset book.</span></span>

   - <span data-ttu-id="3c41e-117">Transakce reklasifikace používá informace z původní zaúčtované akvizice, které zahrnují informace o finanční dimenzi, které jsou zahrnuty v transakci pořízení.</span><span class="sxs-lookup"><span data-stu-id="3c41e-117">The reclassification transaction uses information from the original posted acquisition that includes financial dimension information that is included in the acquisition transaction.</span></span>  
   
   - <span data-ttu-id="3c41e-118">Proces reklasifikace zároveň obrací původní transakci pořízení a transakci převodu majetku.</span><span class="sxs-lookup"><span data-stu-id="3c41e-118">At the same time, the reclassification process reverses the original asset acquisition and asset transfer transaction.</span></span> 

<span data-ttu-id="3c41e-119">Následující diagram a postup poskytují příklad procesu reklasifikace.</span><span class="sxs-lookup"><span data-stu-id="3c41e-119">The following diagram and procedure provide an example of the reclassification process.</span></span> 

<span data-ttu-id="3c41e-120">[![Schéma znázorňující proces reklasifikace](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span><span class="sxs-lookup"><span data-stu-id="3c41e-120">[![Diagram showing the reclassicification process](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)</span></span>

<span data-ttu-id="3c41e-121">Chcete-li reklasifikovat dlouhodobý majetek, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="3c41e-121">Follow these steps to reclassify a fixed asset:</span></span>

1. <span data-ttu-id="3c41e-122">Přejděte na **Dlouhodobý majetek > Pravidelné úlohy > Reklasifikace.**</span><span class="sxs-lookup"><span data-stu-id="3c41e-122">Go to **Fixed assets > Periodic tasks > Reclassification.**</span></span>
2. <span data-ttu-id="3c41e-123">V poli **Skupina dlouhodobého majetku** zvolte skupinu, která má být reklasifikována.</span><span class="sxs-lookup"><span data-stu-id="3c41e-123">In the **Fixed asset group** field, select the group to reclassify.</span></span>
3. <span data-ttu-id="3c41e-124">V poli **Číslo dlouhodobého majetku** zvolte dlouhodobý majetek určený k reklasifikaci.</span><span class="sxs-lookup"><span data-stu-id="3c41e-124">In the **Fixed asset number** field, select the fixed asset to reclassify.</span></span>
4. <span data-ttu-id="3c41e-125">V poli **Nová skupina dlouhodobého majetku** vyberte skupinu, do které chcete dlouhodobý majetek převést.</span><span class="sxs-lookup"><span data-stu-id="3c41e-125">In the **New fixed asset group** field, select a group to transfer the fixed asset to.</span></span>
    * <span data-ttu-id="3c41e-126">Jestliže je nová skupina dlouhodobého majetku přiřazena k číselné řadě, pole **Nové číslo dlouhodobého majetku** se aktualizuje číslem z číselné řady nové skupiny dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="3c41e-126">If the new fixed asset group is attached to a number sequence, the **New fixed asset number** field is updated with the number from the new fixed asset group number sequence.</span></span> <span data-ttu-id="3c41e-127">V opačném případě se pole **Nové číslo dlouhodobého majetku** aktualizuje číslem z číselné řady, která je nastavena na stránce **Parametry dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-127">Otherwise, the **New fixed asset number** field is updated with the number from the number sequence that is set up on the **Fixed asset parameters** page.</span></span> <span data-ttu-id="3c41e-128">Pokud na stránce **Parametry dlouhodobého majetku** není nastavena číselná řada, zadejte číslo do pole **Nové číslo dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-128">If a number sequence is not set up on the **Fixed asset parameters** page, enter a number in the **New fixed asset number** field.</span></span>  
5. <span data-ttu-id="3c41e-129">Do pole **Datum reklasifikace** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="3c41e-129">In the **Reclassification date** field, enter a date.</span></span>
6. <span data-ttu-id="3c41e-130">V poli **Číselná řada dokladů** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3c41e-130">In the **Voucher series** field, enter or select a value.</span></span>
7. <span data-ttu-id="3c41e-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c41e-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
