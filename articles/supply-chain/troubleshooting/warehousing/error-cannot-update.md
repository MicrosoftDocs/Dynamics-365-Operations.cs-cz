---
title: Dojde k chybě, když je místo vybráno během registrace výběrového seznamu
description: Dojde k chybě, když je místo vybráno během registrace výběrového seznamu.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026321"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="76373-103">Dojde k chybě, když je místo vybráno během registrace výběrového seznamu</span><span class="sxs-lookup"><span data-stu-id="76373-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="76373-104">Číslo článku znalostní báze: 4613106</span><span class="sxs-lookup"><span data-stu-id="76373-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="76373-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="76373-105">Symptoms</span></span>

<span data-ttu-id="76373-106">K tomuto problému dochází, když je váš systém nakonfigurován tak, aby automaticky rezervoval prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="76373-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="76373-107">Pokud se pokusíte vybrat umístění pro řádek registrace výběrového seznamu, zobrazí se při použití procesů rezervace skladu (WMS) následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="76373-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="76373-108">Množství nelze aktualizovat pomocí nových dimenzí</span><span class="sxs-lookup"><span data-stu-id="76373-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="76373-109">K tomuto problému může dojít, protože na zadaném místě nemáte dostatek skladových zásob.</span><span class="sxs-lookup"><span data-stu-id="76373-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="76373-110">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="76373-110">Resolution</span></span>

<span data-ttu-id="76373-111">Systém se chová tak, jak byl navržen.</span><span class="sxs-lookup"><span data-stu-id="76373-111">The system is behaving as designed.</span></span>

<span data-ttu-id="76373-112">Ve scénářích, kde použijete proces rezervace na úrovni skladu, pokud nebudou zásoby po ruce rezervovány na všech úrovních dimenze skladu a v zadaném umístění nemáte dostatečné zásoby po ruce, doporučujeme použít proces ruční rezervace z vychystávací linky.</span><span class="sxs-lookup"><span data-stu-id="76373-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="76373-113">Poté můžete použít funkci *Rezervní šarže* pro distribuci nižších rezervací, jako například umístění, pro všechna dostupná množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="76373-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
