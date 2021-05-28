---
title: Z řádků prognózy nemůžete odstranit dimenzi prognózy poptávky skladu
description: Z řádků prognózy nemůžete odstranit dimenzi prognózy poptávky skladu.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026340"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="3a690-103">Z řádků prognózy nemůžete odstranit dimenzi prognózy poptávky skladu</span><span class="sxs-lookup"><span data-stu-id="3a690-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="3a690-104">Číslo článku znalostní báze: 4614408</span><span class="sxs-lookup"><span data-stu-id="3a690-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="3a690-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="3a690-105">Symptoms</span></span>

<span data-ttu-id="3a690-106">K tomuto problému dochází, když dimenze **Sklad** není přiřazena na kartě **Dimenze prognózy** stránky **Parametr prognózy poptávky**.</span><span class="sxs-lookup"><span data-stu-id="3a690-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="3a690-107">Sloupec **Sklad** se však na stránce **Prognóza poptávky** zobrazuje (**Hlavní plánování \> Prognóza \> Entita ruční prognózy \> Řádky prognózy poptávky**).</span><span class="sxs-lookup"><span data-stu-id="3a690-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="3a690-108">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="3a690-108">Resolution</span></span>

<span data-ttu-id="3a690-109">Nastavení na kartě **Dimenze prognózy** na stránce **Parametr prognózy poptávky** neovlivňuje stránku **Prognóza poptávky**.</span><span class="sxs-lookup"><span data-stu-id="3a690-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="3a690-110">Řídí základní prognózu, která se generuje a zobrazuje v upravené prognóze poptávky.</span><span class="sxs-lookup"><span data-stu-id="3a690-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="3a690-111">Neřídí však rozměry, které jsou vyžadovány pro „skutečnou“ prognózu poptávky.</span><span class="sxs-lookup"><span data-stu-id="3a690-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="3a690-112">Autorizací záznamů, které jsou zobrazeny na stránce **Upravená prognóza poptávky**, je můžete převést na „skutečné“ položky prognózy pro model prognózy.</span><span class="sxs-lookup"><span data-stu-id="3a690-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="3a690-113">Tento model lze poté použít pro hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="3a690-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="3a690-114">Na stránce **Prognóza poptávky** jsou dimenze pro „skutečnou“ prognózu, které se zobrazují na řádcích prognózy poptávky, součástí dimenzí zásob.</span><span class="sxs-lookup"><span data-stu-id="3a690-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="3a690-115">(Toto chování se podobá chování pro řádky prodejní objednávky.) Pokud váš systém není nastaven na použití **Skladu** jako povinné dimenze zásob, můžete stránku upravit tak, aby se sloupec skryl.</span><span class="sxs-lookup"><span data-stu-id="3a690-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
