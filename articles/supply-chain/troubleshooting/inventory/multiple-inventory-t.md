---
title: Více skladových transakcí pro čísla šarží, když je zakázána fyzická aktualizace
description: Po úpravě řádku nákupní objednávky u položek, kde je možnost Při fyzické aktualizaci skupiny čísel dávek nastavena na Ne, se vytvoří více transakcí zásob.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026351"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="a8db9-103">Více skladových transakcí pro čísla šarží, když je zakázána fyzická aktualizace</span><span class="sxs-lookup"><span data-stu-id="a8db9-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="a8db9-104">Číslo článku znalostní báze: 4613390</span><span class="sxs-lookup"><span data-stu-id="a8db9-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="a8db9-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="a8db9-105">Symptoms</span></span>

<span data-ttu-id="a8db9-106">Po úpravě řádku nákupní objednávky u položek, kde je možnost **Při fyzické aktualizaci** skupiny čísel dávek nastavena na *Ne*, se vytvoří více transakcí zásob.</span><span class="sxs-lookup"><span data-stu-id="a8db9-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="a8db9-107">Když vytvoříte položku, kde je volba **Při fyzické aktualizaci** skupiny čísel šarží nastavena na *Ne*, systém automaticky vytvoří nové číslo šarže, pokud upravíte množství řádku nákupu a uložíte stránku nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a8db9-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="a8db9-108">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="a8db9-108">Resolution</span></span>

<span data-ttu-id="a8db9-109">Nastavení **Při fyzické aktualizaci** pro skupiny čísel šarží funguje následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="a8db9-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="a8db9-110">Když je tato volba nastavena na *Ano*, nová čísla šarží se vytvoří až po fyzické aktualizaci (například při odeslání nebo přijetí zboží).</span><span class="sxs-lookup"><span data-stu-id="a8db9-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="a8db9-111">Když je tato volba nastavena na *Ne*, nové číslo šarže se vytvoří pokaždé, když dojde k příslušné aktualizaci (například při přidání nového množství k nákupní objednávce).</span><span class="sxs-lookup"><span data-stu-id="a8db9-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
