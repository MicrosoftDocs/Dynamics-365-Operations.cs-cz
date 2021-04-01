---
title: Řešení potíží s nastavením předpovědi peněžních toků
description: Toto téma obsahuje odpovědi na otázky, které můžete mít při konfiguraci předpovědí peněžních toků. Řeší často kladené otázky (FAQ) týkající se nastavení peněžních toků, aktualizací peněžních toků a Power BI peněžních toků.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232482"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="1a83b-104">Řešení potíží s nastavením předpovědi peněžních toků</span><span class="sxs-lookup"><span data-stu-id="1a83b-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a83b-105">Toto téma obsahuje odpovědi na otázky, které můžete mít při konfiguraci předpovědí peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="1a83b-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="1a83b-106">Řeší často kladené otázky (FAQ) týkající se nastavení peněžních toků, aktualizací peněžních toků a Power BI peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="1a83b-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="1a83b-107">Proč se peněžní tok zobrazuje pouze u jedné právnické osoby?</span><span class="sxs-lookup"><span data-stu-id="1a83b-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="1a83b-108">Prognóza peněžních toků je konfigurována a vypočítávána podle právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="1a83b-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="1a83b-109">Zprávy Power BI a prognózy peněžních toků ve statistikách Finance Insights ukazují výsledky.</span><span class="sxs-lookup"><span data-stu-id="1a83b-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="1a83b-110">Pro každou právnickou osobu, pro kterou chcete zobrazit prognózu, je třeba nastavit prognózu peněžních toků.</span><span class="sxs-lookup"><span data-stu-id="1a83b-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="1a83b-111">Zkontrolujte konfiguraci prognózy peněžních toků u všech vašich právnických osob.</span><span class="sxs-lookup"><span data-stu-id="1a83b-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="1a83b-112">Alternativně zkontrolujte konfiguraci všech právnických osob na prognózu peněžních toků a ujistěte se, že jsou nastaveny tak, jak jste zamýšleli.</span><span class="sxs-lookup"><span data-stu-id="1a83b-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="1a83b-113">Proč Power BI nezobrazuje všechny údaje o peněžních tocích?</span><span class="sxs-lookup"><span data-stu-id="1a83b-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="1a83b-114">Než se mohou objevit prognózy peněžních toků v zobrazeních Power BI, je třeba provést několik kroků.</span><span class="sxs-lookup"><span data-stu-id="1a83b-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="1a83b-115">Projděte si následující kontrolní seznam a ujistěte se, že byly provedeny všechny kroky:</span><span class="sxs-lookup"><span data-stu-id="1a83b-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="1a83b-116">Nastavte peněžní tok pro každou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="1a83b-117">V parametrech hlavní knihy nastavte systémovou měnu a typ směnného kurzu systému.</span><span class="sxs-lookup"><span data-stu-id="1a83b-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="1a83b-118">Nastavte účetní měnu hlavní knihy a typ směnného kurzu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="1a83b-119">Zadejte směnný kurz mezi měnou transakce a zúčtovací měnou.</span><span class="sxs-lookup"><span data-stu-id="1a83b-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="1a83b-120">Zadejte směnný kurz mezi zúčtovací měnou a měnou systému.</span><span class="sxs-lookup"><span data-stu-id="1a83b-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="1a83b-121">Zadejte směnný kurz mezi zúčtovací měnou a měnami jednotlivých bank.</span><span class="sxs-lookup"><span data-stu-id="1a83b-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="1a83b-122">Proč peněžní tok Power BI fungoval v předchozích verzích, ale nyní je prázdný?</span><span class="sxs-lookup"><span data-stu-id="1a83b-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="1a83b-123">Ověřte, že byla nakonfigurována měření „Cash flow measure V2“ a „LedgerCovLiquidityMeasurement“ z úložiště Entity.</span><span class="sxs-lookup"><span data-stu-id="1a83b-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="1a83b-124">Další informace o tom, jak pracovat s daty v úložišti Entity, najdete v tématu [Integrace Power BI s úložištěm Entity](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Ověřte, zda byly provedeny všechny kroky potřebné k zobrazení obsahu Power BI.</span><span class="sxs-lookup"><span data-stu-id="1a83b-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="1a83b-125">Další informace naleznete v tématu [Přehled hotovosti obsahu Power BI](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="1a83b-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="1a83b-126">Byly entity úložiště Entity aktualizovány?</span><span class="sxs-lookup"><span data-stu-id="1a83b-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="1a83b-127">Musíte pravidelně obnovovat své entity, abyste zajistili, že data jsou aktuální a přesná.</span><span class="sxs-lookup"><span data-stu-id="1a83b-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="1a83b-128">Chcete-li ručně aktualizovat konkrétní entitu, přejděte na **Správa systému \> Nastavení \> Úložiště Entity**, vyberte entitu a poté vyberte **Obnovit**.</span><span class="sxs-lookup"><span data-stu-id="1a83b-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="1a83b-129">Data lze také aktualizovat automaticky.</span><span class="sxs-lookup"><span data-stu-id="1a83b-129">The data can also be updated automatically.</span></span> <span data-ttu-id="1a83b-130">Na stránce **Úložiště Entity** nastavte možnost **Automatické obnovení povoleno** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="1a83b-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]