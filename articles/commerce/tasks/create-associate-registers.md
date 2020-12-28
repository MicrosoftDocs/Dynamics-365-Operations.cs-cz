---
title: " Vytvoření a přidružení pokladen"
description: Tento postup demonstruje vytvoření pokladních míst.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 001bdd61f9266798dadae2ac7c96a4f4c19dbb94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410842"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="6b004-103"> Vytvoření a přidružení pokladen</span><span class="sxs-lookup"><span data-stu-id="6b004-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b004-104">Tento postup demonstruje vytvoření pokladních míst.</span><span class="sxs-lookup"><span data-stu-id="6b004-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="6b004-105">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="6b004-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="6b004-106">Přejděte do nabídky Retail and Commerce > Nastavení kanálu > Nastavení POS > Pokladny.</span><span class="sxs-lookup"><span data-stu-id="6b004-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="6b004-107">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="6b004-107">Click New.</span></span>
3. <span data-ttu-id="6b004-108">Do pole Číslo pokladny zadejte ID nové pokladny.</span><span class="sxs-lookup"><span data-stu-id="6b004-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="6b004-109">ID registrace obvykle obsahuje kódy, které pomáhají mapovat pokladu s obchodem, do které patří, a skladové místo v obchodě.</span><span class="sxs-lookup"><span data-stu-id="6b004-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="6b004-110">Do pole Název zadejte popisný název pokladny.</span><span class="sxs-lookup"><span data-stu-id="6b004-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="6b004-111">V poli Číslo obchodu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6b004-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="6b004-112">V poli Profil hardwaru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6b004-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="6b004-113">Profily hardwaru umožňují zadat periferní zařízení, která budou připojena k pokladně, jako je například zásuvka a tiskárna účtenek.</span><span class="sxs-lookup"><span data-stu-id="6b004-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="6b004-114">V poli Vizuální profil zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6b004-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="6b004-115">Vizuální profily se používají k určení obrázků použitých na pozadí pokladny a přihlašovací stránky, jakož i motivů pro pokladny.</span><span class="sxs-lookup"><span data-stu-id="6b004-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="6b004-116">Zadejte hodnotu do pole Číslo registrační pokladny POS EFT.</span><span class="sxs-lookup"><span data-stu-id="6b004-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="6b004-117">Číslo pokladny EFT POS umožňuje informovat procesor plateb o tom, který platební terminál odesílá autorizace požadavků.</span><span class="sxs-lookup"><span data-stu-id="6b004-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="6b004-118">Tato hodnota se nazývá často "ID terminálu" nebo "TID".</span><span class="sxs-lookup"><span data-stu-id="6b004-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="6b004-119">TID lze běžně nalézt na štítku na platebním zařízení.</span><span class="sxs-lookup"><span data-stu-id="6b004-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="6b004-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6b004-120">Click Save.</span></span>

