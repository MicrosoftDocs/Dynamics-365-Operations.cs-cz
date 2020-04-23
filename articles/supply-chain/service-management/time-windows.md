---
title: Časová okna
description: Časová okna slouží k optimalizaci plánování řádků servisních zakázek.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63a166806c2c8ac84cc1d71d6ec84fcb28033feb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206512"
---
# <a name="time-windows"></a><span data-ttu-id="a7dab-103">Časová okna</span><span class="sxs-lookup"><span data-stu-id="a7dab-103">Time windows</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7dab-104">Časová okna slouží k optimalizaci plánování řádků servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="a7dab-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="a7dab-105">Systém lze nastavit tak, aby automaticky vytvořil servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="a7dab-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="a7dab-106">Na základě kritérií určených časovým oknem můžete připojit co nejvíce řádků servisních objednávek k co možná nejméně servisním objednávkám.</span><span class="sxs-lookup"><span data-stu-id="a7dab-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="a7dab-107">Časová okna určují, jak daleko lze přesunout řádek servisní zakázky z jeho vypočteného data.</span><span class="sxs-lookup"><span data-stu-id="a7dab-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="a7dab-108">Vypočtené datum je datem, na které byl naplánován řádek servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="a7dab-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="a7dab-109">Datum je založeno na nastavení intervalu a servisním období, které jste definovali na stránce **Vytváření servisních zakázek**.</span><span class="sxs-lookup"><span data-stu-id="a7dab-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="a7dab-110">Časové okno definujete pomocí hodnot v následující tabulce:</span><span class="sxs-lookup"><span data-stu-id="a7dab-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="a7dab-111">Metoda</span><span class="sxs-lookup"><span data-stu-id="a7dab-111">Method</span></span> | <span data-ttu-id="a7dab-112">popis</span><span class="sxs-lookup"><span data-stu-id="a7dab-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7dab-113">Týden</span><span class="sxs-lookup"><span data-stu-id="a7dab-113">Week</span></span>   | <span data-ttu-id="a7dab-114">Datum, kdy řádek servisní zakázky lze přesunout na libovolný otevřený den ve stejném týdnu jako počáteční vypočtené datum.</span><span class="sxs-lookup"><span data-stu-id="a7dab-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="a7dab-115">Měsíc</span><span class="sxs-lookup"><span data-stu-id="a7dab-115">Month</span></span>  | <span data-ttu-id="a7dab-116">Datum, kdy řádek servisní zakázky lze přesunout na libovolný otevřený den ve stejném měsíci jako počáteční vypočtené datum.</span><span class="sxs-lookup"><span data-stu-id="a7dab-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="a7dab-117">Například vypočítané datum pro řádek servisní zakázky je 15. února 2017.</span><span class="sxs-lookup"><span data-stu-id="a7dab-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="a7dab-118">Řádek servisní zakázky lze naplánovat pro všechny pracovní dny mezi 1. a 28. únorem 2017.</span><span class="sxs-lookup"><span data-stu-id="a7dab-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="a7dab-119">Ruční</span><span class="sxs-lookup"><span data-stu-id="a7dab-119">Manual</span></span> | <span data-ttu-id="a7dab-120">Definujte maximální počet dní před nebo po vypočteném datu, kdy lze přesunout řádek servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="a7dab-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="a7dab-121">Pokud neurčíte pro řádek servisní smlouvy žádné časové okno, je nutné provést řádek servisní zakázky odvozené od servisní smlouvy přesně v den, na který bylo jeho provedení původně plánováno.</span><span class="sxs-lookup"><span data-stu-id="a7dab-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7dab-122">Související témata</span><span class="sxs-lookup"><span data-stu-id="a7dab-122">Related topics</span></span>

[<span data-ttu-id="a7dab-123">Tvorba časových oken</span><span class="sxs-lookup"><span data-stu-id="a7dab-123">Create time windows</span></span>](create-time-windows.md)

