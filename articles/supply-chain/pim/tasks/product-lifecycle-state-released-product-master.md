---
title: Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu
description: Tento postup ukazuje, jak přiřadit k uvolněnému produktu a jeho variantám stav životního cyklu produktu.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a5d7f6532e3c0b61fcc5758f383257d4a9a09b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226730"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="2df23-103">Přiřazení stavu životního cyklu produktu k uvolněnému hlavnímu produktu</span><span class="sxs-lookup"><span data-stu-id="2df23-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2df23-104">Tento postup ukazuje, jak přiřadit k uvolněnému produktu a jeho variantám stav životního cyklu produktu.</span><span class="sxs-lookup"><span data-stu-id="2df23-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="2df23-105">Předpoklad: Nejprve je nutné přehrát Průvodce záznamem úloh Vytvoření nového stavu cyklu životnosti produktu pro zajištění, že je vytvořen nejméně jeden stav životního cyklu produktu před přehráním tohoto průvodce záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="2df23-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="2df23-106">Najděte uvolněný základní produkt.</span><span class="sxs-lookup"><span data-stu-id="2df23-106">Find a released product master</span></span>
1. <span data-ttu-id="2df23-107">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="2df23-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2df23-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2df23-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="2df23-109">Základní produkt má podtyp produktu Základní produkt.</span><span class="sxs-lookup"><span data-stu-id="2df23-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="2df23-110">Aktualizace stavu životního cyklu</span><span class="sxs-lookup"><span data-stu-id="2df23-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="2df23-111">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="2df23-111">Click Edit.</span></span>
2. <span data-ttu-id="2df23-112">V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2df23-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="2df23-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2df23-113">Click Save.</span></span>
4. <span data-ttu-id="2df23-114">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="2df23-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="2df23-115">Pokud je vybrána možnost Ano, budou mít všechny související varianty uvolněného produktu, které mají stejný původní stav jako vydaný hlavní produkt, také aktualizovány na nový stav životního cyklu produktu.</span><span class="sxs-lookup"><span data-stu-id="2df23-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="2df23-116">Pokud je vybraná možnost Ne, budou mít všechny varianty svůj stávající stav.</span><span class="sxs-lookup"><span data-stu-id="2df23-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="2df23-117">Varianty, které mají jiný stav životního cyklu než vydaný základní produkt, aktualizovány nejsou.</span><span class="sxs-lookup"><span data-stu-id="2df23-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="2df23-118">Ověření stavu životního cyklu variant</span><span class="sxs-lookup"><span data-stu-id="2df23-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="2df23-119">Klikněte na možnost Uvolněné varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="2df23-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="2df23-120">Všimněte si, že všechny varianty zdědily vybraný stav životního cyklu z uvolněného hlavního uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="2df23-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="2df23-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="2df23-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2df23-122">V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="2df23-122">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]