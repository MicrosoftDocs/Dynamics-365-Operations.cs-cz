---
title: Třídy menší než nákladní vůz (LTL)
description: Toto téma vysvětluje, co jsou třídy menší než nákladní vůz (LTL), a popisuje, jak je nastavit v Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941803"
---
# <a name="less-than-truckload-ltl-classes"></a><span data-ttu-id="d8d08-103">Třídy menší než nákladní vůz (LTL)</span><span class="sxs-lookup"><span data-stu-id="d8d08-103">Less than truckload (LTL) classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8d08-104">Třída méně než nákladní vůz (LTL) je třída nákladní dopravy, která se používá ke klasifikaci položek, které lze odeslat.</span><span class="sxs-lookup"><span data-stu-id="d8d08-104">A less than truckload (LTL) class is a freight shipping class that is used to classify items that can be shipped.</span></span> <span data-ttu-id="d8d08-105">Obecně platí, že každý typ produktu nebo komodity má kód národní klasifikace nákladní dopravy (NMFC), který odpovídá konkrétnímu číslu třídy nákladní dopravy pro zásilky LTL.</span><span class="sxs-lookup"><span data-stu-id="d8d08-105">Generally, every type of product or commodity has a National Motor Freight Classification (NMFC) code that corresponds to a specific freight class number for LTL shipments.</span></span> <span data-ttu-id="d8d08-106">Nákladní třídy LTL představují kategorie položek, zatímco kódy NMFC se vztahují ke konkrétním komoditám v každé z 18 nákladních tříd.</span><span class="sxs-lookup"><span data-stu-id="d8d08-106">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span>

<span data-ttu-id="d8d08-107">Tato funkce systému umožňuje provádět následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="d8d08-107">This feature lets you use your system to perform the following tasks:</span></span>

- <span data-ttu-id="d8d08-108">Definovat třídy nákladní dopravy LTL, které se ve vaší společnosti používají.</span><span class="sxs-lookup"><span data-stu-id="d8d08-108">Define the LTL freight classes that are used at your company.</span></span>
- <span data-ttu-id="d8d08-109">Přiřadit každou třídu LTL kódu NMFC na stránce **Kódy NMFC**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-109">Assign each LTL class to an NMFC code on the **NMFC Codes** page.</span></span> <span data-ttu-id="d8d08-110">Další informace viz [Kódy Národní klasifikace nákladní dopravy (NMFC)](nmfc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d8d08-110">For more information, see [National Motor Freight Classification (NMFC) codes](nmfc-codes.md).</span></span>
- <span data-ttu-id="d8d08-111">Přiřadit každému produktu kód NMFC (a tedy jeho přidružený kód LTL) na stránce **Produkty**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-111">Assign an NMFC code (and therefore its associated LTL code) to each product on the **Products** page.</span></span>
- <span data-ttu-id="d8d08-112">Přesně vyhodnotit třídu LTL každého produktu, kterému je přiřazen kód NMFC.</span><span class="sxs-lookup"><span data-stu-id="d8d08-112">Accurately assess the LTL class of each product that an NMFC code is assigned to.</span></span>
- <span data-ttu-id="d8d08-113">Určit požadavky na balení pro každou třídu LTL kontrolou mezinárodních standardů LTL.</span><span class="sxs-lookup"><span data-stu-id="d8d08-113">Determine packing requirements for each LTL class by checking the international LTL standards.</span></span> <span data-ttu-id="d8d08-114">Tímto způsobem zajistíte, že vaše výrobky budou dobře chráněny a bezpečně odeslány.</span><span class="sxs-lookup"><span data-stu-id="d8d08-114">In this way, you ensure that your products will be well protected and safely shipped.</span></span>
- <span data-ttu-id="d8d08-115">Získejte přesné odhady dopravy na základě přepravní třídy LTL pro každý produkt.</span><span class="sxs-lookup"><span data-stu-id="d8d08-115">Get accurate shipping estimates, based on the LTL freight class for each product.</span></span>

<span data-ttu-id="d8d08-116">Toto téma popisuje, jak vytvořit třídy LTL v řešení Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d8d08-116">This topic describes how to create LTL classes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="create-an-ltl-class"></a><span data-ttu-id="d8d08-117">Vytvoření třídy LTL</span><span class="sxs-lookup"><span data-stu-id="d8d08-117">Create an LTL class</span></span>

<span data-ttu-id="d8d08-118">Třídu LTL vytvoříte takto.</span><span class="sxs-lookup"><span data-stu-id="d8d08-118">To create an LTL class, follow these steps.</span></span>

1. <span data-ttu-id="d8d08-119">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="d8d08-119">Follow one of these steps:</span></span>

    - <span data-ttu-id="d8d08-120">Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Třídy LTL**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-120">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
    - <span data-ttu-id="d8d08-121">Přejděte do nabídky **Správa přepravy \> Nastavení \> Přepravní normy \> Třídy LTL**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-121">Go to **Transportation management \> Setup \> Transportation standards \> LTL classes**.</span></span>

2. <span data-ttu-id="d8d08-122">V podokně Akce vyberte možnost **Nový** a vytvořte třídu LTL.</span><span class="sxs-lookup"><span data-stu-id="d8d08-122">On the Action Pane, select **New** to create an LTL class.</span></span> <span data-ttu-id="d8d08-123">Poté nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="d8d08-123">Then set the following fields:</span></span>

    - <span data-ttu-id="d8d08-124">**Třída LTL** – Zadejte interní identifikátor (ID) třídy LTL vaší společnosti pro typ komodity.</span><span class="sxs-lookup"><span data-stu-id="d8d08-124">**LTL class** – Enter your company's internal LTL class identifier (ID) for the commodity type.</span></span> <span data-ttu-id="d8d08-125">Většina společností používá mezinárodní standard.</span><span class="sxs-lookup"><span data-stu-id="d8d08-125">Most companies use the international standard.</span></span> <span data-ttu-id="d8d08-126">V takovém případě bude hodnota tohoto pole odpovídat hodnotě parametru pole **Třída**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-126">In that case, the value of this field will match the value of the **Class** field.</span></span> <span data-ttu-id="d8d08-127">Pokud však vaše společnost používá svůj vlastní standard, zadejte kód, který tomuto standardu vyhovuje.</span><span class="sxs-lookup"><span data-stu-id="d8d08-127">However, if your company uses its own standard, enter a code that conforms to that standard.</span></span>
    - <span data-ttu-id="d8d08-128">**Název** – Zadejte popisný název, který vám a dalším uživatelům pomůže vybrat správnou třídu LTL pro každý kód NMFC.</span><span class="sxs-lookup"><span data-stu-id="d8d08-128">**Name** – Enter a descriptive name that will help you and other users select the correct LTL class for each NMFC code.</span></span>
    - <span data-ttu-id="d8d08-129">**Třída** – Zadejte mezinárodní standardní ID třídy LTL pro typ komodity.</span><span class="sxs-lookup"><span data-stu-id="d8d08-129">**Class** – Enter the international standard LTL class ID for the commodity type.</span></span> <span data-ttu-id="d8d08-130">Kód, který zde zadáte, musí odpovídat oficiálnímu standardu.</span><span class="sxs-lookup"><span data-stu-id="d8d08-130">The code that you enter here must conform to the official standard.</span></span>

## <a name="example-set-up-ltl-classes"></a><span data-ttu-id="d8d08-131">Příklad: Nastavení tříd LTL</span><span class="sxs-lookup"><span data-stu-id="d8d08-131">Example: Set up LTL classes</span></span>

<span data-ttu-id="d8d08-132">Následující příklad ukazuje, jak nastavit dva různé třídy LTL, které můžete použít s různými typy produktů.</span><span class="sxs-lookup"><span data-stu-id="d8d08-132">The following example shows how to set up two different LTL classes that you can use with different types of products.</span></span>

1. <span data-ttu-id="d8d08-133">Přejděte na **Řízení skladu \> Nastavení \> Zásoby \> Třídy LTL**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-133">Go to **Warehouse management \> Setup \> Inventory \> LTL classes**.</span></span>
1. <span data-ttu-id="d8d08-134">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-134">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d8d08-135">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d8d08-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d8d08-136">**Třída LTL:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="d8d08-136">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="d8d08-137">**Název:** *Počítače, monitory, chladničky*</span><span class="sxs-lookup"><span data-stu-id="d8d08-137">**Name:** *Computers, monitors, refrigerators*</span></span>
    - <span data-ttu-id="d8d08-138">**Třída:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="d8d08-138">**Class:** *92.5*</span></span>

1. <span data-ttu-id="d8d08-139">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-139">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="d8d08-140">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-140">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d8d08-141">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d8d08-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d8d08-142">**Třída LTL:** *125*</span><span class="sxs-lookup"><span data-stu-id="d8d08-142">**LTL class:** *125*</span></span>
    - <span data-ttu-id="d8d08-143">**Název:** *Malé domácí spotřebiče*</span><span class="sxs-lookup"><span data-stu-id="d8d08-143">**Name:** *Small household appliances*</span></span>
    - <span data-ttu-id="d8d08-144">**Třída:** *125*</span><span class="sxs-lookup"><span data-stu-id="d8d08-144">**Class:** *125*</span></span>

1. <span data-ttu-id="d8d08-145">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d8d08-145">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8d08-146">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d8d08-146">Additional resources</span></span>

- [<span data-ttu-id="d8d08-147">Kódy Motor Freight Classification (NMFC)</span><span class="sxs-lookup"><span data-stu-id="d8d08-147">National Motor Freight Classification (NMFC) codes</span></span>](nmfc-codes.md)
- [<span data-ttu-id="d8d08-148">Vytvoření přepravního dokladu</span><span class="sxs-lookup"><span data-stu-id="d8d08-148">Create a bill of lading</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
