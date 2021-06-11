---
title: Nastavení kódů důvodů
description: Aplikace Dynamics 365 Human Resources používá kódy důvodu k vysvětlení důvodu změny zaměstnaneckých výhod.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6fc641233a1bd217de5b9eb6e06560b989f91c7b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056341"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="09995-103">Nastavení kódů důvodů</span><span class="sxs-lookup"><span data-stu-id="09995-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09995-104">Aplikace Dynamics 365 Human Resources používá kódy důvodu k vysvětlení důvodu změny zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="09995-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="09995-105">Od ledna 2021 migrují kódy důvodu do pracovního prostoru **Správa zaměstnanců** místo pracovního prostoru **Správa zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="09995-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="09995-106">Další informace viz [Ruční migrace kódů důvodů do Správy zaměstnanců](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="09995-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="09995-107">Vytvoření kódů rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="09995-107">Create reason codes</span></span>

1. <span data-ttu-id="09995-108">V pracovním prostoru **Správa zaměstnanců** (nebo pracovním prostoru **Správa zaměstnaneckých výhod**, pokud vaše kódy důvodu ještě nebyly migrovány) vyberte **Odkazy** a potom vyberte **Kódy důvodů**.</span><span class="sxs-lookup"><span data-stu-id="09995-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="09995-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="09995-109">Select **New**.</span></span>

3. <span data-ttu-id="09995-110">Zadejte hodnoty pro zbývající pole:</span><span class="sxs-lookup"><span data-stu-id="09995-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="09995-111">Pole</span><span class="sxs-lookup"><span data-stu-id="09995-111">Field</span></span> | <span data-ttu-id="09995-112">Popis</span><span class="sxs-lookup"><span data-stu-id="09995-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09995-113">**Kód důvodu**</span><span class="sxs-lookup"><span data-stu-id="09995-113">**Reason code**</span></span> | <span data-ttu-id="09995-114">Jedinečný název pro identifikaci důvodu, kdy zaměstnanec změnil zápis plánu zaměstnaneckých výhod.</span><span class="sxs-lookup"><span data-stu-id="09995-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="09995-115">**Popis**</span><span class="sxs-lookup"><span data-stu-id="09995-115">**Description**</span></span> | <span data-ttu-id="09995-116">Popis kódu důvodu.</span><span class="sxs-lookup"><span data-stu-id="09995-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="09995-117">V **Použitelné scénáře** nastavte **Správa zaměstnaneckých výhod** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="09995-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="09995-118">(Nepoužije se, pokud vaše kódy důvodu dosud nemigrovaly do pracovního prostoru **Správa zaměstnanců**.)</span><span class="sxs-lookup"><span data-stu-id="09995-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="09995-119">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="09995-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="09995-120">Ruční migrace kódů důvodů do Správy zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="09995-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="09995-121">V lednu 2021 migrují kódy důvodu do pracovního prostoru **Správa zaměstnanců** místo pracovního prostoru **Správa zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="09995-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="09995-122">Data kódu většiny důvodů se automaticky přenesou do vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="09995-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="09995-123">Některá data kódů důvodu nemusí migrovat.</span><span class="sxs-lookup"><span data-stu-id="09995-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="09995-124">Například kódy důvodu mají nyní maximálně 15 znaků, takže jakékoli kódy příčiny delší než 15 znaků nebudou migrovány automaticky.</span><span class="sxs-lookup"><span data-stu-id="09995-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="09995-125">Uvidíte banner na stránce **Odkazy** pracovního prostoru **Správa zaměstnaneckých výhod**, který vás informuje o migraci a o tom, zda kódy důvodu neprovedly migraci.</span><span class="sxs-lookup"><span data-stu-id="09995-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="09995-126">Vyberte **Kódy důvodů** pro podrobnosti o stavu migrace.</span><span class="sxs-lookup"><span data-stu-id="09995-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="09995-127">[![Kódy důvodu](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="09995-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="09995-128">Vyberte kód důvodu, který se nepodařilo migrovat.</span><span class="sxs-lookup"><span data-stu-id="09995-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="09995-129">[![Stav migrace kódu důvodu](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="09995-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="09995-130">Vyberte **Migrujte kód důvodu**.</span><span class="sxs-lookup"><span data-stu-id="09995-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="09995-131">[![Migrovat kód důvodu](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="09995-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="09995-132">V podokně **Migrace kódu důvodu zaměstnaneckých výhod** máte dvě možnosti pro mapování na kód důvodu Správy zaměstnanců:</span><span class="sxs-lookup"><span data-stu-id="09995-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="09995-133">Chcete-li ve správě zaměstnanců použít existující kód důvodu, vyberte jeden důvod v rozbalovací nabídce **Použít stávající kód důvodu**.</span><span class="sxs-lookup"><span data-stu-id="09995-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="09995-134">Existující kód důvodu můžete použít ve správě zaměstnanců pouze v případě, že na něj již jiný kód důvodu správy výhod nebyl migrován.</span><span class="sxs-lookup"><span data-stu-id="09995-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="09995-135">Chcete-li ve správě zaměstnanců vytvořit nový kód důvodu, zadejte nový v **Nový kód důvodu** a poté zadejte popis do **Nový popis**.</span><span class="sxs-lookup"><span data-stu-id="09995-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="09995-136">[![Namapujte na kód důvodu správy zaměstnanců](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="09995-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="09995-137">Po migraci kódů důvodu na správu zaměstnanců je možnost jejich použití ve správě zaměstnaneckých výhod automaticky nastavena na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="09995-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="09995-138">[![Použít ód důvodu ve správě zaměstnaneckých výhod](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="09995-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]