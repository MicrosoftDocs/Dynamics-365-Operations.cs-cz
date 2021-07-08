---
title: Produkt je blokován pro transakce
description: Po potvrzení plánování objednávek se zobrazí chybová zpráva s oznámením, že položka je pro transakce blokována.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301272"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="e25e3-103">Produkt je blokován pro transakce</span><span class="sxs-lookup"><span data-stu-id="e25e3-103">Product is on hold for transactions</span></span>

<span data-ttu-id="e25e3-104">Kód chyby: SYS13295</span><span class="sxs-lookup"><span data-stu-id="e25e3-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="e25e3-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="e25e3-105">Symptoms</span></span>

<span data-ttu-id="e25e3-106">Poté, co potvrdíte plánované objednávky, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="e25e3-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="e25e3-107">Položka %1 je blokována pro transakce v %2.</span><span class="sxs-lookup"><span data-stu-id="e25e3-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="e25e3-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="e25e3-108">Cause</span></span>

<span data-ttu-id="e25e3-109">Při popisu blokovaných položek systém používá termíny *blokováno*, *zastaveno* a *blokováno* zaměnitelně.</span><span class="sxs-lookup"><span data-stu-id="e25e3-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="e25e3-110">Tato chyba znamená, že položka je nastavena jako **Zastaveno** ve výchozím nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="e25e3-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="e25e3-111">Pokud je položka blokována a přidáte ji do nákupní objednávky nebo řádku prodejní objednávky, zobrazí se varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="e25e3-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="e25e3-112">Při blokování položky není možné upravit skladové transakce související se řádkem prodejní či nákupní objednávky (například při účtování dodacího listu nebo faktury).</span><span class="sxs-lookup"><span data-stu-id="e25e3-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="e25e3-113">Nakoupenou položku můžete blokovat a zároveň ji prodat.</span><span class="sxs-lookup"><span data-stu-id="e25e3-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="e25e3-114">V takovém případě je vybráno zaškrtávací políčko **Zastaveno** na nákupní objednávce, ale položka není blokována u zásob nebo v prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="e25e3-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="e25e3-115">Tady jsou některé z podmínek, které mohou způsobit zablokování prodeje čísla položky:</span><span class="sxs-lookup"><span data-stu-id="e25e3-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="e25e3-116">Položka je stále ve vývoji nebo výrobě.</span><span class="sxs-lookup"><span data-stu-id="e25e3-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="e25e3-117">Proto nechcete, aby byl prodán nebo rezervován.</span><span class="sxs-lookup"><span data-stu-id="e25e3-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="e25e3-118">Obdrželi jste mnoho vadných položek a vady je třeba opravit, než bude možné předmět prodat.</span><span class="sxs-lookup"><span data-stu-id="e25e3-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="e25e3-119">V takových případech je možné blokovat položku, až dokud není problém vyřešen.</span><span class="sxs-lookup"><span data-stu-id="e25e3-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="e25e3-120">Při blokování položky a vytvoření řádku vratky se zobrazí zpráva.</span><span class="sxs-lookup"><span data-stu-id="e25e3-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="e25e3-121">Nelze blokovat řadu ani šarži položky.</span><span class="sxs-lookup"><span data-stu-id="e25e3-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="e25e3-122">Pokud mají být blokovány části položky, lze to provést přesunutím zásob nebo zablokováním celé zásoby položky na určené období.</span><span class="sxs-lookup"><span data-stu-id="e25e3-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="e25e3-123">Řešení</span><span class="sxs-lookup"><span data-stu-id="e25e3-123">Resolution</span></span>

- <span data-ttu-id="e25e3-124">Otevřete stránku **Výchozí nastavení objednávky** pro položku a zrušte zaškrtnutí tlačítka **Zastaveno**.</span><span class="sxs-lookup"><span data-stu-id="e25e3-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
