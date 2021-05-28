---
title: Pokud je množství hmotnosti úlovku rozděleno, použije se místo nominálního množství minimální množství
description: Když je množství hmotnosti úlovku rozděleno do dávek, používá pole Vyskladněné množství minimální množství, které je pro položku nastaveno, nikoli nominální množství.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026346"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="1894d-103">Pokud je množství hmotnosti úlovku rozděleno, použije se místo nominálního množství minimální množství</span><span class="sxs-lookup"><span data-stu-id="1894d-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="1894d-104">Číslo článku znalostní báze: 4612073</span><span class="sxs-lookup"><span data-stu-id="1894d-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="1894d-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="1894d-105">Symptoms</span></span>

<span data-ttu-id="1894d-106">Když je množství hmotnosti úlovku rozděleno do dávek, používá pole **Vyskladněné množství** minimální množství, které je pro položku nastaveno, nikoli nominální množství.</span><span class="sxs-lookup"><span data-stu-id="1894d-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="1894d-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="1894d-107">Resolution</span></span>

<span data-ttu-id="1894d-108">Systém se chová tak, jak byl navržen.</span><span class="sxs-lookup"><span data-stu-id="1894d-108">The system is behaving as designed.</span></span> <span data-ttu-id="1894d-109">Systém používá k vychystávání nastavení minimálního množství každé položky.</span><span class="sxs-lookup"><span data-stu-id="1894d-109">The system uses each item's minimum quantity setup for picking.</span></span>
