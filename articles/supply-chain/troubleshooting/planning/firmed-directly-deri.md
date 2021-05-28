---
title: Přímo odvozené potvrzené objednávky jsou zpracovávány v rámci workflow kontroly
description: Přímo odvozené potvrzené objednávky jsou zpracovávány workflow, který má stav Probíhá kontrola.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026345"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="870f9-103">Přímo odvozené potvrzené objednávky jsou zpracovávány v rámci workflow kontroly</span><span class="sxs-lookup"><span data-stu-id="870f9-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="870f9-104">Číslo článku znalostní báze: 4612450</span><span class="sxs-lookup"><span data-stu-id="870f9-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="870f9-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="870f9-105">Symptoms</span></span>

<span data-ttu-id="870f9-106">Přímo odvozené potvrzené objednávky jsou zpracovávány workflow, který má stav *Probíhá kontrola*.</span><span class="sxs-lookup"><span data-stu-id="870f9-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="870f9-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="870f9-107">Resolution</span></span>

<span data-ttu-id="870f9-108">Když je povoleno sledování změn, bude potvrzeným odvozeným objednávkám (dílčí nákupní objednávky) přidělen stav *Probíhá kontrola*.</span><span class="sxs-lookup"><span data-stu-id="870f9-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="870f9-109">Pokud je tedy nákupní objednávka odvozena (nákupní objednávka na subdodávku), odešle se pouze do pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="870f9-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="870f9-110">Pokud je nákupní objednávka pevně plánovanou nákupní objednávkou, je automaticky schválena, aby bylo zajištěno, že plánovací modul nevytvoří nové plánované objednávky, dokud je nákupní objednávka stále ve stavu *Koncept*.</span><span class="sxs-lookup"><span data-stu-id="870f9-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
