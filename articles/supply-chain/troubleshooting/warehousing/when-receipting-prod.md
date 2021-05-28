---
title: Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček
description: Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026336"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="a0f0f-103">Na jednom dokladu je vytištěn pouze jeden štítek pro více pracovních hlaviček</span><span class="sxs-lookup"><span data-stu-id="a0f0f-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="a0f0f-104">Číslo článku znalostní báze: 4614667</span><span class="sxs-lookup"><span data-stu-id="a0f0f-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="a0f0f-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="a0f0f-105">Symptoms</span></span>

<span data-ttu-id="a0f0f-106">Pro stejnou cílovou registrační značku je vytvořeno více pracovních hlaviček jako součást jedné události přijetí aplikace skladu.</span><span class="sxs-lookup"><span data-stu-id="a0f0f-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="a0f0f-107">Po přijetí produktu je však vytištěn pouze jeden štítek s registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="a0f0f-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="a0f0f-108">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="a0f0f-108">Resolution</span></span>

<span data-ttu-id="a0f0f-109">Systém se chová tak, jak byl navržen.</span><span class="sxs-lookup"><span data-stu-id="a0f0f-109">The system is behaving as designed.</span></span>

<span data-ttu-id="a0f0f-110">V aktuálním designu je vždy vygenerován jeden štítek registračních značek vozidla, bez ohledu na počet existujících kombinací hlavičky a pracovní linky.</span><span class="sxs-lookup"><span data-stu-id="a0f0f-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="a0f0f-111">Vygenerovaný štítek obsahuje informace pouze pro jednu kombinaci.</span><span class="sxs-lookup"><span data-stu-id="a0f0f-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="a0f0f-112">Chcete-li tento problém vyřešit, ujistěte se, že vytváření hlavičky práce je vždy mapováno pouze na jednu cílovou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="a0f0f-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
