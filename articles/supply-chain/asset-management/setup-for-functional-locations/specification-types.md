---
title: Typy atributů údržby
description: Toto téma vysvětluje, jak vytvořit typy atributů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783118"
---
# <a name="maintenance-attribute-types"></a><span data-ttu-id="8ce81-103">Typy atributů údržby</span><span class="sxs-lookup"><span data-stu-id="8ce81-103">Maintenance attribute types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="8ce81-104">Toto téma vysvětluje, jak vytvořit typy atributů v modulu Správa majetku.</span><span class="sxs-lookup"><span data-stu-id="8ce81-104">This topic explains how to create attribute types in Asset Management.</span></span> <span data-ttu-id="8ce81-105">Atributy slouží k popisu vlastností různých prvků.</span><span class="sxs-lookup"><span data-stu-id="8ce81-105">Attributes are used to describe the properties of various elements.</span></span> <span data-ttu-id="8ce81-106">Můžete nastavit atributy následujících prvků:</span><span class="sxs-lookup"><span data-stu-id="8ce81-106">You can set up attributes on the following elements:</span></span>

- [<span data-ttu-id="8ce81-107">Typy funkčních míst</span><span class="sxs-lookup"><span data-stu-id="8ce81-107">Functional location types</span></span>](../setup-for-functional-locations/functional-location-types.md)
- [<span data-ttu-id="8ce81-108">Funkční místa</span><span class="sxs-lookup"><span data-stu-id="8ce81-108">Functional locations</span></span>](../functional-locations/create-functional-locations.md)
- [<span data-ttu-id="8ce81-109">Typy majetku</span><span class="sxs-lookup"><span data-stu-id="8ce81-109">Asset types</span></span>](../setup-for-objects/object-types.md)
- <span data-ttu-id="8ce81-110">Prostředky</span><span class="sxs-lookup"><span data-stu-id="8ce81-110">Assets</span></span>

<span data-ttu-id="8ce81-111">Atributy, které můžete nastavit, se mohou lišit v závislosti na prvku.</span><span class="sxs-lookup"><span data-stu-id="8ce81-111">The attributes that you can set up vary, depending on the element.</span></span> <span data-ttu-id="8ce81-112">Například pro funkční umístění můžete nastavit atributy pro konfiguraci a fyzickou velikost skladového místa.</span><span class="sxs-lookup"><span data-stu-id="8ce81-112">For example, for a functional location, you can set up attributes for the configuration and physical size of the location.</span></span> <span data-ttu-id="8ce81-113">U typu majetku nebo majetku můžete nastavit atributy pro objem motoru, spotřebu energie a maximální nosnost za různých podmínek.</span><span class="sxs-lookup"><span data-stu-id="8ce81-113">For an asset type or an asset, you can set up attributes for engine volume, power consumption, and maximum load capacity under different conditions.</span></span>

## <a name="create-attribute-types"></a><span data-ttu-id="8ce81-114">Tvorba typů atributů</span><span class="sxs-lookup"><span data-stu-id="8ce81-114">Create attribute types</span></span>

<span data-ttu-id="8ce81-115">Můžete vytvořit vlastní typy atributů.</span><span class="sxs-lookup"><span data-stu-id="8ce81-115">You can create your own attribute types.</span></span> <span data-ttu-id="8ce81-116">Dále je možné převést dimenze produktu ze Microsoft Dynamics 365 for Finance and Operations na stránku **Typů atributů**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-116">Additionally, you can transfer product dimensions from Microsoft Dynamics 365 for Finance and Operations to the **Attribute types** page.</span></span>

1. <span data-ttu-id="8ce81-117">Vyberte **Správa majetku** \> **Nastavení** \> **Typy atributů**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-117">Select **Asset management** \> **Setup** \> **Attribute types**.</span></span>
2. <span data-ttu-id="8ce81-118">Při prvním nastavení typů atributů vyberte možnost **Vytvořit dimenze produktů**, aby se automaticky přesunuly standardní dimenze produktů Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8ce81-118">The first time that you set up attribute types, select **Create product dimensions** to automatically transfer standard Finance and Operations product dimensions.</span></span>
3. <span data-ttu-id="8ce81-119">Zvolte **Nový** pro vytvoření nového typu atributu.</span><span class="sxs-lookup"><span data-stu-id="8ce81-119">Select **New** to create a new attribute type.</span></span>
4. <span data-ttu-id="8ce81-120">Do pole **Typ atributu** zadejte název typu atributu.</span><span class="sxs-lookup"><span data-stu-id="8ce81-120">In the **Attribute type** field, enter a name for the attribute type.</span></span>
5. <span data-ttu-id="8ce81-121">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-121">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="8ce81-122">V poli **Jednotka** vyberte odpovídající jednotku atributu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="8ce81-122">In the **Unit** field, select the relevant attribute unit, as required.</span></span>
7. <span data-ttu-id="8ce81-123">V poli **Formát datu** vyberte typ dat pro jednotku.</span><span class="sxs-lookup"><span data-stu-id="8ce81-123">In the **Data type** field, select a data type for the unit.</span></span>
8. <span data-ttu-id="8ce81-124">Pokud jste jako typ dat vybrali **Řetězec**, vytvořte pomocí následujících kroků hodnoty pro typ atributu:</span><span class="sxs-lookup"><span data-stu-id="8ce81-124">If you selected **String** as the data type, follow these steps to create values for the attribute type:</span></span>

    1. <span data-ttu-id="8ce81-125">Vyberte typ atributu a pak vyberte **Hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-125">Select the attribute type, and then select **Values**.</span></span>
    2. <span data-ttu-id="8ce81-126">V poli **Hodnoty atributu** vyberte možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-126">In the **Attribute values** field, select **New**.</span></span>
    3. <span data-ttu-id="8ce81-127">V poli **Typ atributu** vyberte požadovaný typ atributu (dimenze).</span><span class="sxs-lookup"><span data-stu-id="8ce81-127">In the **Attribute type** field, select an attribute type (dimension).</span></span>
    4. <span data-ttu-id="8ce81-128">V poli **Hodnota** zadejte související hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8ce81-128">In the **Value** field, enter a related value.</span></span>
    5. <span data-ttu-id="8ce81-129">Zadejte popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-129">In the **Description** field, enter a description.</span></span>
    6. <span data-ttu-id="8ce81-130">Uložte záznam.</span><span class="sxs-lookup"><span data-stu-id="8ce81-130">Save the record.</span></span>
    7. <span data-ttu-id="8ce81-131">Vraťte se na stránku **Typy atributů**.</span><span class="sxs-lookup"><span data-stu-id="8ce81-131">Return to the **Attribute types** page.</span></span>

9. <span data-ttu-id="8ce81-132">Uložte záznam.</span><span class="sxs-lookup"><span data-stu-id="8ce81-132">Save the record.</span></span>

    <span data-ttu-id="8ce81-133">Pole **Typy funkčních míst** zobrazuje počet funkčních míst, která používají typ atributu.</span><span class="sxs-lookup"><span data-stu-id="8ce81-133">The **Functional location types** field shows the number of functional locations that are using the attribute type.</span></span> <span data-ttu-id="8ce81-134">Pole **Typy majetku** zobrazuje počet typů majetku, které jej používají.</span><span class="sxs-lookup"><span data-stu-id="8ce81-134">The **Asset types** field shows the number of asset types that are using it.</span></span>
