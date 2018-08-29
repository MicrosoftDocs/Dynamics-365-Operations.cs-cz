--- 
title: "Vytvoření pokladního místa (pokladen)"
description: "Tento postup demonstruje vytvoření pokladních míst."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: b477b201df62c9fbbbb18978a4a15fa3b4a964ae
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="create-point-of-sale-registers"></a><span data-ttu-id="24996-103">Vytvoření pokladního místa (pokladen)</span><span class="sxs-lookup"><span data-stu-id="24996-103">Create point of sale (registers)</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="24996-104">Tento postup demonstruje vytvoření pokladních míst.</span><span class="sxs-lookup"><span data-stu-id="24996-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="24996-105">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="24996-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="24996-106">Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Nastavení POS > Pokladny.</span><span class="sxs-lookup"><span data-stu-id="24996-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="24996-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="24996-107">Click New.</span></span>
3. <span data-ttu-id="24996-108">Do pole Číslo pokladny zadejte ID nové pokladny.</span><span class="sxs-lookup"><span data-stu-id="24996-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="24996-109">ID registrace obvykle obsahuje kódy, které pomáhají mapovat pokladu s obchodem, do které patří, a skladové místo v obchodě.</span><span class="sxs-lookup"><span data-stu-id="24996-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="24996-110">Do pole Název zadejte popisný název pokladny.</span><span class="sxs-lookup"><span data-stu-id="24996-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="24996-111">V poli Číslo obchodu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="24996-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="24996-112">V poli Profil hardwaru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="24996-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="24996-113">Profily hardwaru umožňují zadat maloobchodní periferní zařízení, která budou připojena k pokladně, jako je například zásuvka a tiskárna účtenek.</span><span class="sxs-lookup"><span data-stu-id="24996-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="24996-114">V poli Vizuální profil zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="24996-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="24996-115">Vizuální profily se používají k určení obrázků použitých na pozadí pokladny a přihlašovací stránky, jakož i motivů pro pokladny.</span><span class="sxs-lookup"><span data-stu-id="24996-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="24996-116">Zadejte hodnotu do pole Číslo registrační pokladny POS EFT.</span><span class="sxs-lookup"><span data-stu-id="24996-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="24996-117">Číslo pokladny EFT POS umožňuje informovat procesor plateb o tom, který platební terminál odesílá autorizace požadavků.</span><span class="sxs-lookup"><span data-stu-id="24996-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="24996-118">Tato hodnota se nazývá často "ID terminálu" nebo "TID".</span><span class="sxs-lookup"><span data-stu-id="24996-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="24996-119">TID lze běžně nalézt na štítku na platebním zařízení.</span><span class="sxs-lookup"><span data-stu-id="24996-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="24996-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="24996-120">Click Save.</span></span>


