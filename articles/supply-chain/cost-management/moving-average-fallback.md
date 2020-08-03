---
title: Klouzavý průměr, posloupnost záložních nákladů
description: Toto téma obsahuje informace o posloupnosti záložních nákladů pro výpočty klouzavých průměrů v Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597377"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="68f85-103">Klouzavý průměr, posloupnost záložních nákladů</span><span class="sxs-lookup"><span data-stu-id="68f85-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="68f85-104">Jedním ze způsobů, jak lze vypočítat náklady na zásoby, je použití _klouzavého průměru_.</span><span class="sxs-lookup"><span data-stu-id="68f85-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="68f85-105">K jednotlivým skladovým položkám lze přidružit až tři hodnoty nákladů:</span><span class="sxs-lookup"><span data-stu-id="68f85-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="68f85-106">**Poslední výdej** – náklady na poslední výdej, které byly přiřazeny před tím, než se zásoby staly zápornými</span><span class="sxs-lookup"><span data-stu-id="68f85-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="68f85-107">**Aktivní náklady** – nejnovější náklady, které byly aktivovány v nákladové verzi</span><span class="sxs-lookup"><span data-stu-id="68f85-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="68f85-108">**Cena položky** – náklady, které jsou zadány pro uvolněný produkt</span><span class="sxs-lookup"><span data-stu-id="68f85-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="68f85-109">Chcete-li určit, které z těchto nákladových hodnot by se měly použít při výpočtech klouzavých průměrnů, systém použije _posloupnost záložních nákladů_ k určení pořadí priority pro hodnoty.</span><span class="sxs-lookup"><span data-stu-id="68f85-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="68f85-110">Není-li upřednostňovaná hodnota nákladů k dispozici, systém použije další upřednostňovanou hodnotu atd.</span><span class="sxs-lookup"><span data-stu-id="68f85-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="68f85-111">V předchozích verzích Microsoft Dynamics 365 Supply Chain Management používal systém fixní posloupnost záložních nákladů (_Poslední výdej – aktivní náklady – cena položky_).</span><span class="sxs-lookup"><span data-stu-id="68f85-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="68f85-112">Ve verzi 10.0.11 je toto pořadí stále výchozí řadou.</span><span class="sxs-lookup"><span data-stu-id="68f85-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="68f85-113">Můžete však také zapnout funkci, která vám umožní vybírat ze tří posloupností záložních nákladů.</span><span class="sxs-lookup"><span data-stu-id="68f85-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="68f85-114">Tato funkce je užitečná zejména pro organizace, které pravidelně používají záporné hodnoty zásob.</span><span class="sxs-lookup"><span data-stu-id="68f85-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="68f85-115">Chcete-li umožnit výběr pro posloupnost záložních nákladů, musíte vy (nebo správce) použít [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapnout funkci s názvem _Klouzavý průměr, posloupnost záložních nákladů_.</span><span class="sxs-lookup"><span data-stu-id="68f85-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="68f85-116">Chcete-li vybrat posloupnost záložních nákladů pro klouzavý průměr, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="68f85-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="68f85-117">Otevřete stránku **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="68f85-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="68f85-118">Na kartě **Skladové účetnictví** v části **Klouzavý průměr** nastavte hodnotu pole **Posloupnost záložních nákladů** na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="68f85-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="68f85-119">**Poslední výdej – aktivní náklady – cena položky** – toto pořadí je výchozí.</span><span class="sxs-lookup"><span data-stu-id="68f85-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="68f85-120">Jedná se o stejnou řadu, která se použije v případě, že funkce _Klouzavý průměr, posloupnost záložních nákladů_ není zapnuta.</span><span class="sxs-lookup"><span data-stu-id="68f85-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="68f85-121">**Aktivní náklady – poslední výdej**</span><span class="sxs-lookup"><span data-stu-id="68f85-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="68f85-122">**Aktivní náklady – cena položky** – organizace mohou mít problémy s výkonem v případě, že používají obchodní procesy, v nichž sklad pravidelně vychází záporný, a zároveň je objem transakce vysoký.</span><span class="sxs-lookup"><span data-stu-id="68f85-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="68f85-123">Toto nastavení může pomoci při zmírnění těchto potíží s výkonem.</span><span class="sxs-lookup"><span data-stu-id="68f85-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="68f85-124">![Parametry skladového účetnictví](media/inventory-accounting-parameters.png "Parametry skladového účetnictví")</span><span class="sxs-lookup"><span data-stu-id="68f85-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
