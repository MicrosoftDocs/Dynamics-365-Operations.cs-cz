---
title: Náklady kvality pro operace neshod
description: Toto téma popisuje, jak vytvořit náklady kvality, které lze použít s operacemi pro neshodu.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestMiscCharges
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfa424e94048aa9eb1ce4da9aa69e8d4df71cefb
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956577"
---
# <a name="charges-for-nonconformance-operations"></a><span data-ttu-id="cf8a5-103">Náklady kvality pro operace neshod</span><span class="sxs-lookup"><span data-stu-id="cf8a5-103">Charges for nonconformance operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf8a5-104">Toto téma popisuje, jak vytvořit náklady kvality, které lze použít s operacemi pro neshodu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-104">This topic describes how to create quality charges that can be used with operations for a nonconformance.</span></span>

<span data-ttu-id="cf8a5-105">Na stránce **Náklady kvality** definujte typy nákladů, které můžete přidat k operacím neshod.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-105">You use the **Quality charges** page to define the types of charges that can be added to operations for a nonconformance.</span></span> <span data-ttu-id="cf8a5-106">Poplatky vám umožňují sledovat podrobnosti poplatků, které dlužíte zákazníkovi za neshodné výrobky, nebo které vám prodejce dluží za neshodné výrobky, které jste obdrželi.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-106">Charges let you track details about fees or charges that you owe to a customer for nonconforming products, or that a vendor owes to you for nonconforming products that you received.</span></span> <span data-ttu-id="cf8a5-107">Můžete také použít poplatky ke sledování nákladů, které jsou požadovány pro externí dodavatele nebo služby k provedení operace.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-107">You might also use charges to track costs that are required for external vendors or services to perform an operation.</span></span>

## <a name="examples-of-quality-charges"></a><span data-ttu-id="cf8a5-108">Příklady nákladů kvality</span><span class="sxs-lookup"><span data-stu-id="cf8a5-108">Examples of quality charges</span></span>

<span data-ttu-id="cf8a5-109">Pracujete pro výrobní společnost.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-109">You work for a manufacturing company.</span></span> <span data-ttu-id="cf8a5-110">Vaše společnost má smlouvy s několika dodavateli.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-110">Your company has contracts with several vendors.</span></span> <span data-ttu-id="cf8a5-111">Tyto smlouvy uvádějí standardy pro včasné odeslání, poškození a kvalitu produktu pro zboží.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-111">Those contracts outline standards for on-time shipment, damages, and product quality for items.</span></span> <span data-ttu-id="cf8a5-112">Podobně má několik vašich zákazníků s vaší společností dohody o vrácení, poškození a kvalitě produktu.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-112">Likewise, several of your customers have agreements with your company about returns, damages, and product quality.</span></span>

<span data-ttu-id="cf8a5-113">Struktura poplatků je definována pro každou okolnost a specifikována ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-113">A fee structure is defined for each circumstance and specified in the contract.</span></span> <span data-ttu-id="cf8a5-114">Můžete nakonfigurovat náklady kvality tak, aby obsahovaly různé typy poplatků, například *Poškození*, *Pozdní dodávka* a *Kvalita*.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-114">You can configure quality charges to outline the various types of charges, such as *Damages*, *Late shipment*, and *Quality*.</span></span> <span data-ttu-id="cf8a5-115">Poté, když vytvoříte neshodu, přidáte jednu nebo více operací.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-115">Then, when you create a nonconformance, you add one or more operations.</span></span> <span data-ttu-id="cf8a5-116">Pro každou operaci vyberete **Náklady** k definování podrobnosti o poplatcích.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-116">For each operation, you select **Charges** to define the details about the fees.</span></span>

## <a name="create-a-quality-charge"></a><span data-ttu-id="cf8a5-117">Vytvoření nákladu kvality</span><span class="sxs-lookup"><span data-stu-id="cf8a5-117">Create a quality charge</span></span>

1. <span data-ttu-id="cf8a5-118">Přejděte na **Řízení zásob \> Nastavení \> Správa kvality \> Náklady kvality**.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-118">Go to **Inventory management \> Setup \> Quality management \> Quality charges**.</span></span>
1. <span data-ttu-id="cf8a5-119">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-119">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="cf8a5-120">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="cf8a5-120">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="cf8a5-121">**Kód nákladu** - Zadejte jedinečné ID nebo název nákladu kvality.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-121">**Charges code** – Enter a unique ID or name for the quality charge.</span></span>
    - <span data-ttu-id="cf8a5-122">**Popis** - Zadejte podrobný popis typu nákladu kvality.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-122">**Description** – Enter a detailed description of the quality charge.</span></span>

1. <span data-ttu-id="cf8a5-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-123">Close the page.</span></span>

## <a name="add-a-quality-charge-to-an-operation-for-a-nonconformance"></a><span data-ttu-id="cf8a5-124">Přidejte do operace náklad kvality kvůli neshodě</span><span class="sxs-lookup"><span data-stu-id="cf8a5-124">Add a quality charge to an operation for a nonconformance</span></span>

<span data-ttu-id="cf8a5-125">Podrobnosti o tom, jak přidat operace k neshodě a účtovat jim náklady, viz [Operace pro neshody](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="cf8a5-125">For details about how to add operations to a nonconformance and apply charges to them, see [Operations for nonconformances](quality-operations.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf8a5-126">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="cf8a5-126">Additional resources</span></span>

- [<span data-ttu-id="cf8a5-127">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="cf8a5-127">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="cf8a5-128">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="cf8a5-128">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="cf8a5-129">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="cf8a5-129">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="cf8a5-130">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="cf8a5-130">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="cf8a5-131">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="cf8a5-131">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="cf8a5-132">Kódy kvality pro náklady.</span><span class="sxs-lookup"><span data-stu-id="cf8a5-132">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="cf8a5-133">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="cf8a5-133">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="cf8a5-134">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="cf8a5-134">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
