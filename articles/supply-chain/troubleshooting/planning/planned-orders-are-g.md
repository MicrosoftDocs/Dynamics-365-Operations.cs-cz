---
title: Hlavní plánování generuje plánované objednávky pro demonstrační produkty
description: Plánované objednávky se generují po spuštění hlavního plánování.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026344"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="655f1-103">Hlavní plánování generuje plánované objednávky pro demonstrační produkty</span><span class="sxs-lookup"><span data-stu-id="655f1-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="655f1-104">Číslo článku znalostní báze: 4614729</span><span class="sxs-lookup"><span data-stu-id="655f1-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="655f1-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="655f1-105">Symptoms</span></span>

<span data-ttu-id="655f1-106">Plánované objednávky se generují po spuštění hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="655f1-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="655f1-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="655f1-107">Resolution</span></span>

<span data-ttu-id="655f1-108">Nastavení možnosti **Demonstrační** pro vydané produkty určuje výchozí typ řádku na kusovníku (BOM).</span><span class="sxs-lookup"><span data-stu-id="655f1-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="655f1-109">Když je možnost **Demonstrační** je nastavena na *Ano*, systém bude i nadále vytvářet plánované objednávky pro položku, ale možnost **Přímo odvozený požadavek** pro každou plánovanou objednávku bude nastavena na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="655f1-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="655f1-110">Proto nelze plánovanou výrobní zakázku zpracovat samostatně.</span><span class="sxs-lookup"><span data-stu-id="655f1-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="655f1-111">Místo toho bude vždy automaticky zahrnut, když je nadřazená výrobní zakázka spuštěna.</span><span class="sxs-lookup"><span data-stu-id="655f1-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="655f1-112">Řádky kusovníku plánované demonstrační objednávky budou navíc zahrnuty do kusovníku nadřazené výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="655f1-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
