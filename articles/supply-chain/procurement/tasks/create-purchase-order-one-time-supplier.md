---
title: Vytvoření nákupní objednávky pro jednorázového dodavatele
description: Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424209"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="9dfc5-103">Vytvoření nákupní objednávky pro jednorázového dodavatele</span><span class="sxs-lookup"><span data-stu-id="9dfc5-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9dfc5-104">Tato procedura popisuje způsob vytváření nákupní objednávky pro jednorázového dodavatele.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="9dfc5-105">Dodavatel je automaticky vytvořen s nákupní objednávkou namísto ručního vytvoření účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="9dfc5-106">Nákupní objednávky jsou obvykle vytvořeny agentem pro nákup.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="9dfc5-107">Příklad v této příručce lze použít v rámci ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="9dfc5-108">Je důležité, aby byl jednorázový účet dodavatele nastaven na stránce Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="9dfc5-109">Vytvoření nákupní objednávky pro jednorázového dodavatele</span><span class="sxs-lookup"><span data-stu-id="9dfc5-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="9dfc5-110">Přejděte do nabídky Zásobování a zdroje > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="9dfc5-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-111">Click New.</span></span>
3. <span data-ttu-id="9dfc5-112">Vyberte možnost v poli Jednorázový dodavatel.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="9dfc5-113">Účet dodavatele je automaticky vytvořen a přiřazen do nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="9dfc5-114">Účet dodavatele je založen na šabloně, která je specifikována na kartě Obecné na stránce Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="9dfc5-115">Do pole Název zadejte název dodavatele.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="9dfc5-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-116">Click OK.</span></span>
    * <span data-ttu-id="9dfc5-117">Nákupní objednávku lze nyní dokončit a zpracovat jako jakoukoli jinou objednávku.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="9dfc5-118">Neexistují žádné zvláštní vlastnosti související se způsobem provedení.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="9dfc5-119">Faktura bude zohledňovat splatnost transakcí na účtu dodavatele, který byl vytvořen s objednávkou, a platba bude poté zpracována.</span><span class="sxs-lookup"><span data-stu-id="9dfc5-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

