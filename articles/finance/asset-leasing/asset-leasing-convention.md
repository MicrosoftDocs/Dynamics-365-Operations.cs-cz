---
title: Konvence leasingu aktiv
description: Toto téma popisuje konvence leasingu aktiv.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237509"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="ada21-103">Konvence leasingu aktiv</span><span class="sxs-lookup"><span data-stu-id="ada21-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ada21-104">Toto téma popisuje konvence leasingu aktiv.</span><span class="sxs-lookup"><span data-stu-id="ada21-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="ada21-105">K určení data zahájení knihy leasingu se používají konvence pro leasing.</span><span class="sxs-lookup"><span data-stu-id="ada21-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="ada21-106">Pokud je konvence leasingu nastavena na **Žádný**, datum zahájení je stejné jako datum zahájení leasingu (tj. hodnota pole **Datum zahájení leasingu**).</span><span class="sxs-lookup"><span data-stu-id="ada21-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="ada21-107">Pokud je konverze leasingu nastavena na **Celý měsíc**, jako datum zahájení se použije první den měsíce, do kterého spadá datum zahájení leasingu.</span><span class="sxs-lookup"><span data-stu-id="ada21-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="ada21-108">Datum zahájení určuje datum zahájení období pro plány amortizace závazků a odpisů aktiv.</span><span class="sxs-lookup"><span data-stu-id="ada21-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="ada21-109">Úrokové náklady a odpisy jsou zaúčtovány k datu ukončení období příslušných plánů.</span><span class="sxs-lookup"><span data-stu-id="ada21-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="ada21-110">Počáteční uznání a zápis do deníku úprav se zaúčtují v den zahájení.</span><span class="sxs-lookup"><span data-stu-id="ada21-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="ada21-111">Funkce pro konvence leasingu musí být zapnutá prostřednictvím správy funkcí.</span><span class="sxs-lookup"><span data-stu-id="ada21-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="ada21-112">V pracovním prostoru **Správa funkcí** vyhledejte a vyberte funkci, která se jmenuje **Konvence leasingu pro leasing majetku** a poté vyberte **Povolit nyní**.</span><span class="sxs-lookup"><span data-stu-id="ada21-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="ada21-113">Konvence leasingu jsou přiřazeny nastavení pro knihu pronájmu aktiv.</span><span class="sxs-lookup"><span data-stu-id="ada21-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="ada21-114">Chcete-li zobrazit nebo přiřadit konvenci leasingu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ada21-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="ada21-115">Přejděte na **Leasing majetku \> Nastavení \> Leasingové knihy**.</span><span class="sxs-lookup"><span data-stu-id="ada21-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="ada21-116">V poli **Konvence leasingu** vyberte některou z následujících hodnot.</span><span class="sxs-lookup"><span data-stu-id="ada21-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="ada21-117">Leasingová smlouva</span><span class="sxs-lookup"><span data-stu-id="ada21-117">Leasing convention</span></span> | <span data-ttu-id="ada21-118">popis</span><span class="sxs-lookup"><span data-stu-id="ada21-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="ada21-119">Není</span><span class="sxs-lookup"><span data-stu-id="ada21-119">None</span></span>               | <span data-ttu-id="ada21-120">Odpisy závazků a odpisy majetku začínají dnem zahájení leasingu, protože datum zahájení se rovná datu zahájení leasingu.</span><span class="sxs-lookup"><span data-stu-id="ada21-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="ada21-121">Datum ukončení je o měsíc později.</span><span class="sxs-lookup"><span data-stu-id="ada21-121">The end date is one month later.</span></span> <span data-ttu-id="ada21-122">Tato konvence leasingu nezaručuje, že úroky budou zaúčtovány v poslední den každého měsíce.</span><span class="sxs-lookup"><span data-stu-id="ada21-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="ada21-123">Celý měsíc</span><span class="sxs-lookup"><span data-stu-id="ada21-123">Full month</span></span>         | <span data-ttu-id="ada21-124">U leasingů, jejichž počáteční datum nastane kdykoli během měsíce, se odpisy závazků a odpisy aktiv začnou časově rozlišovat od prvního dne daného měsíce.</span><span class="sxs-lookup"><span data-stu-id="ada21-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="ada21-125">Tato konvence leasingu zajišťuje, že úroky se kumulují poslední den každého měsíce po celý měsíc.</span><span class="sxs-lookup"><span data-stu-id="ada21-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="ada21-126">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ada21-126">Select **Save**.</span></span>

<span data-ttu-id="ada21-127">Když je vytvořen leasing, datum zahájení každé knihy se automaticky zadá na základě data zahájení, které je zadáno pro leasing, a leasingové konvence, která je pro knihu zadána.</span><span class="sxs-lookup"><span data-stu-id="ada21-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]