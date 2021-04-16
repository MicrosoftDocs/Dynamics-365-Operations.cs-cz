---
title: Řešení potíží s nastavením předpovědi peněžních toků
description: Toto téma obsahuje odpovědi na otázky, které můžete mít při konfiguraci předpovědí peněžních toků. Řeší často kladené otázky (FAQ) týkající se nastavení peněžních toků, aktualizací peněžních toků a Power BI peněžních toků.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827307"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="bc58b-104">Řešení potíží s nastavením předpovědi peněžních toků</span><span class="sxs-lookup"><span data-stu-id="bc58b-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc58b-105">Toto téma obsahuje odpovědi na otázky, které můžete mít při konfiguraci předpovědí peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="bc58b-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="bc58b-106">Řeší často kladené otázky (FAQ) týkající se nastavení peněžních toků, aktualizací peněžních toků a Power BI peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="bc58b-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="bc58b-107">Proč se peněžní tok zobrazuje pouze u jedné právnické osoby?</span><span class="sxs-lookup"><span data-stu-id="bc58b-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="bc58b-108">Prognóza peněžních toků je konfigurována a vypočítávána podle právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="bc58b-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="bc58b-109">Zprávy Power BI a prognózy peněžních toků ve statistikách Finance Insights ukazují výsledky.</span><span class="sxs-lookup"><span data-stu-id="bc58b-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="bc58b-110">Pro každou právnickou osobu, pro kterou chcete zobrazit prognózu, je třeba nastavit prognózu peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="bc58b-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="bc58b-111">Zkontrolujte konfiguraci prognózy peněžních toků u všech vašich právnických osob.</span><span class="sxs-lookup"><span data-stu-id="bc58b-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="bc58b-112">Alternativně zkontrolujte konfiguraci všech právnických osob na prognózu peněžních toků a ujistěte se, že jsou nastaveny tak, jak jste zamýšleli.</span><span class="sxs-lookup"><span data-stu-id="bc58b-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="bc58b-113">Proč Power BI nezobrazuje všechny údaje o peněžních tocích?</span><span class="sxs-lookup"><span data-stu-id="bc58b-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="bc58b-114">Než se mohou objevit prognózy peněžních toků v zobrazeních Power BI, je třeba provést několik kroků.</span><span class="sxs-lookup"><span data-stu-id="bc58b-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="bc58b-115">Projděte si následující kontrolní seznam a ujistěte se, že byly provedeny všechny kroky:</span><span class="sxs-lookup"><span data-stu-id="bc58b-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="bc58b-116">Nastavte peněžní tok pro každou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="bc58b-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="bc58b-117">V parametrech hlavní knihy nastavte systémovou měnu a typ směnného kurzu systému.</span><span class="sxs-lookup"><span data-stu-id="bc58b-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="bc58b-118">Nastavte účetní měnu hlavní knihy a typ směnného kurzu.</span><span class="sxs-lookup"><span data-stu-id="bc58b-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="bc58b-119">Zadejte směnný kurz mezi měnou transakce a zúčtovací měnou.</span><span class="sxs-lookup"><span data-stu-id="bc58b-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="bc58b-120">Zadejte směnný kurz mezi zúčtovací měnou a měnou systému.</span><span class="sxs-lookup"><span data-stu-id="bc58b-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="bc58b-121">Zadejte směnný kurz mezi zúčtovací měnou a měnami jednotlivých bank.</span><span class="sxs-lookup"><span data-stu-id="bc58b-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="bc58b-122">Proč peněžní tok Power BI fungoval v předchozích verzích, ale nyní je prázdný?</span><span class="sxs-lookup"><span data-stu-id="bc58b-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="bc58b-123">Ověřte, že byla nakonfigurována měření „Cash flow measure V2“ a „LedgerCovLiquidityMeasurement“ z úložiště Entity.</span><span class="sxs-lookup"><span data-stu-id="bc58b-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="bc58b-124">Další informace o práci s daty v úložišti entit získáte v tématu [Integrace Power BI s úložištěm entit](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="bc58b-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="bc58b-125">Ověřte, zda byly dokončeny všechny kroky potřebné k zobrazení obsahu Power BI.</span><span class="sxs-lookup"><span data-stu-id="bc58b-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="bc58b-126">Další informace naleznete v tématu [Přehled hotovosti obsahu Power BI](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="bc58b-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="bc58b-127">Byly entity úložiště Entity aktualizovány?</span><span class="sxs-lookup"><span data-stu-id="bc58b-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="bc58b-128">Musíte pravidelně obnovovat své entity, abyste zajistili, že data jsou aktuální a přesná.</span><span class="sxs-lookup"><span data-stu-id="bc58b-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="bc58b-129">Chcete-li ručně aktualizovat konkrétní entitu, přejděte na **Správa systému \> Nastavení \> Úložiště Entity**, vyberte entitu a poté vyberte **Obnovit**.</span><span class="sxs-lookup"><span data-stu-id="bc58b-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="bc58b-130">Data lze také aktualizovat automaticky.</span><span class="sxs-lookup"><span data-stu-id="bc58b-130">The data can also be updated automatically.</span></span> <span data-ttu-id="bc58b-131">Na stránce **Úložiště Entity** nastavte možnost **Automatické obnovení povoleno** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="bc58b-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="bc58b-132">Jakou metodu výpočtu je třeba použít při výpočtu prognóz cashflow?</span><span class="sxs-lookup"><span data-stu-id="bc58b-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="bc58b-133">Metoda výpočtu prognózy cashflow má dvě důležité možnosti výběru.</span><span class="sxs-lookup"><span data-stu-id="bc58b-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="bc58b-134">Možnost **Nový** vypočítá prognózy cashflow pro nové dokumenty a dokumenty, které se změnily v době po spuštění poslední dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="bc58b-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="bc58b-135">Tato možnost obvykle probíhá rychleji, protože zpracovává menší podmnožinu dokumentů.</span><span class="sxs-lookup"><span data-stu-id="bc58b-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="bc58b-136">Možnost **Celkem** přepočítá prognózy cashflow pro každý dokument v systému.</span><span class="sxs-lookup"><span data-stu-id="bc58b-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="bc58b-137">Tato možnost trvá déle, protože má větší rozsah práce.</span><span class="sxs-lookup"><span data-stu-id="bc58b-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="bc58b-138">Jak mohu zlepšit výkonnost opakující se dávkové úlohy předpovědi cashflow?</span><span class="sxs-lookup"><span data-stu-id="bc58b-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="bc58b-139">Doporučujeme předpovědi cashflow spouštět jednou za den mimo špičku a použít metodu výpočtu **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bc58b-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="bc58b-140">Doporučujeme používat tento přístup šest dní v týdnu.</span><span class="sxs-lookup"><span data-stu-id="bc58b-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="bc58b-141">Poté jednou týdně spusťte prognózu cashflow využívající metodu výpočtu **Celkem**, a to v den s nejmenším množstvím aktivity.</span><span class="sxs-lookup"><span data-stu-id="bc58b-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

