---
title: Atributy dávky
description: Toto téma popisuje informace o atributech dávky. Atributy dávky umožňují charakterizovat suroviny a hotové výrobky, které vytvářejí skladové dávky. Toto téma rovněž vysvětluje postup přiřazení atributů dávky a způsob, jakým je můžete vyhledat při rezervaci dávek.
author: ShylaThompson
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 744c8d65d8f1b28dc8197f3f8dd1803f916958b5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246470"
---
# <a name="batch-attributes"></a><span data-ttu-id="eabc1-105">Atributy dávky</span><span class="sxs-lookup"><span data-stu-id="eabc1-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eabc1-106">Toto téma popisuje informace o atributech dávky.</span><span class="sxs-lookup"><span data-stu-id="eabc1-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="eabc1-107">Atributy dávky umožňují charakterizovat suroviny a hotové výrobky, které vytvářejí skladové dávky.</span><span class="sxs-lookup"><span data-stu-id="eabc1-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="eabc1-108">Toto téma rovněž vysvětluje postup přiřazení atributů dávky a způsob, jakým je můžete vyhledat při rezervaci dávek.</span><span class="sxs-lookup"><span data-stu-id="eabc1-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="eabc1-109">Atributy dávky umožňují charakterizovat suroviny a hotové výrobky, které vytvářejí skladové dávky.</span><span class="sxs-lookup"><span data-stu-id="eabc1-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="eabc1-110">Atributy dávky se mohou lišit v závislosti na celé řadě faktorů (například na podmínkách prostředí, na kvalitě surovin použitých při výrobě dávky nebo na výsledku dokončených produktů).</span><span class="sxs-lookup"><span data-stu-id="eabc1-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="eabc1-111">Počet a typy použitých atributů dávky se mohou výrazně lišit také mezi různými odvětvími.</span><span class="sxs-lookup"><span data-stu-id="eabc1-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="eabc1-112">Zde jsou dva příklady použití atributů dávky:</span><span class="sxs-lookup"><span data-stu-id="eabc1-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="eabc1-113">V mlékárenském průmyslu může mít mléko jako surovina pro výrobu sýra například atributy udávající obsah tuku a hmotnostní procento.</span><span class="sxs-lookup"><span data-stu-id="eabc1-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="eabc1-114">Sýr vyrobený z mléka může mít další atributy, například podíl sušiny a stáří.</span><span class="sxs-lookup"><span data-stu-id="eabc1-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="eabc1-115">V ocelářském průmyslu může mít vyráběná ocel například atributy udávající procentuální obsah hořčíku, stříbra a zinku.</span><span class="sxs-lookup"><span data-stu-id="eabc1-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="eabc1-116">Pro zjednodušení správy počtu a typů atributů můžete použít skupiny atributů dávky.</span><span class="sxs-lookup"><span data-stu-id="eabc1-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="eabc1-117">Tímto způsobem nemusíte přidávat jednotlivé atributy zvlášť.</span><span class="sxs-lookup"><span data-stu-id="eabc1-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="eabc1-118">Přiřazení atributů dávky</span><span class="sxs-lookup"><span data-stu-id="eabc1-118">Assign batch attributes</span></span>
<span data-ttu-id="eabc1-119">Atributy dávky se přiřazují k jednotlivým produktům, které jsou zahrnuty do skladových dávek nebo jsou přiřazeny k produktům, které jsou asociovány s konkrétními odběrateli.</span><span class="sxs-lookup"><span data-stu-id="eabc1-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="eabc1-120">Před přiřazením atributu dávky na úrovni odběratelů je nutné přiřadit je na úrovni produktu.</span><span class="sxs-lookup"><span data-stu-id="eabc1-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="eabc1-121">Výrobek musí mít dimenze dávky nastavené na **Aktivní** ve skupině sledování dimenze.</span><span class="sxs-lookup"><span data-stu-id="eabc1-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="eabc1-122">Pokud chcete přiřadit atribut dávky k jednotlivým produktům, použijte stránku specifickou pro produkt.</span><span class="sxs-lookup"><span data-stu-id="eabc1-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="eabc1-123">Je-li atribut specifický pro produkt odběratele, použijte stránku specifickou pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="eabc1-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="eabc1-124">Po přidání atributu k produktu se také definují další parametry.</span><span class="sxs-lookup"><span data-stu-id="eabc1-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="eabc1-125">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="eabc1-125">Here are some examples:</span></span>

-   <span data-ttu-id="eabc1-126">Minimální a maximální rozsah pro atribut typu **Celé číslo** nebo **Zlomek**.</span><span class="sxs-lookup"><span data-stu-id="eabc1-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="eabc1-127">Akce tolerance pro atribut typu **Celé číslo** nebo **Zlomek**.</span><span class="sxs-lookup"><span data-stu-id="eabc1-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="eabc1-128">Pokud hodnota atributu spadá mimo rozsah minima a maxima, akce může být upozornění nebo chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="eabc1-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="eabc1-129">Cílová hodnota základního atributu.</span><span class="sxs-lookup"><span data-stu-id="eabc1-129">The target value for the attribute.</span></span> <span data-ttu-id="eabc1-130">Tato hodnota je optimální hodnota atributu a platí pro všechny typy atributů.</span><span class="sxs-lookup"><span data-stu-id="eabc1-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="eabc1-131">Lze otevřít stránky pro produkty, které vyberete na stránce **Uvolněné produkty** v modulu Řízení informací o produktu.</span><span class="sxs-lookup"><span data-stu-id="eabc1-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="eabc1-132">Po přiřazení atributů dávky k produktu můžete přiřadit specifické hodnoty k atributům na stránce **Atributy skladové dávky**.</span><span class="sxs-lookup"><span data-stu-id="eabc1-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="eabc1-133">Rezervace dávek</span><span class="sxs-lookup"><span data-stu-id="eabc1-133">Reserve batches</span></span>
<span data-ttu-id="eabc1-134">Atribut dávky můžete vyhledat, pokud rezervujete dávku pro prodejní objednávku s cílem naplnit objednávku odběratele, nebo vydáváte dávky pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="eabc1-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="eabc1-135">Hledání pomáhá vyhledat skladovou dávku, která obsahuje produkt, který má požadovaný atribut dávky.</span><span class="sxs-lookup"><span data-stu-id="eabc1-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="eabc1-136">Po nalezení jedné nebo více dávek je možné rezervovat produkt pro původní řádek skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="eabc1-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]