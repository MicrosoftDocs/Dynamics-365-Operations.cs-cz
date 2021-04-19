---
title: Vytvoření nákupní objednávky pro jednorázového dodavatele
description: Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe76a3d481c3bc8dd3a3d45eda031df61ece4aa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812364"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="f2793-103">Vytvoření nákupní objednávky pro jednorázového dodavatele</span><span class="sxs-lookup"><span data-stu-id="f2793-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2793-104">Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f2793-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="f2793-105">Dodavatel je automaticky vytvořen s nákupní objednávkou namísto ručního vytvoření účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f2793-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="f2793-106">Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup.</span><span class="sxs-lookup"><span data-stu-id="f2793-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="f2793-107">Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f2793-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="f2793-108">Je důležité, aby byl jednorázový účet dodavatele nastaven na stránce Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="f2793-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="f2793-109">Vytvoření nákupní objednávky pro jednorázového dodavatele</span><span class="sxs-lookup"><span data-stu-id="f2793-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="f2793-110">Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f2793-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f2793-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f2793-111">Click New.</span></span>
3. <span data-ttu-id="f2793-112">Vyberte možnost v poli Jednorázový dodavatel.</span><span class="sxs-lookup"><span data-stu-id="f2793-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="f2793-113">Účet dodavatele je automaticky vytvořen a přiřazen do nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f2793-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="f2793-114">Účet dodavatele je založen na šabloně, která je specifikována na kartě Obecné na stránce Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="f2793-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="f2793-115">Do pole Název zadejte název dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f2793-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="f2793-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f2793-116">Click OK.</span></span>
    * <span data-ttu-id="f2793-117">Nákupní objednávku lze nyní dokončit a zpracovat jako jakoukoli jinou objednávku.</span><span class="sxs-lookup"><span data-stu-id="f2793-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="f2793-118">Neexistují žádné zvláštní vlastnosti související se způsobem provedení.</span><span class="sxs-lookup"><span data-stu-id="f2793-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="f2793-119">Faktura bude zohledňovat splatnost transakcí na účtu dodavatele, který byl vytvořen s objednávkou, a platba bude poté zpracována.</span><span class="sxs-lookup"><span data-stu-id="f2793-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]