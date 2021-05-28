---
title: Číslo dávky se vymaže, když je vybráno nové ID dávky
description: Při kontrole řádku deníku výběrových seznamů se hodnota v poli Číslo dávky vymaže, pokud v poli ID dávky vyberete novou hodnotu.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026322"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="f5487-103">Číslo dávky se vymaže, když je vybráno nové ID dávky</span><span class="sxs-lookup"><span data-stu-id="f5487-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="f5487-104">Číslo článku znalostní báze: 4613107</span><span class="sxs-lookup"><span data-stu-id="f5487-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="f5487-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="f5487-105">Symptoms</span></span>

<span data-ttu-id="f5487-106">Při kontrole řádku deníku výběrových seznamů se hodnota v poli **Číslo dávky** vymaže, pokud v poli **ID dávky** vyberete novou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f5487-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="f5487-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="f5487-107">Resolution</span></span>

<span data-ttu-id="f5487-108">Systém se chová tak, jak byl navržen.</span><span class="sxs-lookup"><span data-stu-id="f5487-108">The system is behaving as designed.</span></span> <span data-ttu-id="f5487-109">Pokud změníte ID dávky, změníte kontext položky.</span><span class="sxs-lookup"><span data-stu-id="f5487-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="f5487-110">Proto je číslo dávky resetováno.</span><span class="sxs-lookup"><span data-stu-id="f5487-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="f5487-111">Chcete-li přidružit číslo dávky k ID dávky, musíte nejprve nastavit ID dávky.</span><span class="sxs-lookup"><span data-stu-id="f5487-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
