---
title: Vybrané číslo receptury není pro dávkovou objednávku schváleno
description: Při pokusu o potvrzení plánované objednávky se zobrazí chybová zpráva s oznámením, že vybrané číslo receptury není pro dávkovou objednávku schváleno.
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
ms.openlocfilehash: 4f993c92ca0a2f8f79e4b0e0eda43904529163f8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294025"
---
# <a name="selected-formula-number-isnt-approved-for-a-batch-order"></a><span data-ttu-id="186c2-103">Vybrané číslo receptury není pro dávkovou objednávku schváleno</span><span class="sxs-lookup"><span data-stu-id="186c2-103">Selected formula number isn't approved for a batch order</span></span>

<span data-ttu-id="186c2-104">Kód chyby: PRO2614</span><span class="sxs-lookup"><span data-stu-id="186c2-104">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="186c2-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="186c2-105">Symptoms</span></span>

<span data-ttu-id="186c2-106">Když se pokusíte potvrdit objednávku, zobrazí se následující chybová zpráva:</span><span class="sxs-lookup"><span data-stu-id="186c2-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="186c2-107">Vybrané číslo receptury není pro dávkovou objednávku schváleno.</span><span class="sxs-lookup"><span data-stu-id="186c2-107">The selected formula number is not approved for a batch order.</span></span>

## <a name="cause"></a><span data-ttu-id="186c2-108">Příčina</span><span class="sxs-lookup"><span data-stu-id="186c2-108">Cause</span></span>

<span data-ttu-id="186c2-109">Systém ověří potvrzení, aby se ujistil, že pro aktivní položku je k dispozici schválená receptura.</span><span class="sxs-lookup"><span data-stu-id="186c2-109">The system validates the firming operation to make sure that an approved formula is available for the active item.</span></span> <span data-ttu-id="186c2-110">Pravděpodobně musíte recepturu schválit.</span><span class="sxs-lookup"><span data-stu-id="186c2-110">You must probably approve the formula.</span></span>

## <a name="resolution"></a><span data-ttu-id="186c2-111">Řešení</span><span class="sxs-lookup"><span data-stu-id="186c2-111">Resolution</span></span>

<span data-ttu-id="186c2-112">Chcete-li schválit recepturu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="186c2-112">To approve a formula, follow these steps.</span></span>

1. <span data-ttu-id="186c2-113">Přejděte do nabídky **Řízení informací o produktech \> Kusovníky a receptury \> Receptury**.</span><span class="sxs-lookup"><span data-stu-id="186c2-113">Go to **Product information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="186c2-114">Vyberte příslušnou recepturu.</span><span class="sxs-lookup"><span data-stu-id="186c2-114">Select the relevant formula.</span></span>
1. <span data-ttu-id="186c2-115">V podokně akcí na kartě **Receptura** ve skupině **Spravovat** zvolte **Schválit recepturu**.</span><span class="sxs-lookup"><span data-stu-id="186c2-115">On the Action Pane, on the **Formula** tab, in the **Maintain** group, select **Approve formula**.</span></span>
1. <span data-ttu-id="186c2-116">V dialogovém okně **Schválit kusovník nebo recepturu** okně vyberte schvalovatele a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="186c2-116">In the **Approve BOM or formula** dialog box, select an approver, and then select **OK**.</span></span>
