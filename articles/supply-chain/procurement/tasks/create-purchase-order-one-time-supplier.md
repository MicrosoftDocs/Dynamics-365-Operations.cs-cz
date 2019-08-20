---
title: Vytvoření nákupní objednávky pro jednorázového dodavatele
description: Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26c62aa72a7919c780bb709b185b48c97066c538
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836305"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a6a6a-103">Vytvoření nákupní objednávky pro jednorázového dodavatele</span><span class="sxs-lookup"><span data-stu-id="a6a6a-103">Create a purchase order for a one-time supplier</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6a6a-104">Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="a6a6a-105">Dodavatel je automaticky vytvořen s nákupní objednávkou namísto ručního vytvoření účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="a6a6a-106">Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="a6a6a-107">Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="a6a6a-108">Je důležité, aby byl jednorázový účet dodavatele nastaven na stránce Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="a6a6a-109">Vytvoření nákupní objednávky pro jednorázového dodavatele</span><span class="sxs-lookup"><span data-stu-id="a6a6a-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="a6a6a-110">Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="a6a6a-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-111">Click New.</span></span>
3. <span data-ttu-id="a6a6a-112">Vyberte možnost v poli Jednorázový dodavatel.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="a6a6a-113">Účet dodavatele je automaticky vytvořen a přiřazen do nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="a6a6a-114">Účet dodavatele je založen na šabloně, která je specifikována na kartě Obecné na stránce Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="a6a6a-115">Do pole Název zadejte název dodavatele.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="a6a6a-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-116">Click OK.</span></span>
    * <span data-ttu-id="a6a6a-117">Nákupní objednávku lze nyní dokončit a zpracovat jako jakoukoli jinou objednávku.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="a6a6a-118">Neexistují žádné zvláštní vlastnosti související se způsobem provedení.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="a6a6a-119">Faktura bude zohledňovat splatnost transakcí na účtu dodavatele, který byl vytvořen s objednávkou, a platba bude poté zpracována.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span> <span data-ttu-id="a6a6a-120">Nakonec bude účet dodavatele odstraněn.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-120">When this is completed, the vendor account can be deleted.</span></span> <span data-ttu-id="a6a6a-121">To se provádí obvykle v oddělení závazků.</span><span class="sxs-lookup"><span data-stu-id="a6a6a-121">This is typically done by the accounts payable department.</span></span>  

