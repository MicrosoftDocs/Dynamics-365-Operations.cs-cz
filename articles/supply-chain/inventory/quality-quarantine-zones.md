---
title: Karanténní zóny pro neshody
description: Toto téma popisuje, jak vytvářet a používat karanténní zóny pro neshody.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f4b9dfc7882af4570bf1908784b8d114396402
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021797"
---
# <a name="quarantine-zones-for-nonconformances"></a><span data-ttu-id="79d2a-103">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="79d2a-103">Quarantine zones for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79d2a-104">Toto téma popisuje, jak vytvářet a používat karanténní zóny pro neshody.</span><span class="sxs-lookup"><span data-stu-id="79d2a-104">This topic describes how to create and use quarantine zones for nonconformances.</span></span>

<span data-ttu-id="79d2a-105">K definici zón, které lze neshodám přiřadit, použijte stránku **Karanténní zóny**.</span><span class="sxs-lookup"><span data-stu-id="79d2a-105">You use the **Quarantine zones** page to define zones that can be assigned to nonconformances.</span></span> <span data-ttu-id="79d2a-106">Když vytvoříte neshodu, můžete nastavit pole **Karanténní zóna** a **Typ karantény** na kartě **Obecné** stránky **Neshody**.</span><span class="sxs-lookup"><span data-stu-id="79d2a-106">When you create a nonconformance, you can set the **Quarantine zone** and **Quarantine type** fields on the **General** tab of the **Non conformances** page.</span></span> <span data-ttu-id="79d2a-107">Pole **Karanténní zóna** obvykle označuje oblast nebo umístění, kde se položka nachází.</span><span class="sxs-lookup"><span data-stu-id="79d2a-107">The **Quarantine zone** field typically indicates the area or location where the item is located.</span></span> <span data-ttu-id="79d2a-108">Pole **Typ karantény** definuje položku buď jako *Omezené použití*, nebo *Nepoužitelné*.</span><span class="sxs-lookup"><span data-stu-id="79d2a-108">The **Quarantine type** field defines the item as either *Restricted usage* or *Unusable*.</span></span>

<span data-ttu-id="79d2a-109">Když vytisknete sestavu o neshodě nebo opravách pro neshodu, můžete zobrazit karanténní zónu, kde je položka umístěna.</span><span class="sxs-lookup"><span data-stu-id="79d2a-109">When you print a nonconformance or corrections report for a nonconformance, you can view the quarantine zone where the item is located.</span></span>

<span data-ttu-id="79d2a-110">Můžete také vytisknout značku neshody pro neshodu.</span><span class="sxs-lookup"><span data-stu-id="79d2a-110">You can also print a nonconformance tag for a nonconformance.</span></span> <span data-ttu-id="79d2a-111">V této sestavě se zobrazí přiřazená karanténní zóna a informace o použití, které poskytují návod, jak manipulovat s vadným materiálem.</span><span class="sxs-lookup"><span data-stu-id="79d2a-111">This report shows the assigned quarantine zone and information about usage to provide guidance about how defective material should be handled.</span></span> <span data-ttu-id="79d2a-112">Karanténní zóny mohou odpovídat umístěním zásob nebo provozním prostředkům.</span><span class="sxs-lookup"><span data-stu-id="79d2a-112">The quarantine zones might correspond to inventory locations or operations resources.</span></span>

## <a name="examples-of-quarantine-zones"></a><span data-ttu-id="79d2a-113">Příklady karanténních zón</span><span class="sxs-lookup"><span data-stu-id="79d2a-113">Examples of quarantine zones</span></span>

### <a name="example-1"></a><span data-ttu-id="79d2a-114">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="79d2a-114">Example 1</span></span>

<span data-ttu-id="79d2a-115">Pracujete ve společnosti vyrábějící elektroniku, která vyrábí a distribuuje televizory, reproduktory a přehrávače médií.</span><span class="sxs-lookup"><span data-stu-id="79d2a-115">You work at an electronics manufacturing company that produces and distributes televisions, speakers, and media players.</span></span> <span data-ttu-id="79d2a-116">V tomto případě můžete nakonfigurovat karanténní zónu tak, aby představovala každý typ produktu.</span><span class="sxs-lookup"><span data-stu-id="79d2a-116">In this case, you can configure a quarantine zone to represent each type of product.</span></span>

### <a name="example-2"></a><span data-ttu-id="79d2a-117">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="79d2a-117">Example 2</span></span>

<span data-ttu-id="79d2a-118">Tři přihrádky a dva stojany se používají k ukládání položek s neshodou.</span><span class="sxs-lookup"><span data-stu-id="79d2a-118">Three bins and two racks are used to store items that are nonconforming.</span></span> <span data-ttu-id="79d2a-119">V tomto případě můžete nakonfigurovat pět karanténních zón, jednu pro každou přihrádku a každý stojan.</span><span class="sxs-lookup"><span data-stu-id="79d2a-119">In this case, you can configure five quarantine zones, one for each bin and each rack.</span></span>

## <a name="create-a-quarantine-zone"></a><span data-ttu-id="79d2a-120">Vytvoření karanténní zóny</span><span class="sxs-lookup"><span data-stu-id="79d2a-120">Create a quarantine zone</span></span>

1. <span data-ttu-id="79d2a-121">Přejděte k nabídce **Řízení zásob \> Nastavení \> Správa kvality \> Karanténní zóny**.</span><span class="sxs-lookup"><span data-stu-id="79d2a-121">Go to **Inventory management \> Setup \> Quality management \> Quarantine zones**.</span></span>
1. <span data-ttu-id="79d2a-122">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="79d2a-122">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="79d2a-123">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="79d2a-123">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="79d2a-124">**Karanténní zóna** – zadejte jedinečné ID nebo název karanténní zóny.</span><span class="sxs-lookup"><span data-stu-id="79d2a-124">**Quarantine zone** – Enter a unique ID or name for the quarantine zone.</span></span>
    - <span data-ttu-id="79d2a-125">**Popis** – zadejte podrobný popis karanténní zóny.</span><span class="sxs-lookup"><span data-stu-id="79d2a-125">**Description** – Enter a detailed description of the quarantine zone.</span></span>

1. <span data-ttu-id="79d2a-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="79d2a-126">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79d2a-127">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="79d2a-127">Additional resources</span></span>

- [<span data-ttu-id="79d2a-128">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="79d2a-128">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="79d2a-129">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="79d2a-129">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="79d2a-130">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="79d2a-130">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="79d2a-131">Typy problémů pro neshody</span><span class="sxs-lookup"><span data-stu-id="79d2a-131">Problem types for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="79d2a-132">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="79d2a-132">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="79d2a-133">Kódy kvality pro náklady.</span><span class="sxs-lookup"><span data-stu-id="79d2a-133">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="79d2a-134">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="79d2a-134">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="79d2a-135">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="79d2a-135">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
