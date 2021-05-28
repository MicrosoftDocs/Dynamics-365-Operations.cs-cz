---
title: Při importu záznamů prognózy poptávky nemůžete aktualizovat předpokládané jednotkové náklady
description: Když použijete datové entity k importu záznamů prognózy poptávky, nákladová cena pro stávající záznamy se neaktualizuje tak, aby odpovídala importovaným datům.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026341"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="ff458-103">Při importu záznamů prognózy poptávky nemůžete aktualizovat předpokládané jednotkové náklady</span><span class="sxs-lookup"><span data-stu-id="ff458-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="ff458-104">Číslo článku znalostní báze: 4614109</span><span class="sxs-lookup"><span data-stu-id="ff458-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="ff458-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="ff458-105">Symptoms</span></span>

<span data-ttu-id="ff458-106">Když použijete datové entity k importu záznamů prognózy poptávky, hodnota **Prognózovaná jednotková cena** pro stávající záznamy se neaktualizuje tak, aby odpovídala importovaným datům.</span><span class="sxs-lookup"><span data-stu-id="ff458-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="ff458-107">Příčina</span><span class="sxs-lookup"><span data-stu-id="ff458-107">Cause</span></span>

<span data-ttu-id="ff458-108">**Předpokládané jednotkové náklady** je pole jen pro čtení.</span><span class="sxs-lookup"><span data-stu-id="ff458-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="ff458-109">Hodnota je založena na jednotkové ceně produktu a nelze ji nastavit přímo pomocí importu.</span><span class="sxs-lookup"><span data-stu-id="ff458-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="ff458-110">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="ff458-110">Resolution</span></span>

<span data-ttu-id="ff458-111">Protože je pole jen pro čtení, nemůžete pro něj importovat hodnoty.</span><span class="sxs-lookup"><span data-stu-id="ff458-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="ff458-112">Hodnota bude vypočítána podle stávající obchodní logiky.</span><span class="sxs-lookup"><span data-stu-id="ff458-112">The value will be calculated according to the existing business logic.</span></span>
