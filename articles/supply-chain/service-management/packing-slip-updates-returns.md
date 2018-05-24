---
title: "Aktualizace dodacího listu pro vrácení"
description: "Před přijetím vrácených položek na sklad je nutné aktualizovat dodací list objednávky, do které náleží."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7532c5b1debdb498c2d6bab129208a412387c8fa
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="585e5-103">Aktualizace dodacího listu pro vrácení</span><span class="sxs-lookup"><span data-stu-id="585e5-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="585e5-104">Před přijetím vrácených položek na sklad je nutné aktualizovat dodací list objednávky, do které náleží.</span><span class="sxs-lookup"><span data-stu-id="585e5-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="585e5-105">Stejně jako je proces aktualizace faktury aktualizací finanční transakce, proces aktualizace dodacího listu je fyzickou aktualizací skladového záznamu a potvrzuje tedy změny zásob.</span><span class="sxs-lookup"><span data-stu-id="585e5-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="585e5-106">V případě vrácení jsou kroky přiřazené k dispoziční akci implementovány v průběhu aktualizace dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="585e5-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="585e5-107">Aktualizaci dodacího listu lze zpracovat buď v deníku doručení položek, nebo ve vratce.</span><span class="sxs-lookup"><span data-stu-id="585e5-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="585e5-108">Jako součást procesu účtování dodacích listů lze volitelně přiřadit referenční číslo dodacího listu z přepravních dokumentů odběratele k řádkům objednávky.</span><span class="sxs-lookup"><span data-stu-id="585e5-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="585e5-109">Toto přiřazení je nepovinné a má pouze informativní charakter.</span><span class="sxs-lookup"><span data-stu-id="585e5-109">This association is optional and for reference only.</span></span> <span data-ttu-id="585e5-110">Nevytváří žádné aktualizace transakcí.</span><span class="sxs-lookup"><span data-stu-id="585e5-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="585e5-111">Pokud nebyly dodány všechny očekávané vrácené položky, měli byste zadat pouze množství obdržené v aktualizaci dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="585e5-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="585e5-112">Ponechte zbývající položky na objednávce, dokud nebudou dodána zbylá část vrácené dodávky.</span><span class="sxs-lookup"><span data-stu-id="585e5-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="585e5-113">Při odeslání položky zpět z karantény do oddělení expedice a příjmu, například pokud karanténní inspektor neobdrží informace k uložení položek na skladu, je dále nutné aktualizovat odpovídající dodací list, aby došlo ke správné registraci a reakci na dispoziční kód, který byl zadán jako výsledek karantény.</span><span class="sxs-lookup"><span data-stu-id="585e5-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="585e5-114">Při aktualizaci dodacího listu pro vrácenou položku, která pochází z prodejní smlouvy, je závazek prodejní smlouvy pro danou položku automaticky aktualizován tak, aby odrážel změnu množství nebo částky.</span><span class="sxs-lookup"><span data-stu-id="585e5-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="585e5-115">Viz také</span><span class="sxs-lookup"><span data-stu-id="585e5-115">See also</span></span>

[<span data-ttu-id="585e5-116">Provádění aktualizací faktur pro vrácení</span><span class="sxs-lookup"><span data-stu-id="585e5-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  



