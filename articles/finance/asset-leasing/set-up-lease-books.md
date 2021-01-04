---
title: Nastavení leasingových knih
description: Toto téma popisuje informace udržované v leasingových knihách. Leasingové knihy obsahují účetní zásady, které určují, jak je v systému účtován leasing.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441355"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="4aebc-104">Nastavení leasingových knih</span><span class="sxs-lookup"><span data-stu-id="4aebc-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aebc-105">Leasingové knihy obsahují účetní zásady, které určují, jak je v systému účtován leasing.</span><span class="sxs-lookup"><span data-stu-id="4aebc-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="4aebc-106">Kromě hotovostního účetnictví podporuje majetkový leasing následující standardy:</span><span class="sxs-lookup"><span data-stu-id="4aebc-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="4aebc-107">Obecně uznávané účetní zásady ve Spojených státech (US GAAP)</span><span class="sxs-lookup"><span data-stu-id="4aebc-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="4aebc-108">Téma kodifikace účetních standardů 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="4aebc-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="4aebc-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="4aebc-109">ASC 840</span></span>
- <span data-ttu-id="4aebc-110">Mezinárodní standard účetního výkaznictví 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="4aebc-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="4aebc-111">Mezinárodní účetní standard 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="4aebc-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="4aebc-112">Při vytváření leasingové knihy postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="4aebc-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="4aebc-113">Přejděte na **Leasing majetku \> Nastavení \> Leasingové knihy**.</span><span class="sxs-lookup"><span data-stu-id="4aebc-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="4aebc-114">Vyberte **Nový** pro přidání knihy.</span><span class="sxs-lookup"><span data-stu-id="4aebc-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="4aebc-115">Nastavte následující pole.</span><span class="sxs-lookup"><span data-stu-id="4aebc-115">Set the following fields.</span></span>

    | <span data-ttu-id="4aebc-116">Jméno</span><span class="sxs-lookup"><span data-stu-id="4aebc-116">Name</span></span>                                     | <span data-ttu-id="4aebc-117">popis</span><span class="sxs-lookup"><span data-stu-id="4aebc-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="4aebc-118">Účtovací vrstva</span><span class="sxs-lookup"><span data-stu-id="4aebc-118">Posting layer</span></span>                            | <span data-ttu-id="4aebc-119">Vyberte účtovací vrstvu, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="4aebc-119">Select the posting layer to use.</span></span> <span data-ttu-id="4aebc-120">Každá kniha, která je připojena k leasingu, je nastavena pro konkrétní účtovací vrstvu.</span><span class="sxs-lookup"><span data-stu-id="4aebc-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="4aebc-121">Každá účtovací vrstva má jiné účely zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="4aebc-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="4aebc-122">Typ leasingu</span><span class="sxs-lookup"><span data-stu-id="4aebc-122">Lease type</span></span>                               | <span data-ttu-id="4aebc-123">Vyberte, zda má být leasing klasifikován automaticky nebo zda má být předdefinován jako finanční nebo operativní leasing.</span><span class="sxs-lookup"><span data-stu-id="4aebc-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="4aebc-124">Rámec účetnictví</span><span class="sxs-lookup"><span data-stu-id="4aebc-124">Accounting framework</span></span>                     | <span data-ttu-id="4aebc-125">Vyberte rámec, který je spojen s knihou.</span><span class="sxs-lookup"><span data-stu-id="4aebc-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="4aebc-126">Nastavení doby trvání leasingu / očekávané doby použitelnosti</span><span class="sxs-lookup"><span data-stu-id="4aebc-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="4aebc-127">Systém klasifikuje leasing jako finanční, pokud je typ leasingu nastaven na **automatický** a je-li doba trvání leasingu na očekávanou dobu použitelnosti majetku větší než nebo rovna procentu zadanému v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="4aebc-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="4aebc-128">Nastavení současné hodnoty / reálné hodnoty majetku</span><span class="sxs-lookup"><span data-stu-id="4aebc-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="4aebc-129">Zadejte celé číslo a definujte prahovou hodnotu, která určí typ leasingu.</span><span class="sxs-lookup"><span data-stu-id="4aebc-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="4aebc-130">Pokud je současná hodnota budoucích minimálních leasingových plateb větší než uživatelem definovaná hodnota z nastavení knihy a pokud je klasifikace knihy leasingu nastavena na automatickou, systém klasifikuje leasing jako finanční leasing.</span><span class="sxs-lookup"><span data-stu-id="4aebc-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="4aebc-131">Krátkodobá prahová hodnota</span><span class="sxs-lookup"><span data-stu-id="4aebc-131">Short-term threshold</span></span>                     | <span data-ttu-id="4aebc-132">Zadejte počet měsíců, které se mají použít jako prahová hodnota pro krátkodobé leasingy.</span><span class="sxs-lookup"><span data-stu-id="4aebc-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="4aebc-133">Pokud je doba leasingu menší nebo rovna počtu měsíců, které zde zadáte, systém klasifikuje leasing jako krátkodobý a použije se odložená splátka.</span><span class="sxs-lookup"><span data-stu-id="4aebc-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="4aebc-134">Prahová hodnota nízké hodnoty</span><span class="sxs-lookup"><span data-stu-id="4aebc-134">Low value threshold</span></span>                      | <span data-ttu-id="4aebc-135">Zadejte částku, která se použije jako prahová hodnota pro leasingy aktiv s nízkou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="4aebc-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="4aebc-136">Pokud je reální hodnota majetku menší nebo rovna hodnotě, kterou zde zadáte, systém klasifikuje leasing jako leasing aktiv s nízkou hodnotou a použije se odložená splátka.</span><span class="sxs-lookup"><span data-stu-id="4aebc-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="4aebc-137">Platba dodavateli</span><span class="sxs-lookup"><span data-stu-id="4aebc-137">Pay to vendor</span></span>                            | <span data-ttu-id="4aebc-138">Tuto možnost nastavte na **Ano**, pokud chcete umožnit účtování leasingových plateb jako fakturu na účet dodavatele, který je uveden u každého leasingu.</span><span class="sxs-lookup"><span data-stu-id="4aebc-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="4aebc-139">Po zaúčtování leasingové splátky bude připsána částka na účet dodavatele.</span><span class="sxs-lookup"><span data-stu-id="4aebc-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="4aebc-140">Pokud je tato možnost nastavena na **Ne**, bude místo toho hodnota připsána na účet, který je určen pro typ zaúčtování **Leasingová platba** na stránce **Parametry zaúčtování leasingu**.</span><span class="sxs-lookup"><span data-stu-id="4aebc-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
