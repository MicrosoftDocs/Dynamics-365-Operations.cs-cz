---
title: Fyzicky přijaté nákupní objednávky se v závěrečném přehledu zásob neobjeví
description: Fyzicky přijaté nákupní objednávky se neobjeví v závěrečném přehledu zásob Zkontrolovat otevřená množství.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026337"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="e4723-103">Fyzicky přijaté nákupní objednávky se v závěrečném přehledu zásob neobjeví</span><span class="sxs-lookup"><span data-stu-id="e4723-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="e4723-104">Číslo článku znalostní báze: 4612595</span><span class="sxs-lookup"><span data-stu-id="e4723-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="e4723-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="e4723-105">Symptoms</span></span>

<span data-ttu-id="e4723-106">Fyzicky přijaté nákupní objednávky se neobjeví v závěrečném přehledu zásob **Zkontrolovat otevřená množství**.</span><span class="sxs-lookup"><span data-stu-id="e4723-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4723-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="e4723-107">Resolution</span></span>

<span data-ttu-id="e4723-108">Zpráva **Zkontrolujte otevřené množství** zobrazuje transakce vystavení, které nelze k vybranému datu uzávěrky vypořádat proti finančně aktualizovaným příjmům ze skladu.</span><span class="sxs-lookup"><span data-stu-id="e4723-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="e4723-109">Můžete se rozhodnout zahrnout do sestavy fyzické příjmy.</span><span class="sxs-lookup"><span data-stu-id="e4723-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="e4723-110">V takovém případě se zobrazí fyzické příjmy, pokud mohou pokrýt emisní transakce, které nelze vypořádat.</span><span class="sxs-lookup"><span data-stu-id="e4723-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="e4723-111">Další informace naleznete v tématu [Příprava na spuštění zásob](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="e4723-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
