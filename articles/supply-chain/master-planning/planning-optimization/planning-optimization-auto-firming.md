---
title: Automatické potvrzení s optimalizací plánování
description: Toto téma vysvětluje, jak používat automatické potvrzování s optimalizací plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783146"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="8e9bd-103">Automatické potvrzení s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="8e9bd-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e9bd-104">Automatické potvrzení umožňuje potvrdit (tj. vydat) plánované objednávky v rámci procesu hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="8e9bd-105">Při potvrzení jsou plánované objednávky transformovány do skutečných nákupních objednávek, převodních příkazů nebo výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="8e9bd-106">Je-li použita optimalizace plánování, budou plánované objednávky během hlavního plánování potvrzeny v okamžiku, kdy datum objednávky (tj. datum zahájení) spadá do ochranné doby pro potvrzení.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="8e9bd-107">K automatickému potvrzení plánované nákupní objednávky může dojít pouze tehdy, pokud je položka přidružena k dodavateli.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="8e9bd-108">Zapnout automatické potvrzování</span><span class="sxs-lookup"><span data-stu-id="8e9bd-108">Turn on auto-firming</span></span>

<span data-ttu-id="8e9bd-109">Chcete-li zapnout automatické potvrzování, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="8e9bd-110">V pracovním prostoru **Správa funkcí** na kartě **Nová** vyberte v seznamu **automatické potvrzení pro optimalizaci plánování**.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="8e9bd-111">Pokud se tato funkce nezobrazí na kartě **Nová**, podívejte se na karty **Není povoleno** a **Vše**.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="8e9bd-112">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-112">Select **Enable now**.</span></span> <span data-ttu-id="8e9bd-113">Můžete také vybrat možnost **Plán** a vybrat čas, kdy má být funkce zapnuta.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="8e9bd-114">Nastavení časového ohraničení potvrzení</span><span class="sxs-lookup"><span data-stu-id="8e9bd-114">Set up the firming time fence</span></span>

<span data-ttu-id="8e9bd-115">Ochranná doba potvrzení se počítá od data spuštění hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="8e9bd-116">Definuje ji počet dní, které zadáte.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="8e9bd-117">Ochrannou dobu potvrzování můžete řídit následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="8e9bd-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="8e9bd-118">Chcete-li definovat výchozí ochrannou dobu potvrzování pro skupinu disponibility, přejděte na **Hlavní plánování** \> **Nastavení** \> **Disponibilita** \> **Skupiny disponibility** a vyberte skupinu disponibility.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="8e9bd-119">Pak na pevné záložce **Jiné** zadejte do pole **Ochranná doba automatického potvrzování (ve dnech)** počet dní.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="8e9bd-120">Pokud chcete přepsat ochrannou dobu potvrzení definovanou pro skupinu pokrytí pro konkrétní položku, přejděte na **Správa informací o produktu** \> **Vydané produkty**, v podokně akcí vyberte **Plán** a pak vyberte **Pokrytí položky**.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the action pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="8e9bd-121">Potom na kartě **Obecné** vyberte **Přepsat ochrannou lhůtu** a do pole **Automatická ochranná lhůta (dny)** zadejte počet dní.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="8e9bd-122">Chcete-li přepsat ochrannou dobu potvrzování definovanou pro skupinu disponibility a disponibilitu položky pro určitý hlavní plán, přejděte na **Hlavní plánování** \> **Nastavení** \> **Hlavní plány** a vyberte hlavní plán.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="8e9bd-123">Pak na pevné záložce **Ochranná doba ve dnech** nastavte **Zmrazit** na **Ano** a zadejte počet dní.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="8e9bd-124">Je-li pro spuštění hlavního plánování, které používá optimalizaci plánování, zapnuto automatické potvrzování, bude proces automatického potvrzování proveden v souladu s nastavením automatického potvrzování.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="8e9bd-125">Pokud není zapnuto automatické potvrzování nebo pokud je plánování zahájeno ze stránky **Požadavky netto**, bude proces automatického potvrzování přeskočen.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="8e9bd-126">Optimalizace plánování vs. předdefinovaný modul plánování správy zásobovacího řetězce</span><span class="sxs-lookup"><span data-stu-id="8e9bd-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="8e9bd-127">Optimalizaci plánování i plánovací modul, který je integrovaný v Microsoft Dynamics 365 Supply Chain Management, lze použít k automatickému potvrzování plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="8e9bd-128">Existují však některé důležité rozdíly.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-128">However, there are some important differences.</span></span> <span data-ttu-id="8e9bd-129">Pokud například optimalizace plánování použije datum objednávky (tj. počáteční datum) k určení, které plánované objednávky mají být potvrzeny, použije předdefinovaný modul plánování pro správu zásobovacího řetězce datum požadavku (tj. koncové datum).</span><span class="sxs-lookup"><span data-stu-id="8e9bd-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="8e9bd-130">Zde je souhrn rozdílů.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="8e9bd-131">**Optimalizace plánování**</span><span class="sxs-lookup"><span data-stu-id="8e9bd-131">**Planning Optimization**</span></span>

- <span data-ttu-id="8e9bd-132">Automatické potvrzení je založeno na datu objednávky (počáteční datum).</span><span class="sxs-lookup"><span data-stu-id="8e9bd-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="8e9bd-133">Vzhledem k tomu, že datum objednávky (počáteční datum) aktivuje potvrzení, nemusíte považovat dobu realizace za součást ochranné doby potvrzení.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="8e9bd-134">Chcete-li potvrdit všechny objednávky, které musí být zahájeny v aktuálním týdnu, musí být ochranná doba potvrzování jeden týden.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="8e9bd-135">**Integrovaný modul plánování v Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="8e9bd-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="8e9bd-136">Automatické potvrzení je založeno na datu požadavku (koncové datum).</span><span class="sxs-lookup"><span data-stu-id="8e9bd-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="8e9bd-137">Chcete-li zajistit, aby byly příkazy potvrzeny včas, musí být ochranná doba potvrzení delší než doba realizace.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="8e9bd-138">Chcete-li potvrdit všechny objednávky, které musí být zahájeny v aktuálním týdnu, musí být ochranná doba potvrzování doba realizace plus jeden týden.</span><span class="sxs-lookup"><span data-stu-id="8e9bd-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>